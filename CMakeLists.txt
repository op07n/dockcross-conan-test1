project(dockcross-conan-test1)
cmake_minimum_required(VERSION 3.1)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup(TARGETS)

add_executable(dockcross-conan-test1 testcurl.c)
target_link_libraries(dockcross-conan-test1 CONAN_PKG::libcurl)
