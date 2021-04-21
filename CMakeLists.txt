cmake_minimum_required(VERSION 3.19)
set(CMAKE_CXX_STANDARD 11)

project(aquila-cpp-boilerplate)

set(AQUILA_ROOT "D:/Code Projects/Cpp Libraries/aquila")

link_directories(
  ${AQUILA_ROOT}/build
)

add_executable(${PROJECT_NAME} main.cpp ${AQUILA_ROOT}/lib/ooura/fft4g.c)

target_include_directories(${PROJECT_NAME}
    PRIVATE
      ${AQUILA_ROOT})

target_link_libraries(${PROJECT_NAME}
  PRIVATE 
    aquila)
