cmake_minimum_required(VERSION 3.10)
project(CG)

set(CMAKE_CXX_STANDARD 17)

add_subdirectory(external/glfw)

include_directories(
        external/glad/include
        external/glm
        external/glfw/include
)

add_executable(CompGraph
        main.cpp
        external/glad/src/glad.c
)

if(APPLE)
    target_link_libraries(CompGraph glfw "-framework OpenGL" "-framework Cocoa" "-framework IOKit" "-framework CoreVideo")
else()
    target_link_libraries(CompGraph glfw)
endif()