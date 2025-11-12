cmake_minimum_required(VERSION 3.20)

project(FastWatchPlus LANGUAGES C CXX)

# Set default to Release if not provided
if(NOT CMAKE_BUILD_TYPE)
  set(CMAKE_BUILD_TYPE Release CACHE STRING "Build type" FORCE)
endif()

# Enable C++17 for passes/tools
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Let users point LLVM via -DLLVM_DIR=/path/to/lib/cmake/llvm
# (needed for the out-of-tree pass build)
add_subdirectory(compiler/llvm-passes)
