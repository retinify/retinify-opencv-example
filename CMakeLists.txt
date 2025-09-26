cmake_minimum_required(VERSION 3.11)

set(CMAKE_BUILD_TYPE Release)
project(retinify-opencv-example LANGUAGES CXX)

add_executable(retinify-opencv-example main.cpp)

find_package(retinify REQUIRED)
find_package(OpenCV REQUIRED)

target_link_libraries(${PROJECT_NAME} 
    PRIVATE
        retinify::retinify ${OpenCV_LIBS}
)