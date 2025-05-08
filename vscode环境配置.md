Vscode只是一款文本编辑器，虽然衍生功能强大，但是需要对其做环境配置


下载c/c++插件和c/c++ compile run插件
此时编写好了代码，仍然需要配置

主要配置三个json文件
c_cpp_properties.json
c/c++配置用文件，比如头文件路径，全局定义等
launch.json
调试配置，按F5启动调试时，从该配置文件读取设置和相关配置
tasks.json
调试配置，对应launch.json文件中的preLaunchTask项
settings.json
工程设置，编译设置等

### 各json文件的作用
首先，确保你已经将OpenCV的静态库文件添加到你的项目目录中，并记下这些文件的路径。

然后，在你的VSCode项目中，创建一个"tasks.json"文件，用于定义编译任务。在这个文件中，你需要指定编译器命令，包括OpenCV的包含路径和链接库路径。

接下来，你需要创建一个"launch.json"文件，用于配置调试器。在这个文件中，你需要指定可执行文件的路径。

最后，你需要在你的源代码中包含OpenCV的头文件，并链接OpenCV的静态库。

详细的设置步骤取决于你的具体项目结构和编译环境，但通常情况下，以上提到的几个步骤是连接OpenCV静态库到VSCode项目所需的基本步骤。




**c_cpp_properties.json**
这个文件专门用于配置 ​​C/C++ IntelliSense​​（代码提示、错误检查等），而 tasks.json 仅控制编译行为。
需要配置的有：
* 包含目录：
  * 1.工作区里自定义头文件路径 "${workspaceFolder}/**
  * 2.一些外部库的头文件路径（不进行包含的话会提示检查错误）
* 编译器路径
  * 选择自定义的编译器路径即可 


**一、一般的c++工程：**
1.c_cpp_properties.json
```
{
    "configurations": [
        {
            "name": "Win32",                  //没影响的设置，自定义名称
            "includePath": [
                "${workspaceFolder}/**"      //包含目录只包括了工作区，两个**代表需要递归查找子目录
            ],
            "defines": [
                "_DEBUG",
                "UNICODE",
                "_UNICODE"
            ],
            "compilerPath": "C:/Program Files/mingw64/bin/g++.exe", //编译器的路径
            "cStandard": "c17",                              //C语言标准
            "cppStandard": "gnu++14",                    //c++标准
            "intelliSenseMode": "windows-gcc-x64"      //配置用于智能感知的模式（代码检查）
        }
    ],
    "version": 4
}
```
**task.json**
用于告诉编译器编译的参数指定等信息，调试参数写在"args": [...]中
2.task.json
```
{
    "version": "2.0.0",
    "tasks": [
        {
            "type": "cppbuild",
            "label": "C/C++: gcc.exe 生成活动文件", //要和Launch.json中的PrelaunchTask配置名一致
            "command": "C:/Program Files/mingw64/bin/g++.exe",//要改成你自己的编译器地址

            "args": [
                "-g",
                "${file}",

            //外部库和头文件的路径，按实际填写，要满足其格式

                "-I", "E:/OpenCV_4.5.5/build/install/include",   //告诉编译器外部库头文件路径
                "-L", "E:/OpenCV_4.5.5/build/install/x64/mingw/lib",//告诉编译器外部库文件路径
                "-l", "opencv_world455",           //具体要链接的库名

                "-o",
                "${workspaceFolder}/exe/${fileBasenameNoExtension}.exe"//把生成的.exe文件放到exe文件夹中
            ], 
            //上述相当于在命令行下输入了: gcc 源文件.c -o 源文件 -I 头文件路径 -L 库文件路径 -l 库名
            
            "options": {
                "cwd": "${workspaceFolder}" //Current working directory (当前工作目录)
            },
            "problemMatcher": [
                "$gcc"
            ],
            "group": {
                "kind": "build",
                "isDefault": true
            },
            "detail": "调试器生成的任务。" //无关紧要的描述信息
        }
    ]
}
```
**launch.json**
这里要配置的是动态库的加载路径，调试器的路径

