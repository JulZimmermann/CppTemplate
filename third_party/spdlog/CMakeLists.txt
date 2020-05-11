add_library(spdlog STATIC   src/spdlog.cpp
                            src/stdout_sinks.cpp
                            src/fmt.cpp
                            src/color_sinks.cpp
                            src/file_sinks.cpp
                            src/async.cpp)

target_compile_definitions(spdlog PUBLIC SPDLOG_COMPILED_LIB)
target_link_libraries(spdlog PUBLIC Threads::Threads)
target_include_directories(spdlog PUBLIC include)

if (TARGET fmt::fmt)
    target_compile_definitions(spdlog PUBLIC SPDLOG_FMT_EXTERNAL)
    target_link_libraries(spdlog PUBLIC fmt::fmt)
endif()

add_library(spdlog::spdlog ALIAS spdlog)