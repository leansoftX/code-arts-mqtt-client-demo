cmake_minimum_required(VERSION 3.17)
find_package(eclipse-paho-mqtt-c 1.3.9 REQUIRED)
project(mqtt_c C)
include_directories(/usr/local/include)
link_directories(/usr/local/lib)
set(CMAKE_C_STANDARD 99)

add_executable(mqtt_tls_c main_tls.c)
find_library(PAHO_MQTT3C_LIB paho-mqtt3cs PATHS /usr/local/lib)
target_link_libraries(mqtt_tls_c ${PAHO_MQTT3C_LIB})

add_executable(emqx_file_transfer emqx_file_transfer.c)
find_library(PAHO_MQTT3C_LIB paho-mqtt3c PATHS /usr/local/lib)
target_link_libraries(emqx_file_transfer ${PAHO_MQTT3C_LIB})

add_executable(mqtt_c main.c)
find_library(PAHO_MQTT3C_LIB paho-mqtt3c PATHS /usr/local/lib)
target_link_libraries(mqtt_c ${PAHO_MQTT3C_LIB})

