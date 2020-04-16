project(myapp)
cmake_minimum_required(VERSION 3.1)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup(TARGETS)

add_executable(myapp testcurl.c)
target_link_libraries(myapp CONAN_PKG::libcurl)
