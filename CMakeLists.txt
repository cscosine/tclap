cmake_minimum_required(VERSION 3.31)
project(tclapSol VERSION 1.0.0 LANGUAGES CXX)

# add the csCMake system
include(csCMake)

cs_initialize_project(NAMESPACE tclap CXX_STANDARD 17
    # add the default configurations supported by this project, only Release
    DEFAULT_CONFIG Release
)

# add libs, executables, etc
add_subdirectory(tclap)
add_subdirectory(examples)
