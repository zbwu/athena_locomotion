add_subdirectory(Goldfarb_Optimizer EXCLUDE_FROM_ALL)
#add_subdirectory(osqp EXCLUDE_FROM_ALL)
#add_subdirectory(JCQP EXCLUDE_FROM_ALL)
add_subdirectory(qpOASES EXCLUDE_FROM_ALL)
add_subdirectory(yaml-cpp EXCLUDE_FROM_ALL)

if (LCM_MSG)
# add_subdirectory(lcm EXCLUDE_FROM_ALL)
endif()

if (INI_FILE)
# add_subdirectory(inih)
endif()

if(CMAKE_SYSTEM_NAME MATCHES Linux)
# add_subdirectory(vectornav)
# add_subdirectory(lord_imu)
# add_subdirectory(SOEM)
endif()
