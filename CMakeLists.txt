cmake_minimum_required(VERSION 3.16.0)
set(EXTRA_COMPONENT_DIRS .)

include($ENV{IDF_PATH}/tools/cmake/project.cmake)

# Имя проекта
project(tesserae-reterminal-e1002)

# Регистрация компонента с исходниками
idf_component_register(
    SRCS
        main/main.c
        main/epd_driver.c
        main/heartbeat.c
        main/image_decoder.c
        main/image_fetcher.c
        main/mqtt_config.c
        main/mqtt_handler.c
        main/pmic.c
        main/provisioning.c
        main/splash.c
        main/wifi_manager.c
    INCLUDE_DIRS
        "main"
        "include"
    EMBED_FILES
        "assets/splash_logo.bin"
        "assets/splash_portal.bin"
    REQUIRES
        driver
        esp_driver_i2c
        esp_driver_usb_serial_jtag
        esp_event
        esp_http_client
        esp_http_server
        esp_netif
        esp_wifi
        esp-tls
        mqtt
        nvs_flash
        mbedtls
        lwip
        mdns
)
