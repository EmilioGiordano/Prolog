13. Se tiene la siguiente base de datos con ciudades vecinas y las rutas que las conectan:
conectadas(arrecifes, san_antonio_de_areco, ruta_8).
conectadas(san_antonio_de_areco, cardales, ruta_8).
conectadas(carmen_de_areco, san_andres_de_giles, ruta_7).
conectadas(san_andres_de_giles, lujan, ruta_7).
conectadas(cardales, lujan, ruta_6).
conectadas(san_antonio_de_areco, san_andres_de_giles, ruta_41).
conectadas(san_andres_de_giles, mercedes, ruta 41).
conectadas(arrecifes, carmen_de_areco, ruta 51).
conectadas(carmen_de_areco, chivilcoy, ruta_51).
conectadas(lujan, mercedes, ruta_5).
conectadas(mercedes, chivilcoy, ruta_5).
siguiente(X, Y, Z) :- conectadas(Y, X, Z).


Escribir las siguientes consultas:
A. Están conectadas San Andrés de Giles y Mercedes?
B. Chivilcoy está conectada con San Antonio de Areco?
C. La ruta 51 conecta Carmen de Areco con San Andrés de Giles?
D. Con quien está conectada Luján?
E. Cual es la que está conectada con San Andrés de Giles?
F. Cuales son las que están conectadas con San Andrés de Giles?
G. Que rutas llegan a Luján?
H. Que rutas salen de Luján?
I. Se puede salir de Carmen de Areco y llegar a Luján pasando por San
Andrés de Giles?
J. Que ruta llega a Chivilcoy saliendo de Luján y pasando por Mercedes?