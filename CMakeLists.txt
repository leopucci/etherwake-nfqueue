cmake_minimum_required(VERSION 3.7)
project(etherwake-nfqueue C)

set(CMAKE_C_STANDARD 99)

add_executable(etherwake-nfqueue
        ether-wake.c
        nfqueue.c nfqueue.h)

target_link_libraries(etherwake-nfqueue netfilter_queue)

install(TARGETS etherwake-nfqueue DESTINATION bin)
