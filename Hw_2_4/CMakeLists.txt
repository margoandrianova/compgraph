add_executable(Hw_2_4 main.cpp)

target_include_directories(Hw_2_4 PRIVATE ${COMMON_INCLUDES})

target_link_libraries(Hw_2_4 PRIVATE glfw glad_lib)

add_custom_command(TARGET Hw_2_4 POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_directory
        "${CMAKE_SOURCE_DIR}/assets"
        "$<TARGET_FILE_DIR:Hw_2_4>/assets"
)