# Target:   example_lib
# Type:     Library
file(GLOB SOURCE *.cpp)
add_library(example_lib SHARED ${SOURCE})
set_target_properties(example_lib PROPERTIES
    "OUTPUT_NAME" "example"
    "INCLUDE_DIRECTORIES" "${CMAKE_CURRENT_SOURCE_DIR}/include"
)
install(TARGETS example_lib EXPORT example DESTINATION ${CMAKE_SOURCE_DIR}/lib)
export(TARGETS example_lib FILE ${CMAKE_BINARY_DIR}/example-config.cmake)
