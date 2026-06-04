cmake_minimum_required(VERSION 3.20)
project(CG C CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_subdirectory(external/glfw)

add_library(glad_lib STATIC "${CMAKE_CURRENT_SOURCE_DIR}/external/glad/src/glad.c")
target_include_directories(glad_lib PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/external/glad/include")

set(COMMON_INCLUDES
        "${CMAKE_CURRENT_SOURCE_DIR}/external/glm"
        "${CMAKE_CURRENT_SOURCE_DIR}/external/glfw/include"
        "${CMAKE_CURRENT_SOURCE_DIR}/external/glad/include"
)

add_subdirectory(Hw_2_2)
add_subdirectory(Hw_2_3)
add_subdirectory(Hw_2_4)
add_subdirectory(Hw_2_5)