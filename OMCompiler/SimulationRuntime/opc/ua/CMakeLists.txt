cmake_minimum_required(VERSION 3.14)
project(omopcua)


add_library(omopcua SHARED)
target_sources(omopcua PRIVATE omc_opc_ua.c)

target_link_libraries(omopcua PRIVATE omc::3rd::opcua)
target_include_directories(omopcua PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../../c/)

install(TARGETS omopcua)
