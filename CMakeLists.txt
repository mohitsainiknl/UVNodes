cmake_minimum_required(VERSION 3.18)


project(UVNodes VERSION 1.0 LANGUAGES CXX)


set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)


find_package(Qt6 REQUIRED COMPONENTS Core Gui Widgets OpenGL)


qt_standard_project_setup()


include(FetchContent)
FetchContent_Declare(QtNodes
    GIT_REPOSITORY "https://github.com/paceholder/nodeeditor"
    GIT_TAG "630999276b5f1e63060ee85492d8f32090ebf87d"
)
FetchContent_MakeAvailable(QtNodes)


add_subdirectory(src)


# set_target_properties(${PROJECT_NAME} PROPERTIES
#     WIN32_EXECUTABLE TRUE
#     MACOSX_BUNDLE TRUE
# )




