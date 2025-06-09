# TODO 1: Set the minimum required version of CMake to be 3.10
cmake_minimum_required(VERSION 3.10)

# TODO 2: Create a project named Tutorial
project(Tutorial)

# TODO 7: Set the project version number as 1.0 in the above project command

# TODO 6: Set the variable CMAKE_CXX_STANDARD to 11
#         and the variable CMAKE_CXX_STANDARD_REQUIRED to True
set(CMAKE_CXX_STANDARD 11)
    # CMAKE_CXX_STANDARD:
    #   Default value for CXX_STANDARD target property
    # CXX_STANDARD:
    #   The C++ standard whose features are requested to build this target
set(CMAKE_CXX_STANDARD_REQUIRED ON)
    # 如果设置为 `ON`，那么 CMake 会要求编译器必须支持
    # `CMAKE_CXX_STANDARD` 中设置的 C++ 版本，否则会配置失败
    #
    # CMAKE_CXX_STANDARD_REQUIRED:
    #   Default value for CXX_STANDARD_REQUIRED target property
    # CXX_STANDARD_REQUIRED:
    #   Boolean describing whether the value of CXX_STANDARD is a requirement.

# TODO 8: Use configure_file to configure and copy TutorialConfig.h.in to
#         TutorialConfig.h

# TODO 3: Add an executable called Tutorial to the project
# Hint: Be sure to specify the source file as tutorial.cxx
add_executable(Tutorial tutorial.cxx)

# TODO 9: Use target_include_directories to include ${PROJECT_BINARY_DIR}
