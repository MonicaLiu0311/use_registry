cmake_minimum_required(VERSION 3.18)

set(CMAKE_TOOLCHAIN_FILE "E:/vcpkg02/scripts/buildsystems/vcpkg.cmake")

project(test CXX)
add_executable(main main.cpp)

find_package(beicode CONFIG REQUIRED)
target_link_libraries(main PRIVATE beicode::beicode)

find_package(beison CONFIG REQUIRED)
target_link_libraries(main PRIVATE beison::beison)

find_package(fmt CONFIG REQUIRED)
target_link_libraries(main PRIVATE fmt::fmt)

# find_path(JWT_CPP_INCLUDE_DIRS "jwt-cpp/base.h")
# target_include_directories(main PRIVATE ${JWT_CPP_INCLUDE_DIRS})

# find_package(jsoncpp CONFIG REQUIRED)
# target_link_libraries(main PRIVATE JsonCpp::JsonCpp)

# find_package(jsoncons CONFIG REQUIRED)
# target_link_libraries(main PRIVATE jsoncons)

# find_package(json-dto CONFIG REQUIRED)
# target_link_libraries(main PRIVATE json-dto::json-dto)

