cmake_minimum_required(VERSION 3.5)
project(rc_test)

include_directories(${CMAKE_BINARY_DIR})

include_directories("./")
include_directories("../robot/include")
include_directories("../common/include/")
include_directories("../third-party/yaml-cpp/include")
include_directories("../third-party/vectornav/include")
include_directories("../third-party/vectornav/include/vn")
include_directories("../third-party/lord_imu/Include")

include_directories("../lcm-types/cpp")

file(GLOB sources "*.cpp")

add_executable(rc_test ${sources})

target_link_libraries(rc_test biomimetics pthread lcm robot)
if(CMAKE_SYSTEM_NAME MATCHES Linux)
    target_link_libraries(rc_test libvnc rt)
endif()
