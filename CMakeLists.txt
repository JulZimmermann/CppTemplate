cmake_minimum_required(VERSION 3.16)

project(Template)

find_package(Threads REQUIRED)

add_subdirectory(third_party/json)
add_subdirectory(third_party/range-v3)
add_subdirectory(third_party/fmt)
add_subdirectory(third_party/asio-1.12.2)
add_subdirectory(third_party/date)
add_subdirectory(third_party/googletest)
add_subdirectory(third_party/jthread)
add_subdirectory(third_party/spdlog)

add_subdirectory(main)