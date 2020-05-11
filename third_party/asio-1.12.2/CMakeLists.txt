if(NOT TARGET asio)
    add_library(asio INTERFACE)
    target_include_directories(asio INTERFACE include)
    target_compile_definitions(asio INTERFACE ASIO_STANDALONE)

    if(WIN32)
        target_link_libraries(asio INTERFACE ws2_32 wsock32)
    endif()

    add_library(asio::asio ALIAS asio)

endif()
