# C/C++工程模板   

一个基于Windows系统，VScode+Mingw+Cmake构建的工程模板   

## 环境搭建   

- VScode下载 https://code.visualstudio.com/   
    >下载并安装后，按照自己需要下载插件   
    C/C++
    CMake
    ...
- MinGW下载 https://sourceforge.net/projects/mingw-w64/   
    >1   
- CMake下载 https://cmake.org/download/   
    >进入下载页面选择Binary distributions下的 *windows x64 installer* 或者 *windows x64 zip*   
    installer类似于安装包   
    zip需要配置系统环境变量(建议)   
- 下载完成后，打开任意终端输入以下命令行，有版本输出，即环境搭建完成
    ```shell
    cmake --version
    gcc --version
    g++ --version
    ``` 


## 如何进行编译调试   

因为采用的是MinGW编译器，所以编译的时候要指定mingw的makefile生成器   

```shell
mkdir build
cd build
cmake -G "MinGW Makefiles" ..
cd ..
cmake --build build
```

