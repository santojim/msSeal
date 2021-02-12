cmake_minimum_required(VERSION 3.10)
project(SEALDemo VERSION 1.0)
add_executable(examples examples.cpp)
target_sources(examples
  PRIVATE
  ${CMAKE_CURRENT_LIST_DIR}/4_ckks_basics_modified.cpp
    )
set_target_properties(examples PROPERTIES
    CXX_STANDARD 17
    CXX_STANDARD_REQUIRED ON
    CXX_EXTENSIONS ON
  )

find_package(SEAL)
target_link_libraries(examples seal-3.6)
