cmake_minimum_required(VERSION 3.0.0)
project(is_prime VERSION 0.1.0)

aux_source_directory(. ROOT_SRC)

add_executable(
    ${PROJECT_NAME}
    ${ROOT_SRC}
)

target_link_libraries(
    ${PROJECT_NAME} 
    m
)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
