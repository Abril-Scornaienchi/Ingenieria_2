# Establecer que se trata de una biblioteca compartida
add_library(my_library SHARED
    my_library.h
    my_library.cpp)

# Inidcar las rutas en las que se deben buscar las librerías
target_include_directories(my_library PUBLIC
    ${CMAKE_CURRENT_LIST_DIR})


