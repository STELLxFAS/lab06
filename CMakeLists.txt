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
set(CPACK_PACKAGE_VENDOR "STELLxFAS")
set(CPACK_PACKAGE_CONTACT "egorkarbazov@gmail.com")
set(CPACK_DEBIAN_PACKAGE_MAINTAINER "STELLxFAS")

set(CPACK_GENERATOR "TGZ;ZIP;DEB;RPM")

set(CPACK_DEBIAN_PACKAGE_DEPENDS "libc6")
set(CPACK_DEBIAN_PACKAGE_SECTION "utils")
set(CPACK_DEBIAN_PACKAGE_ARCHITECTURE "amd64")

set(CPACK_RPM_PACKAGE_LICENSE "MIT")
set(CPACK_RPM_PACKAGE_GROUP "Applications/Utilities")

include(CPack)
