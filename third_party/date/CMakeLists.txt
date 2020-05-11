add_library(date INTERFACE)

target_include_directories(date INTERFACE include)

add_library(date::date ALIAS date)