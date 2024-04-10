cmake_minimum_required(VERSION 3.5.0)
project(wasm-interpreter VERSION 0.1.0 LANGUAGES C CXX)

include(CTest)
enable_testing()
set(CXX_STANDARD_REQUIRED 17)

aux_source_directory(src sources)

add_executable(wasm-interpreter main.cpp ${sources}
        src/util.hpp
        src/util.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
