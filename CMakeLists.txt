cmake_minimum_required(VERSION 3.11)

set(CMAKE_BUILD_TYPE Release)
set(CMAKE_CXX_STANDARD 20)
project(retinify-opencv-example)

add_executable(retinify-opencv-example main.cpp)

find_package(retinify REQUIRED)
find_package(OpenCV REQUIRED)

target_link_libraries(${PROJECT_NAME} 
    PRIVATE
        retinify ${OpenCV_LIBS}
)