# SPDX-License-Identifier: Apache-2.0

wasmedge_add_library(wasmedgeSystem
  allocator.cpp
  fault.cpp
  mmap.cpp
  path.cpp
)

target_include_directories(wasmedgeSystem
  PUBLIC
  ${CMAKE_CURRENT_BINARY_DIR}
)

target_link_libraries(wasmedgeSystem
  PUBLIC
  wasmedgeCommon
  Boost::boost
)
