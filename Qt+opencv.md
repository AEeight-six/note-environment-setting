###前置准备
1.Qt5.12.1
2.opencv(4.5.4)手动编译库（动态库）

**一、新建Qt工程**

**二、添加opencv包含目录**
##
包含目录路径:
INCLUDEPATH += E:\opencv\opencv-4.5.4_compile\install\include




**三、添加opencv库目录**

动态链接库的连接:
LIBS += E:\opencv\opencv-4.5.4_compile\install\x64\mingw\bin\libopencv_*.dll

LIBS += E:\opencv\opencv-4.5.4_compile\install\x64\mingw\lib\libopencv_*.dll.a

静态链接库的连接:
LIBS+= E:\opencv\opencv\build\x64\vc15\lib\opencv_world454d.lib
LIBS+= E:\opencv\opencv\build\x64\vc15\lib\opencv_world454.lib