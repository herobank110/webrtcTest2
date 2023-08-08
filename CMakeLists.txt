cmake_minimum_required(VERSION 3.14 FATAL_ERROR)

project(WebrtcTest2)

set(ENV OPENSSL_ROOT_DIR "C:/Program Files/OpenSSL-Win64")
set(PCAP_LIBRARY "C:/Program Files (x86)/Win10Pcap/x64")
include(./cmake/CPM.cmake)
# CPMAddPackage("gh:the-tcpdump-group/libpcap#libpcap-1.10.4")
CPMAddPackage("gh:paullouisageneau/libdatachannel@0.18.5")

add_executable(WebrtcTest2 main.cpp)
target_compile_features(WebrtcTest2 PRIVATE cxx_std_20)
target_link_libraries(WebrtcTest2 libdatachannel)