3.launch.json
```
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "gcc.exe - 生成和调试活动文件",    //自定义的名称
            "type": "cppdbg",
            "request": "launch",
            "program": "${workspaceFolder}/exe/${fileBasenameNoExtension}.exe",//要启动的exe文件路径，和Task.json中一样即可


            "args": [],
            "stopAtEntry": false,
            "cwd": "${workspaceFolder}",
            "environment": [

                 "name": "PATH",
                //如果要用到动态库，那么运行时这里指定动态库的路径
                //这一句的含义是将动态库的路径添加到总的环境变量中而不是进行覆盖，如果不加;$(env:PATH),就会对原来的环境变量覆盖了，到时候会找不到gcc之类的运行库，大概表现为窗口闪退崩溃的呢过，其实在设置将动态库的路径添加到总环境变量中是更好选择

                "value": "E:/OpenCV_4.5.5/build/install/x64/mingw/bin;${env:PATH}"


            ],
            "externalConsole": true,//这个设置用于调出外部终端
            "MIMode": "gdb",
            "miDebuggerPath": "C:/Program Files/mingw64/bin/gdb.exe",//改成自己的调试器路径
            "setupCommands": [
                {
                    "description": "为 gdb 启用整齐打印",
                    "text": "-enable-pretty-printing",
                    "ignoreFailures": true
                }
            ],
            "preLaunchTask": "C/C++: gcc.exe 生成活动文件"     //和task.json的label一致
        }
    ]
}
```



**2.连接第三方库Opencv环境配置**

**2.1 Msvc（微软）编译器**
由于mingw编译器需要posix型和非posix型进行区分，而且下载的微软已编译win版本的Opencv没有给到mingw编译器的接口，踩坑太多暂时先采用了msvc版本的编译器



(1)打开visual studio本地的64位cmd，启动code
其实本质上还是因为没有配置环境变量，因为如果不这样启动opencv会识别不到微软编译器等环境

![](assert/cmd启动vscode.PNG)
由于已经下载过扩展了，可以在右下方选择任务的配置

![](assert/选择配置任务.PNG)
实质上在弹出的任务配置界面选择ui界面可以看到
![](assert/任务配置的ui界面.PNG)
由于我们是在vs的cmd下启动的vscode，所以可以识别到msvc编译器的选项和路径
之前不是这种启动方式的务必要从

```
C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Visual Studio 2022\Visual Studio Tools\VC
```
目录下启动
```
x64 Native Tools Command Prompt for VS 2022
```


(2)配置三个json文件

