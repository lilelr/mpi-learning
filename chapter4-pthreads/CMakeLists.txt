cmake_minimum_required(VERSION 3.8)

set(CMAKE_CXX_STANDARD 11)

set(THREADS_PREFER_PTHREAD_FLAG ON)
find_package(Threads REQUIRED)

set(chapter4_dir /home/lilelr/CLionProjects/mpi-learning/chapter4-pthreads)


set(CHAP4_Pth_hello ${chapter4_dir}/pth_hello.c)
add_executable(CHAP4_Pth_hello ${CHAP4_Pth_hello})
target_link_libraries(CHAP4_Pth_hello Threads::Threads)

