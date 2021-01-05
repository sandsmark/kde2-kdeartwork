cmake_minimum_required(VERSION 3.0)
project(kde2-kdeartwork)
set(KDEDIR ${CMAKE_INSTALL_PREFIX})
find_package(kdelibs2 REQUIRED)
find_package(DCOP REQUIRED)
find_package(kdecore REQUIRED)
find_package(kdeui REQUIRED)

add_subdirectory(styles)
add_subdirectory(Themes)

install(
    FILES
        sounds/KDE_Logout_new.wav
        sounds/KDE_Startup_new.wav
    DESTINATION ${KDE2_SOUNDDIR}
    )

install(
    FILES
        wallpapers/kdemagic.jpg
    DESTINATION ${KDE2_WALLPAPERDIR}
    )

