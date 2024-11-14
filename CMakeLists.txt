cmake_minimum_required(VERSION 3.12...3.27.4)

project(sdl3_cmake_project)

find_package(SDL3 CONFIG QUIET)

if(NOT SDL3_FOUND)
  message(STATUS "SDL3 not found. Building it from source.")
  include(FetchContent)
  FetchContent_Declare(
    SDL
    GIT_REPOSITORY https://github.com/libsdl-org/SDL
    GIT_TAG        "preview-3.1.6"
  )
  FetchContent_MakeAvailable(SDL)
else()
  find_package(SDL3 REQUIRED CONFIG REQUIRED COMPONENTS SDL3-shared)
endif()

add_executable(${PROJECT_NAME} WIN32 src/main.cpp)
target_link_libraries(${PROJECT_NAME} PRIVATE SDL3::SDL3)

install(TARGETS ${PROJECT_NAME} RUNTIME DESTINATION .)
include(CPack)
