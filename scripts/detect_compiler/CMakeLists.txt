cmake_minimum_required(VERSION 3.10)
project(detect_compiler NONE)

set(CMAKE_C_COMPILER_WORKS 1)
set(CMAKE_C_COMPILER_ID_RUN 1)
set(CMAKE_C_COMPILER_FORCED 1)
set(CMAKE_CXX_COMPILER_WORKS 1)
set(CMAKE_CXX_COMPILER_ID_RUN 1)
set(CMAKE_CXX_COMPILER_FORCED 1)

enable_language(C)
enable_language(CXX)

file(SHA1 "${CMAKE_CXX_COMPILER}" CXX_HASH)
file(SHA1 "${CMAKE_C_COMPILER}" C_HASH)
string(SHA1 COMPILER_HASH "${C_HASH}${CXX_HASH}")

message("#COMPILER_HASH#${COMPILER_HASH}")
