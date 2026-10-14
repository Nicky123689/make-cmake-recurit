cmake_minimum_required(VERSION 3.16)

project(calculator LANGUAGES C)

# 生成可执行文件 calculator（源文件都在 src/ 下）
add_executable(calculator src/main.c src/calculator.c)

# 让 calculator 这个目标能找到 include/ 里的头文件
target_include_directories(calculator PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include)
