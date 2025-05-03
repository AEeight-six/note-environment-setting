## 一 为Windows安装C编译器（MinGW-W64 GCC）

<略>

参考之前的文章：[Windows下安装C编译器MinGW](https://www.cnblogs.com/xiaml/articles/17391725.html)

## 二 安装并配置Visual Studio Code

下载VSCode，下载地址为：[https://code.visualstudio.com/](https://link.zhihu.com/?target=https%3A//code.visualstudio.com/)，在网页中点击”Download for Windows“按钮即可下载。当然，还可以点击按钮右侧紧挨的向下的箭头选择不同操作系统的VSCode版本。

下载下来是一个exe的安装文件，`VSCodeUserSetup-x64-<version>.exe`。

VSCode的安装比较简单，根据提示一路`下一步`完成安装，完成后在开始菜单下就会有“Visual Studio Code”了，点击打开。

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511172632002-447057873.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511172632002-447057873.png)

打开后，如下图。左侧边栏是几个快速的按钮，点击**最下面**的“Extensions”（扩展）按钮。

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511172643712-796694257.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511172643712-796694257.png)

在随后出现的”扩展市场“的搜索框中输入”C/C++“，在随后出现的列表中选择对应的扩展，确认是Microsoft发布的，就点击”Install“按钮即可安装。

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511172656984-1736907631.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511172656984-1736907631.png)

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511172710868-542962749.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511172710868-542962749.png)

等待一会，出现uninstall按钮就代表安装完成了。

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511172722277-1655036568.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511172722277-1655036568.png)

安装完”C/C++"扩展后，安装“Code Runner”扩展，方法相同。

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511172735314-349991729.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511172735314-349991729.png)

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511172745636-888952340.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511172745636-888952340.png)

两个扩展安装完成后，对“Code Runner”扩展进行配置，在“File”菜单下找到“Preference”再找到“Settings”子菜单或者直接使用快捷方式`CTRL+,`。

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511172801875-2029553701.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511172801875-2029553701.png)

依此找到"Extensions"->"Code Runner Configuration"。并勾选：

-   Run in Terminal
-   Save All File Before Run
-   Save File Before Run

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511172822128-646247774.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511172822128-646247774.png)

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511172830976-2101341739.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511172830976-2101341739.png)

VSCode及其扩展的安装、配置就完成了。

在你喜欢的位置创建一个文件夹，建议使用纯英文字符的名。

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511172844366-1269797429.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511172844366-1269797429.png)

随后，打开VSCode，然后在”File“菜单下找到”Open Folder“子菜单，并点击。

定位到刚刚创建的新文件夹，然后点击”选择文件夹“按钮。

当然，如果你刚打开VSCode，没有选定文件夹，它也会出现一个”Open Folder“按钮，你通过这个按钮选择刚刚创建的文件夹效果是一样的。

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511172855696-1332008118.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511172855696-1332008118.png)

选择”Yes,……“。

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511172907434-1630760489.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511172907434-1630760489.png)

鼠标移动到打开的文件夹处会出现4个快捷按钮，点击左边第一个就可以给文件夹创建一个新的文件，命名为”hello.c“。

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511172920480-1295604919.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511172920480-1295604919.png)

在”hello.c“文件中输入代码；比如：

cpp

```
  # include</span>  &lt;stdio.h&gt;</span></span>
 
   int</span>  main</span> ()</span></span>{
      printf</span>( "hello world! I\' m xiamingliang。\n"</span>);
   return</span>  0</span>;
 }
```

并保存。

## 四 配置编译和Debug设定

重点来了，代码编辑完成后还不能直接运行。还需要配置两个json文件。

-   tasks.json 用来是设置指令编译代码。
-   launch.json 设置执行环境来执行代码。（如果不设置每次点击调试的时候都需要手动选择debugger）

### tasks.json配置文件

首先，在”Terminal“菜单下点击”Configure Tasks...”子菜单。在随后出现的弹出框中选择“C/C++:gcc.exe生成活动文件”

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511172935406-2124100203.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511172935406-2124100203.png)

随后，在“MyC”文件夹中会自动生成一个“.vscode"的子文件夹，在这个子文件夹下自动创建一个”tasks.json“的文件。

不用做任何改动。

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511172949025-1865046899.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511172949025-1865046899.png)

json

