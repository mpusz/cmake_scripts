# cmake_scripts

CMake scripts shared among other repositories. It provides tools and wrappers useful in every project.

It also provides different patches and bugfixes for other projects when they are not working properly.


Tools and utilities:
- `conan_init()` - includes cmake files generated by Conan Package Manger if present and runs `conan_basic_setup(TARGETS)`
- `configure_and_install(configure_in_file_path, version_compare_rules)` - creates CMake package version and config files
     and istaslls them together with `${CMAKE_PROJECT_NAME}Targets` ``EXPORT` target.

Current list of patches:
- `set(CMAKE_CXX_STANDARD 17)` - fix for CMake not setting `/std:c++latest` for VS 2017
- `find_package(GTest)` - fix for compilation under VS 2017 with C++17 enabled
