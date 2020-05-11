add_library(range-v3 INTERFACE)

target_include_directories(range-v3 INTERFACE include)

add_library(ericniebler::range-v3 ALIAS range-v3)