```
 {
  "version"</span>:  "2.0.0"</span>,
  "tasks"</span>: [
 {
  "type"</span>:  "cppbuild"</span>,
  "label"</span>:  "C/C++: gcc.exe 生成活动文件"</span>,
  "command"</span>:  "D:\\MinGW\\C\\mingw64\\bin\\gcc.exe"</span>,
  "args"</span>: [
  "-fdiagnostics-color=always"</span>,
  "-g"</span>,
  "${file}"</span>,
  "-o"</span>,
  "${fileDirname}\\${fileBasenameNoExtension}.exe"</span>
 ],
  "options"</span>: {
  "cwd"</span>:  "${fileDirname}"</span>
 },
  "problemMatcher"</span>: [
  "$gcc"</span>
 ],
  "group"</span>:  "build"</span>,
  "detail"</span>:  "编译器: D:\\MinGW\\C\\mingw64\\bin\\gcc.exe"</span>
 }
 ]
 }
```

最后，回到“hello.c”文件，单击鼠标右键选择“Run Code”即可运行代码。

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173006868-325036079.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173006868-325036079.png)

运行结果会在下面出现的“Terminal”中显示；这里乱码是使用了中文的字符导致的，先忽略吧。

如果想要调试代码的话呢？点击“Run”菜单下的“Start Debugging”子菜单或者使用`F5`快捷键。

在随后出现的弹出框中选择“C++(GDB/LLDB)”，再选择”gcc.exe“。

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173018581-1929469570.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173018581-1929469570.png)

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173028902-2098202035.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173028902-2098202035.png)

这个时候就可以进入调试，如果我们将代码改一下，并设置断点。

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173044075-480542287.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173044075-480542287.png)

这个时候，进入调试（F5快捷键）如下：运行到scanf那一行后在terminal中等待我们输入，假设输入“10,20"，然后回车。

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173056039-1158774758.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173056039-1158774758.png)

F10执行下一行。

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173107127-1056612201.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173107127-1056612201.png)

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173117480-959594280.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173117480-959594280.png)

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173125961-819753118.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173125961-819753118.png)

当然，也可以在调试的时候使用”DEBUG CONSOLE“进行适当指令的输入以检查程序是否按照我们的设想在执行。

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173138997-579673680.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173138997-579673680.png)

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173148800-1487702607.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173148800-1487702607.png)

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173200446-1536426893.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173200446-1536426893.png)

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173210728-1219291578.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173210728-1219291578.png)

### launch.json配置文件

为了避免每次调试都要选择”Debugger”，我们再“Run”->"Add Configuration..."

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173221143-843078275.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173221143-843078275.png)

vscode会自动帮我们生成launch.json配置文件。

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173232667-1222719410.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173232667-1222719410.png)

我们需要修改这个配置文件以匹配我们当前的环境。

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173243333-696129095.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173243333-696129095.png)

内容比较多，参考这里（直接复制粘贴）：

卖个关子，这里有坑！！

json

```
 {
     
     
     
      "version"</span>:  "0.2.0"</span>,
      "configurations"</span>: [
         {
              "name"</span>:  "MyLaunch"</span>,              
              "type"</span>:  "cppdbg"</span>,                    
              "request"</span>:  "launch"</span>,                 
              "program"</span>:  "${workspaceFolder}/${fileBasenameNoExtension}.out"</span>, 
              "miDebuggerPath"</span>:  "D:\\MinGW\\C\\mingw64\\bin\\gcc.exe"</span>,    
              "preLaunchTask"</span>: "build"</span>,             
              "args"</span>: [],                          
              "stopAtEntry"</span>:  false</span>,
              "cwd"</span>:  "${workspaceFolder}"</span>,         
              "environment"</span>: [],                   
              "externalConsole"</span>:  true</span>,
              "MIMode"</span>:  "gdb"</span>,                     
              "setupCommands"</span>: [
                 {
                      "description"</span>:  "Enable pretty-printing for gdb"</span>,
                      "text"</span>:  "-enable-pretty-printing"</span>,
                      "ignoreFailures"</span>:  true</span>
                 }
             ]
         }
     ]
 }
```

## 排个错

上面的配置下有问题：

`Could not find the task 'build'.`

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173306913-1155570991.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173306913-1155570991.png)

明天排查！！！！

继续：

提示已经说到问题的重点了，找不到task（名字叫build）；原因是tasks.json中代表task名字的字段lable默认是

1c

```
  "label"</span>:  "C/C++: gcc.exe 生成活动文件"</span>,
```

而launch.json中指定的preLaunchTask字段却是

1c

```
  "preLaunchTask"</span>: "build"</span>,  
```  

导致vscode认为找不到名字叫build的task。

因此，解决把方法就是；修改tasks.json或者launch.json使

launch.json的preLaunchTask字段和tasks.json的lable字段值一致即可。

我这里调整下launch.json的preLaunchTask字段

json

