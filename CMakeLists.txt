cmake_minimum_required(VERSION 3.15)

project(pro_demo
        AUtor "JXC"
        VERSION 0.0.1
        LANGUAGES C CXX
        PROJECT_DESCRIPTION "A demo project")


# 添加可执行文件
add_executable(${PROJECT_NAME} ${SRC_FILES})

