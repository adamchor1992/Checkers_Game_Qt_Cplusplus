cmake_minimum_required(VERSION 3.5)

project(CheckersTest LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(GOOGLE_TEST_DIR ${CMAKE_CURRENT_SOURCE_DIR}/google_test)

include_directories(${GOOGLE_TEST_DIR}/include)
add_executable(CheckersTest main.cpp)

target_link_libraries(CheckersTest ${GOOGLE_TEST_DIR}/lib/libgtestd.a)
target_link_libraries(CheckersTest ${GOOGLE_TEST_DIR}/lib/libgmockd.a)
target_link_libraries(CheckersTest ${GOOGLE_TEST_DIR}/lib/libgtest_maind.a)
target_link_libraries(CheckersTest ${GOOGLE_TEST_DIR}/lib/libgmock_maind.a)
