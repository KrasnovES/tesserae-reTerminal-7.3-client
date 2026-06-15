cmake_minimum_required(VERSION 3.16)

# Указываем, что компоненты ищем в папке src (а не main)
set(EXTRA_COMPONENT_DIRS src)

include($ENV{IDF_PATH}/tools/cmake/project.cmake)

project(tesserae-reterminal-e1002)
