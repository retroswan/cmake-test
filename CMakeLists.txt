cmake_minimum_required(VERSION 3.10)

project(HelloWorldProj VERSION 1.0)
add_executable(HelloWorldProj src/main.c)

target_link_libraries(HelloWorldProj PUBLIC HelloWorld)
target_include_directories(HelloWorldProj PUBLIC
"${PROJECT_BINARY_DIR}"
"${PROJECT_SOURCE_DIR}/HelloWorld"
)
add_library(HelloWorld SHARED src/HelloWorld/hello.c)
