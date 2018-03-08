cmake_minimum_required(VERSION 3.1)
project(game.libretro.virtualjaguar)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-virtualjaguar REQUIRED)

set(VIRTUALJAGUAR_CUSTOM_BINARY ${VIRTUALJAGUAR_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} VIRTUALJAGUAR "")

include(CPack)
