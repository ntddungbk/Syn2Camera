cmake_minimum_required (VERSION 2.8.12)
project (ConfigIPCAM)
find_package(OpenCV REQUIRED)

include_directories(include)
add_definitions("-std=c++11")


add_executable(config src/config.cpp)
target_link_libraries(config ${OpenCV_LIBS} curl pthread)

add_executable(showCam src/showCam.cpp)
target_link_libraries(showCam ${OpenCV_LIBS} curl pthread)

add_executable(manConf src/man_config.cpp	)
target_link_libraries(manConf curl ${OpenCV_LIBS})

