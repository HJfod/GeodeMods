cmake_minimum_required(VERSION 3.22)

project(ninXout_mods)

if (NOT DEFINED ENV{GEODE_SDK})
    message(FATAL_ERROR "Unable to find Geode SDK! Please define GEODE_SDK environment variable to point to Geode")
else()
    message(STATUS "Found Geode: $ENV{GEODE_SDK}")
endif()

set(GEODE_LINK_NIGHTLY On)
add_subdirectory($ENV{GEODE_SDK} $ENV{GEODE_SDK}/build)

add_subdirectory(FPSRipoff)
add_subdirectory(NewBestPause)
add_subdirectory(NoclipAccuracy)
add_subdirectory(NoMirrorFlip)
add_subdirectory(NoWaveRipoff)
add_subdirectory(NoWaveStreak)
add_subdirectory(PracticeMusicHack)
add_subdirectory(ReallyAccurate)
add_subdirectory(SafeProgress)
add_subdirectory(SmartCheckpoints)
add_subdirectory(UltraRainbow)
