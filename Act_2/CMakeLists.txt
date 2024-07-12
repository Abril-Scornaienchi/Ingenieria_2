# Para ejecutar cmake, nos movemos dentro de un directorio build previamente creado y 
# ejecutamos en una terminal el comando: cmake ..
# luego ejecutamos el comando make

# Establecer la mínima versión requerida de cmake
cmake_minimum_required(VERSION 3.8)

# Establecer versión de C++
set (CMAKE_CXX_STANDARD 17)

# Establecer los compiladores de C y C++
set(CMAKE_C_COMPILER "gcc")
set(CMAKE_CXX_COMPILER "g++")

# Nombre del proyecto Cmake
project(MyLibraryProject)

# Indicar el nombre del directorio que debe tener en cuenta
add_subdirectory(my_library)

# añadir nombre del ejecutable y el archivo a compilar
add_executable(main main.cpp)

# Inidcar que el ejecutable main.exe, también necesitará la biblioteca "my_library"
target_link_libraries(main
    my_library)