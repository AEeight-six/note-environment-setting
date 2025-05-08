E:\OpenCV_4.5.5/
├── opencv/             # 主仓库
├── opencv_contrib/     # 扩展模块
└── build/              # 编译输出目录

配置过程先把梯子开起来科学上网，以免有些文件下载失败

```
cmd打开

# 删除旧构建目录
rm -rf build
mkdir build && cd build

# 重新配置
cmake ../opencv -G "MinGW Makefiles" ^
    -DCMAKE_BUILD_TYPE=Release ^  #release版本
    -DBUILD_SHARED_LIBS=ON ^      #动态链接库

    #构建world将模块整合
    -DBUILD_opencv_world=ON ^     
    #添加扩展模块目录
    -DOPENCV_EXTRA_MODULES_PATH=../opencv_contrib/modules ^ 
     
    -DCPU_BASELINE=SSE3 ^    # 使用 SSE3 作为基础指令集
    
    # 分派到 SSE4/AVX/AVX2，跳过 AVX-512
    -DCPU_DISPATCH=SSE4,AVX,AVX2  

# 编译并安装
make -j4
make install
```