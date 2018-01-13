cmake_minimum_required(VERSION 3.8)

set(CMAKE_CXX_STANDARD 11)
set(chapter3_dir /home/lilelr/CLionProjects/mpi-learning/chapter3)
set(CHAP3_SOURCE_FILES ${chapter3_dir}/mpi_trap1.cpp)
add_executable(chapter3 ${CHAP3_SOURCE_FILES})
target_link_libraries(chapter3 ${MPI_C_LIBRARIES})