```
 {
     
     
     
      "version"</span>:  "0.2.0"</span>,
      "configurations"</span>: [
         {
              "name"</span>:  "MyLaunch"</span>,              
              "type"</span>:  "cppdbg"</span>,                    
              "request"</span>:  "launch"</span>,                 
              "program"</span>:  "${workspaceFolder}/${fileBasenameNoExtension}.out"</span>, 
              "miDebuggerPath"</span>:  "D:\\MinGW\\C\\mingw64\\bin\\gcc.exe"</span>,    
              "preLaunchTask"</span>:  "C/C++: gcc.exe 生成活动文件"</span>,             
              "args"</span>: [],                          
              "stopAtEntry"</span>:  false</span>,
              "cwd"</span>:  "${workspaceFolder}"</span>,         
              "environment"</span>: [],                   
              "externalConsole"</span>:  true</span>,
              "MIMode"</span>:  "gdb"</span>,                     
              "setupCommands"</span>: [
                 {
                      "description"</span>:  "Enable pretty-printing for gdb"</span>,
                      "text"</span>:  "-enable-pretty-printing"</span>,
                      "ignoreFailures"</span>:  true</span>
                 }
             ]
         }
     ]
 }
```

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173323439-316395667.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173323439-316395667.png)

再次执行debug（右上角的小虫子或者F5或者"Run"->"Start Debuging"）

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173333159-1854668956.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173333159-1854668956.png)

选择MyLaunch；他是我们在launch.json中指定的name。

再次出现报错：  
[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173341632-535247020.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173341632-535247020.png)

## 继续排错

报错信息：

`launch: program 'D:\MyC\hello.out' does not exist`

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173355106-1149670825.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173355106-1149670825.png)

有经验的童鞋很明显可以看出debug过程中准备执行"D:\\MyC\\hello.out"，但是这个文件不存在；为什么会这样呢？

还是因为tasks.json和launch.json中的字段互相没关联起来导致的。

tasks.json中指定-o输出的文件名后缀是exe：

bash

```
  "args"</span>: [
  "-fdiagnostics-color=always"</span>,
  "-g"</span>,
  " ${file}</span>"</span>,
  "-o"</span>,
  " ${fileDirname}</span>\\ ${fileBasenameNoExtension}</span>.exe"</span>
 ],
```

而launch.json中准备执行的文件后缀却是out：

dart

```
  "program"</span>:  " ${workspaceFolder}</span>/ ${fileBasenameNoExtension}</span>.out"</span>, 
``` 

因此，解决办法是修改两个配置文件中的任意一个使他们的后缀保持一致即可，我们还是调整launch.json的program字段；修改后的配置文件为：

json

```
 {
     
     
     
      "version"</span>:  "0.2.0"</span>,
      "configurations"</span>: [
         {
              "name"</span>:  "MyLaunch"</span>,              
              "type"</span>:  "cppdbg"</span>,                    
              "request"</span>:  "launch"</span>,                 
              "program"</span>:  "${workspaceFolder}/${fileBasenameNoExtension}.exe"</span>, 
              "miDebuggerPath"</span>:  "D:\\MinGW\\C\\mingw64\\bin\\gcc.exe"</span>,    
              "preLaunchTask"</span>:  "C/C++: gcc.exe 生成活动文件"</span>,             
              "args"</span>: [],                          
              "stopAtEntry"</span>:  false</span>,
              "cwd"</span>:  "${workspaceFolder}"</span>,         
              "environment"</span>: [],                   
              "externalConsole"</span>:  true</span>,
              "MIMode"</span>:  "gdb"</span>,                     
              "setupCommands"</span>: [
                 {
                      "description"</span>:  "Enable pretty-printing for gdb"</span>,
                      "text"</span>:  "-enable-pretty-printing"</span>,
                      "ignoreFailures"</span>:  true</span>
                 }
             ]
         }
     ]
 }
```

保存并验证。

又遇到报错：

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173414097-2112250858.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173414097-2112250858.png)

## 继续排错

报错信息：

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173419232-386835489.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173419232-386835489.png)

主要信息：

vim

```
 gcc. exe</span>: error: unrecognized  command</span>  line</span> option  '--interpreter=mi'</span>
```

原因：

这里其实是网上某些教程的错误导致的；launch.json中指定的调试器位置应该指向gdb.exe而不是gcc.exe；

因为gcc.exe是编译程序主要作用是将文本内容的.c源码转换为可执行的程序.exe(一般习惯)，

gdb.exe才是用来程序进行调试的工具。

swift

```
  "miDebuggerPath"</span>:  "D: \\</span>MinGW \\</span>C \\</span>mingw64 \\</span>bin \\</span>gcc.exe"</span>,    
```    

因此，需要将launch.json中的"miDebuggerPath"修改为：

swift

```
  "miDebuggerPath"</span>:  "D: \\</span>MinGW \\</span>C \\</span>mingw64 \\</span>bin \\</span>gdb.exe"</span>,    
```    

最终解决办法（lauch.json的完整配置）：

json

