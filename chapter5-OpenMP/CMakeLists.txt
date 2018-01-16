cmake_minimum_required(VERSION 3.8)

set(CMAKE_CXX_STANDARD 11)
find_package(OpenMP)
if (OPENMP_FOUND)
    set (CMAKE_C_FLAGS "${CMAKE_C_FLAGS} ${OpenMP_C_FLAGS}")
    set (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${OpenMP_CXX_FLAGS}")
endif()
set(THREADS_PREFER_PTHREAD_FLAG ON)
find_package(Threads REQUIRED)

set(chapter5_dir /home/lilelr/CLionProjects/mpi-learning/chapter5-OpenMP/)


set(CHAP5-OpenMP ${chapter5_dir}/omp_hello.c)
add_executable(CHAP5-OpenMP ${CHAP5-OpenMP})
target_link_libraries(CHAP5-OpenMP Threads::Threads)

