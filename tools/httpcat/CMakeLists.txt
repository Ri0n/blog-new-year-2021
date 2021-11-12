project(rhhp_httpcat)

find_package(Boost COMPONENTS program_options REQUIRED)

set(BIN2_TARGET httpcat)
add_executable(${BIN2_TARGET} main.cpp)
target_link_libraries(${BIN2_TARGET} rhhp Boost::program_options)

include(RhhpUtil)
rhhp_setup_compiler(${BIN2_TARGET})