```
 {
     
     
     
      "version"</span>:  "0.2.0"</span>,
      "configurations"</span>: [
         {
              "name"</span>:  "MyLaunch"</span>,              
              "type"</span>:  "cppdbg"</span>,                    
              "request"</span>:  "launch"</span>,                 
              "program"</span>:  "${workspaceFolder}/${fileBasenameNoExtension}.exe"</span>, 
              "miDebuggerPath"</span>:  "D:\\MinGW\\C\\mingw64\\bin\\gdb.exe"</span>,    
              "preLaunchTask"</span>:  "C/C++: gcc.exe 生成活动文件"</span>,             
              "args"</span>: [],                          
              "stopAtEntry"</span>:  false</span>,
              "cwd"</span>:  "${workspaceFolder}"</span>,         
              "environment"</span>: [],                   
              "externalConsole"</span>:  true</span>,
              "MIMode"</span>:  "gdb"</span>,                     
              "setupCommands"</span>: [
                 {
                      "description"</span>:  "Enable pretty-printing for gdb"</span>,
                      "text"</span>:  "-enable-pretty-printing"</span>,
                      "ignoreFailures"</span>:  true</span>
                 }
             ]
         }
     ]
 }
```

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173438227-1256611451.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173438227-1256611451.png)

再次验证。

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/3195567-20230511173448237-448601941.png)](https://img2023.cnblogs.com/blog/3195567/202305/3195567-20230511173448237-448601941.png)

坑已填完，顺利上岸！！

-   [一 为Windows安装C编译器（MinGW-W64 GCC）](https://www.cnblogs.com/xiaml/articles/17391759.html#%E4%B8%80-%E4%B8%BAwindows%E5%AE%89%E8%A3%85c%E7%BC%96%E8%AF%91%E5%99%A8mingw-w64-gcc)
-   [二 安装并配置Visual Studio Code](https://www.cnblogs.com/xiaml/articles/17391759.html#%E4%BA%8C-%E5%AE%89%E8%A3%85%E5%B9%B6%E9%85%8D%E7%BD%AEvisual-studio-code)
-   [三 开发C语言工程](https://www.cnblogs.com/xiaml/articles/17391759.html#%E4%B8%89-%E5%BC%80%E5%8F%91c%E8%AF%AD%E8%A8%80%E5%B7%A5%E7%A8%8B)
-   [四 配置编译和Debug设定](https://www.cnblogs.com/xiaml/articles/17391759.html#%E5%9B%9B-%E9%85%8D%E7%BD%AE%E7%BC%96%E8%AF%91%E5%92%8Cdebug%E8%AE%BE%E5%AE%9A)
-       [tasks.json配置文件](https://www.cnblogs.com/xiaml/articles/17391759.html#tasksjson%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6)
-       [launch.json配置文件](https://www.cnblogs.com/xiaml/articles/17391759.html#launchjson%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6)
-   [排个错](https://www.cnblogs.com/xiaml/articles/17391759.html#%E6%8E%92%E4%B8%AA%E9%94%99)
-   [继续排错](https://www.cnblogs.com/xiaml/articles/17391759.html#%E7%BB%A7%E7%BB%AD%E6%8E%92%E9%94%99)
-   [继续排错](https://www.cnblogs.com/xiaml/articles/17391759.html#%E7%BB%A7%E7%BB%AD%E6%8E%92%E9%94%99-1)

\_\_EOF\_\_

[![](VS%20Code%E9%85%8D%E7%BD%AEC%E8%AF%AD%E8%A8%80%E5%BC%80%E5%8F%91%E4%B8%8E%E8%B0%83%E8%AF%95%E7%8E%AF%E5%A2%83(%E8%B6%85%E8%AF%A6%E7%BB%86)%20-%20Arthur%E5%8F%A4%E5%BE%B7%E6%9B%BC%20-%20%E5%8D%9A%E5%AE%A2%E5%9B%AD/20230511120122.png)](https://pic.cnblogs.com/avatar/3195567/20230511120122.png)

-   **本文作者：** [xiamingliang's blog](https://www.cnblogs.com/xiaml)
-   **本文链接：** [https://www.cnblogs.com/xiaml/articles/17391759.html](https://www.cnblogs.com/xiaml/articles/17391759.html)
-   **关于博主：** 永远的萌新一名，像疯子一样热爱生活，希望每天都有新的进步；记录点滴，记录人生，可能并不惊艳但它时真实的！
-   **版权声明：** 本博客所有文章除特别声明外，均采用 [BY-NC-SA](https://creativecommons.org/licenses/by-nc-nd/4.0/ "BY-NC-SA") 许可协议。转载请注明出处！
-   **声援博主：** 如果您觉得文章对您有帮助，可以点击文章右下角**【推荐】**一下。