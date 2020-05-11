add_library(jthread INTERFACE)

target_include_directories(jthread INTERFACE include)

add_library(josuttis::jthread ALIAS jthread)