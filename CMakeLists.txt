cmake_minimum_required(VERSION 3.30.0)
project(planning
    VERSION 0.0.1
    DESCRIPTION "a demo of cmake planning"
    HOMEPAGE_URL "https://github.com/foolfriendly/cmake_planning_demo"
    LANGUAGES CXX
)
set(CMAKE_CXX_STANDARD 17)

#变量设置，可传递到子目录,将相应的文件位置赋给Process_Dir等
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)
set(Process_Dir ${CMAKE_SOURCE_DIR}/src/process)
set(PNC_Map_Dir ${CMAKE_SOURCE_DIR}/src/pnc_map)

#添加子目录,找子目录中的CMakeLists
add_subdirectory(src)