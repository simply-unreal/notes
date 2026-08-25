# Notes

## Clang Setup
run
```bash
mkdir build
mkdir src
mkdir include
touch src/main.cpp
touch CMakeLists.txt
touch run.sh
```

then in `CMakeLists.txt` add this
```cpp
cmake_minimum_required(VERSION 3.20)

project(MyProject LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_executable([project_name]
    src/main.cpp
)
```

then in `run.sh` add this
```bash
cmake --build build && clear && ./build/[project_name]
```

then run
```bash
cmake -S . -B build -DCMAKE_CXX_COMPILER=clang++
```

then to run the program with CMake just run
```bash
./run.sh
```
or you can get the script run extension on VSCode to run `run.sh` with the click of a button
