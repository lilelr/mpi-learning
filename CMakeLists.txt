cmake_minimum_required(VERSION 3.8)
project(mpi_learning)

set(CMAKE_CXX_STANDARD 11)
find_package(MPI) #make it REQUIRED, if you want
include_directories(SYSTEM ${MPI_INCLUDE_PATH})

set(SOURCE_FILES main.cpp helllo_world.cpp)
add_executable(mpi_learning ${SOURCE_FILES})
target_link_libraries(mpi_learning ${MPI_C_LIBRARIES})