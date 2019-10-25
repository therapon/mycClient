cmake_minimum_required(VERSION 3.14)
project(mycClient
        VERSION 1.0.0
        LANGUAGES C CXX)

# add_subdirectory(mycLib/src)

find_package(MyCLib REQUIRED)

add_executable(myapp myapp.c)
target_link_libraries(myapp
        PRIVATE
        MyCLib::myclib)