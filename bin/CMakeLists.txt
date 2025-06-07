add_executable(${PROJECT_NAME} main.cpp ../lib/CacheManager.cpp ../lib/YandexScheduleAPI.cpp)

target_include_directories(${PROJECT_NAME} PUBLIC ${PROJECT_SOURCE_DIR})

target_link_libraries(${PROJECT_NAME} PRIVATE cpr::cpr nlohmann_json::nlohmann_json)