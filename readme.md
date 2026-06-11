# C/C++工程模板   

一个基于Windows系统，VScode+Mingw+Cmake构建的工程模板   

## 环境搭建   

- VScode下载 https://code.visualstudio.com/   
    >下载并安装后，按照自己需要下载插件   
    C/C++
    CMake
    ...
- MinGW下载 https://github.com/niXman/mingw-builds-binaries/releases   
    >选择x86_64-16.1.0-release-win32-seh-ucrt-rt_v14-rev1.7z   
    当前最新版本为16.1.0   
    这是已经编译好的，需要配置系统环境变量
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
--------------------------------------------------或者
cmake -S . -B build -G "MinGW Makefiles"
cmake --build build
```
调试点击F5或者Ctrl+Shift+B即可进入调试，但是进入调试前需要修改.vscode文件夹下的文件，主要是文件中的编译器以及调试器路径   

