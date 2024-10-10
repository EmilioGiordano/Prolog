1. Escribir las siguientes oraciones en Prolog:
- El oro es valioso.
- Isabel es mujer.
- Juan es Rey.
- Zeus es el progenitor de Hercules.
- José le presta dinero a Pedro.


```prolog
es_valioso(oro). 
es_mujer(isabel).
es_rey(juan).
es_progenitor_de(zeus, hercules).
le_presta_dinero(jose, pedro).
```

2. Escribir en Prolog los datos relevantes, (a los efectos genealógicos), del siguiente párrafo: "La familia de Luis no es muy numerosa, sus padres, Carlos y Susana, tuvieron tres hijos: Roberto, Amalia, y Luis, de los cuales Luis es el menor. Carlos, a su vez, tiene una hermana mayor llamada Isabel, siendo ambos hijos de Ana y Guillermo. Los padres de Susana, Mercedes y Ernesto, tuvieron otra hija bastante menor que ella, a quien bautizaron con el nombre de Angélica, la que es tan bella como su nombre. Los dos hijos de Luis y su esposa Laura, llamados Federico y Carla, están estudiando letras".
__Utilizar solamente los predicados "es_progenitor_de", "es_varon" y "es_mujer".__

```prolog
% Definición del predicado padre
padre(X, Y) :- es_progenitor_de(X, Y), es_varon(X).
% familia carlos y susana
es_progenitor_de(carlos,roberto).
es_progenitor_de(carlos,amalia).
es_progenitor_de(carlos,luis).
es_progenitor_de(susana,roberto).
es_progenitor_de(susana,amalia).
es_progenitor_de(susana,luis).
% familia luis y laura
es_progenitor_de(luis, federico).
es_progenitor_de(luis, carla).
es_progenitor_de(laura, federico).
es_progenitor_de(laura, carla).
% familia ana y guillermo
es_progenitor_de(guillermo, carlos).
es_progenitor_de(guillermo, isabel).
es_progenitor_de(ana, carlos).
es_progenitor_de(ana, isabel).
% familia ernesto y mercedes
es_progenitor_de(ernesto, angelica).
es_progenitor_de(ernesto, susana).
es_progenitor_de(mercedes, angelica).
es_progenitor_de(mercedes, susana).
%genero
es_varon(carlos).
es_varon(roberto).
es_varon(luis).
es_varon(federico).
es_varon(guillermo).
es_varon(ernesto).
es_mujer(amalia).
es_mujer(susana).
es_mujer(laura).
es_mujer(carla).
es_mujer(mercedes).
es_mujer(angelica).
```

3. Usando la base de datos generada en el problema de la familia de Luis, y con
lo que se conoce hasta ahora, escribir consultas para obtener la siguiente
información:
Preguntas simples:
A. ¿Es Carlos progenitor de Guillermo?
B. ¿Es Jorge progenitor de Gonzalo?
C. ¿Es Carlos progenitor de Amalia?
D. Usando el predicado "padre" preguntar: ¿Es Carlos padre de Roberto?
E. ¿Gonzalo es mujer?
F. ¿Alberto es varón?
__Preguntas compuestas (conjunciones):__
G. ¿Es cierto que Luis es progenitor de Carla, y que Carla es mujer?.
H. ¿Es cierto que Ernesto es progenitor de Carlos, y que éste es progenitor
de Luis, y a su vez Luis es progenitor de Carla?

4. Usando la base de datos generada en el problema de la familia de Luis, y con
lo que se conoce hasta ahora, escribir consultas para obtener la siguiente
información:
A. ¿Federico es progenitor de alguien?
B. ¿Quiénes son los progenitores de Roberto?
C. ¿Guillermo tuvo alguna hija?
D. ¿Ernesto tuvo algún hijo varón?
E. ¿Roberto y Amalia tienen el mismo padre?
F. ¿Ernesto tuvo alguna hija que a su vez tenga una hija?

5. Definir un predicado que relacione una temperatura expresada en grados Celsius con la misma temperatura expresada en grados Farenheit. Recordamos que F = (9/5) * C + 32

6. Definir un predicado que relacione una longitud expresada en centímetros,
con la misma longitud expresada en pulgadas, pies y yardas. Recordamos que:
1 yarda = 3 pies
1 pie = 12 pulgadas
1 pulgada = 2.54 centímetros

7. Una empresa de ventas paga a sus empleados un salario fijo de 800 pesos, mas una comisión de $50 por cada venta realizada, más el 8% sobre el monto total de ventas. Escribir la regla de un predicado ternario que vincule la cantidad de ventas, con el monto total de ventas y el sueldo del vendedor.
   
8. Definir un predicado que vincule las notas de cuatro parciales con la nota promedio.

9. Una empresa tiene 5 gerentes, 23 empleados administrativos y 7 ordenanzas. Preparar un predicado que vincule el sueldo de cada categoría con el total que la empresa debe pagar a fin de mes.
10. Un millonario excéntrico tenía tres hijos Carlos, José' y Marta. Al morir dejó el siguiente legado: "A José le dejo 4/3 de lo que le dejo a Carlos; a Carlos le dejo 1/3 de mi fortuna y a Marta le dejo la mitad de lo que le dejo a José". Preparar un predicado que vincule la suma a repartir con lo que le toca a cada uno.
11. En un negocio se desea armar una oferta para fin de año combinando un artículo de bazar, uno de perfumería y uno de juguetería, con la condición de que la oferta no supere un cierto precio máximo. Para ello contamos con la siguiente base de datos:
```prolog
bazar(fuentes).
bazar(vasos)
bazar(juego_de_café).
perfumería(jabones).
perfumería(crema).
perfumería(perfume).
juguetería(autito).
juguetería(muñeca).
juguetería(oso).
precio(fuentes, 15).
precio(vasos, 12).
precio(juego_de_café, 20).
precio(jabones, 10).
precio(crema, 15).
precio(perfume, 25).
precio(autito, 10).
precio(muñeca, 15).
precio(oso, 20).
Escribir una regla "oferta" que relacione tres artículos, uno de cada
rubro, con el precio máximo, y que sea verdadero cuando la oferta no
supere el precio máximo.
```
__Hacer una consulta para encontrar todas las ofertas de menos de $50.__


12. La siguiente es la descripción de la familia Adams:
```prolog
padre_de(homero, pericles).
padre_de(homero, merlina).
padre_de(desconocido, lucas).
padre_de(desconocido, homero).
varon(homero).
varon(lucas).
varon(cosa).
varon(pericles).
mujer(merlina).
mujer(morticia).
mujer(la-abuela).
madre(la-abuela, homero).
esposos(morticia, homero).
```
Usando los predicados anteriores, definir la relación "hermano_de".

Escriba las reglas necesarias para la consulta : 
```prolog
?- tio(Quien,merlina).
```
13. Se tiene la siguiente base de datos con ciudades vecinas y las rutas que las conectan:
```prolog
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
```

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