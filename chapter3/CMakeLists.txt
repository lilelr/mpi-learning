cmake_minimum_required(VERSION 3.8)

set(CMAKE_CXX_STANDARD 11)
set(chapter3_dir /home/lilelr/CLionProjects/mpi-learning/chapter3)
set(CHAP3_SOURCE_FILES ${chapter3_dir}/mpi_trap1.cpp)
add_executable(chapter3 ${CHAP3_SOURCE_FILES})
target_link_libraries(chapter3 ${MPI_C_LIBRARIES})

set(CHAP3_mpi_vector_add ${chapter3_dir}/mpi_vector_add.cpp)
add_executable(CHAP3_mpi_vector_add ${CHAP3_mpi_vector_add})
target_link_libraries(CHAP3_mpi_vector_add ${MPI_C_LIBRARIES})


set(CHAP3_mpi_odd_even ${chapter3_dir}/mpi_odd_even.cpp)
add_executable(CHAP3_mpi_odd_even ${CHAP3_mpi_odd_even})
target_link_libraries(CHAP3_mpi_odd_even ${MPI_C_LIBRARIES})