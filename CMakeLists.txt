cmake_minimum_required(VERSION 3.28)
project(sfmlTry1)

set(CMAKE_CXX_STANDARD 17)

add_executable(sfmlTry1 main.cpp
        Player.cpp
        Animation.cpp
        DrawText.cpp
        Enemy.cpp
        EnemyManager.cpp
        Ufo.cpp
        Headers/DrawText.hpp
        Headers/Animation.hpp
        Headers/Enemy.hpp
        Headers/EnemyManager.hpp
        Headers/Global.hpp
        Headers/Player.hpp
        Headers/Ufo.hpp
)

set(SFML_STATIC_LIBRARIES TRUE)
set(SFML_DIR C:/SFML/SFML-2.6.1/lib/cmake/SFML)
find_package(SFML COMPONENTS system window graphics audio network REQUIRED)

include_directories(C:/SFML/SFML-2.6.1/include/SFML)
target_link_libraries(sfmlTry1 sfml-system sfml-window sfml-graphics sfml-audio)