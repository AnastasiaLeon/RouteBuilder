cmake_minimum_required(VERSION 3.10)

project(RouteBuilder)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(cpr REQUIRED)
find_package(nlohmann_json REQUIRED)

add_executable(RouteBuilder main.cpp YandexScheduleAPI.cpp CacheManager.cpp)

target_link_libraries(RouteBuilder PRIVATE cpr::cpr nlohmann_json::nlohmann_json)