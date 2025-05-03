###前置准备
1.vs2022->qt插件的安装
2.opencv(4.5.4)官方编译库

**一、新建Qt工程**

**二、添加opencv包含目录**
E:\opencv\opencv\build\include
E:\opencv\opencv\build\include\opencv2


**三、添加opencv库目录**

E:\opencv\opencv\build\x64\vc15\lib

**四、添加链接器**
链接器->输入栏，选择上面库目录的对应opencv的lib文件
注意选择的lib文件是需要和工程状态相符
例如Debug选opencv_world454d.lib
release选的是opencv_world454.lib


#记得首先要包含头文件和写命名空间！再写代码



qt和vs2022联合编程

1.vs2022->qt插件的安装
2.qt添加一下环境变量
3.vs2022选择qmake作为编译器
