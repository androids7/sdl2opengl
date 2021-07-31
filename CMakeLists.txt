cmake_minimum_required (VERSION 3.13)
project(SDL2opengl)



set(module_name "opengl")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "build")
# 查找指定目录下的所有源文件，然后将结果存进指定变量名
aux_source_directory(. SRC_LIST)

add_executable(${module_name} ${SRC_LIST})

target_link_libraries(${module_name}  mingw32 SDL2main SDL2_ttf   SDL2  SDL2_image SDL2_net SDL2_mixer freetype png z )