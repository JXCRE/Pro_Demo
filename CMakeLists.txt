# 首先指定最小的CMake版本，建议使用3.15或更高版本
cmake_minimum_required(VERSION 3.15)

# 定义项目名称、版本、使用的编程语言和项目描述
project(pro_demo
        VERSION 0.0.1
        LANGUAGES C CXX
        DESCRIPTION "A demo project")

# 设置变量
set(common_path ${CMAKE_CURRENT_SOURCE_DIR}/include)

# 批量添加c文件
file(GLOB SRC_FILES "src/*.c")

# 生成可执行文件，使用add_executable命令，目标exe和其源文件
add_executable(${PROJECT_NAME} ${SRC_FILES})
# 生成库文件，可以使用add_library命令
# add_library(<target> <source_files>...)
# 链接库文件，可以使用target_link_libraries命令
# target_link_libraries(<target> <libraries>...)

# 添加头文件搜索路径
include_directories(
        ${common_path}
)