**1.c_cpp_properties.json**
```
{
    "configurations": [
        {
            "name": "Win32",
            "includePath": [
                "${workspaceFolder}/**",
                "E:/opencv/opencv-4.5.4_compile/install/include/"
            ],
            "defines": [
                "_DEBUG",
                "UNICODE",
                "_UNICODE"
            ],
            "compilerPath": "C:/Program Files/mingw64_1/bin/g++.exe",
            "cStandard": "c17",
            "cppStandard": "gnu++14",
            "intelliSenseMode": "windows-gcc-x64"
        },
        {
            "name": "MSVC",
            "includePath": [
                "D:/visual studio2022/VC/Tools/MSVC/14.36.32532/include",
                "E:/opencv/opencv/build/include/**"
            ],
            "defines": [
                "_DEBUG",
                "UNICODE",
                "_UNICODE"
            ],
            "compilerPath": "D:/visual studio2022/VC/Tools/MSVC/14.36.32532/bin/Hostx64/x86/cl.exe",
            "cStandard": "c11",
            "cppStandard": "gnu++14",
            "intelliSenseMode": "windows-msvc-x64",
            "mergeConfigurations": false,
            "browse": {
                "path": [
                    "c:/Users/64574/Desktop/repO/opencv/**",
                    "${workspaceFolder}"
                ],
                "limitSymbolsToIncludedHeaders": true
            }
        }
    ],
    "version": 4
}
```
**2.launch.json**
```
{
    // 使用 IntelliSense 了解相关属性。 
    // 悬停以查看现有属性的描述。
    // 欲了解更多信息，请访问: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "name": "(Windows msvc opencv) 启动",
            "type": "cppvsdbg",
            "request": "launch",
            "program": "${fileDirname}\\${fileBasenameNoExtension}.exe",
            "args": [],
            "stopAtEntry": false,
            "cwd": "${fileDirname}",
            "environment": [],
            "console": "externalTerminal",
            "preLaunchTask":"C/C++: cl.exe 生成活动文件 opencv"
        },
    
        {
            "name": "gcc.exe - 生成和调试活动文件",
            "type": "cppdbg",
            "request": "launch",
            "program": "${workspaceFolder}/exe/${fileBasenameNoExtension}.exe",//同task.json中的
            "args": [],
            "stopAtEntry": false,
            "cwd": "${workspaceFolder}",
            "environment": [],
            "externalConsole": true,//如果你要输入，则设置为true
            "MIMode": "gdb",
            "miDebuggerPath": "C:\\Program Files\\mingw64_1\\bin\\gdb.exe",//要改自己的路径
            "setupCommands": [
                {
                    "description": "为 gdb 启用整齐打印",
                    "text": "-enable-pretty-printing",
                    "ignoreFailures": true
                }
            ],
            "preLaunchTask": "C/C++: g++.exe 生成活动文件 opencv"
        }
    ]
}
```
**3.task.json**
```
{
    "version": "2.0.0",
    "tasks": [
        {
            "type": "cppbuild",
            "label": "C/C++: g++.exe 生成活动文件 opencv",
            "command": "C:\\Program Files\\mingw64\\bin\\g++.exe",
            "args": [
                "-g",
                "${file}",
                "-o",
                "${workspaceFolder}/exe/${fileBasenameNoExtension}.exe",
                "-L",
                "E:/opencv/opencv-4.5.4_compile/install/x64/mingw/lib",
                "-l",
                "opencv_highgui454",
                "-I",
                "E:/opencv/opencv-4.5.4_compile/install/include"
            ],
            "options": {
                "cwd": "${workspaceFolder}"
            },
            "problemMatcher": [
                "$gcc"
            ],
            "group": {
                "kind": "build",
                "isDefault": true
            },
            "detail": "调试器生成的任务。"
        },
        {
            "type": "cppbuild",
            "label": "C/C++: cl.exe 生成活动文件 opencv",
            "command": "cl.exe",
            "args": [
                "/Zi",
                "/EHsc",
                "/nologo",
                "/Fe${fileDirname}\\${fileBasenameNoExtension}.exe",
                "${file}",
                "/I\"E:\\opencv\\opencv\\build\\include\"",
                "E:\\opencv\\opencv\\build\\x64\\vc15\\lib\\opencv_world454.lib"
            ],
            "options": {
                "cwd": "${fileDirname}"
            },
            "problemMatcher": [
                "$msCompile"
            ],
            "group": "build",
            "detail": "编译器: cl.exe"
        }
    ]
}
```


快捷键的配置：
* Ctrl+Shift+B  构建
* F5            调试
* Ctrl+F5       运行

code runner配置：
如果不进行配置，默认点击三角按钮就是会不带参数的构建、运行，如果需要引入外部库的情况，这时候就会报错找不到头文件等各种错误。需要在插件的配置文件Settings.json中添加相关的参数，建议是使用vscode的快捷键进行生成、运行（依赖于task.json和launch.json的填写）

调试运行要记得是在左侧栏进行任务配置的选取后再调试
![](assert/如何调试运行.png)
![](assert/vscode_msvc运行opencv.PNG)