# CMake 最低版本号要求
cmake_minimum_required (VERSION 2.8)

# 项目信息
project (Demo)

# 添加头文件目录
include_directories(json)


# 查找当前目录下的所有源文件
# 并将名称保存到 DIR_SRCS 变量
aux_source_directory(. DIR_SRCS)

# 添加库
# add_library(lib_json
#        cmd.cpp
#        global.cpp
#        md5.cpp
# )



# 添加需要链接的库文件目录
link_directories(lib)


# link_libraries(jsoncpp)

# 添加 json 子目录
# add_subdirectory(json)

# 指定生成目标
add_executable(Demo ${DIR_SRCS})

# 添加链接库
target_link_libraries(Demo ${lib})
