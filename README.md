# Laba3_report-TiMP
### Задание №1
```
touch CMakeLists.txt
nano CMakeLists.txt


cmake_minimum_required(VERSION 3.16.3)
project(formatter)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(formatter STATIC formatter.cpp formatter.h)


cmake -H. -Bbuild1
cmake --build build1

```
### Задание №2
```
touch CMakeLists.txt
nano CMakeLists.txt


cmake_minimum_required(VERSION 3.16.3)
project(formatter_ex)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(formatter_ex STATIC formatter_ex.cpp formatter_ex.h)

include_directories(~/lab03/formatter_ex_lib/../formatter_lib)
target_link_libraries(formatter_ex formatter)

cmake -H. -Bbuild2
cmake --build build2

```
### Задание №3
Part 1
```
touch CMakeLists.txt
nano CMakeLists.txt

cmake_minimum_required(VERSION 3.16.3)
project(hello_world)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(hello_world hello_world.cpp)

include_directories(~/lab03/hello_world_application/../formatter_ex_lib)
target_link_libraries(hello_world formatter_ex)

```
Part 2
```
touch CMakeLists.txt
nano CMakeLists.txt

cmake_minimum_required(VERSION 3.16.3)
project(solver)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(solver STATIC solver.cpp solver.h)

```
Part 3
```
touch CMakeLists.txt
nano CMakeLists.txt

cmake_minimum_required(VERSION 3.16.3)
project(equation)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(equation equation.cpp)

include_directories(~/lab03/solver_application/../formatter_ex_lib)
include_directories(~/lab03/solver_application/../solver_lib)

target_link_libraries(equation formatter_ex)
target_link_libraries(equation solver)

```
