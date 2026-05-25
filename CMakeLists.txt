cmake_minimum_required(VERSION 3.10)
project(FormatterInc VERSION 1.0.0 LANGUAGES CXX)

add_subdirectory(formatter_lib)
add_subdirectory(formatter_ex_lib)
add_subdirectory(solver_lib)

add_subdirectory(hello_world_application)
add_subdirectory(solver_application)

set(CPACK_PACKAGE_NAME "Solver")
set(CPACK_PACKAGE_VERSION "1.0.0")
set(CPACK_PACKAGE_DESCRIPTION_SUMMARY "Quadratic Equation Solver")
set(CPACK_PACKAGE_VENDOR "YourName")

set(CPACK_GENERATOR "TGZ;ZIP;DEB;RPM") 

include(CPack)
