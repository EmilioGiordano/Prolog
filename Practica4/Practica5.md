## Guia de ejercicios: Decisiones en Prolog

- [Guia de ejercicios: Decisiones en Prolog](#guia-de-ejercicios-decisiones-en-prolog)
  - [Ejercicio 1](#ejercicio-1)
      - [Hechos](#hechos)
      - [Regla](#regla)
  - [Ejercicio 2](#ejercicio-2)
  - [Ejercicio 3](#ejercicio-3)
      - [Predicado binario](#predicado-binario)
  - [Ejercicio 4](#ejercicio-4)
      - [Regla](#regla-1)
  - [Ejercicio 5](#ejercicio-5)
      - [Predicado binario](#predicado-binario-1)
  - [Ejercicio 6](#ejercicio-6)
  - [Ejercicio 7](#ejercicio-7)
  - [Ejercicio 8](#ejercicio-8)
  - [Ejercicio 9](#ejercicio-9)
  - [Ejercicio 10](#ejercicio-10)
      - [Predicado](#predicado)
  - [Ejercicio 11](#ejercicio-11)

### Ejercicio 1
Se tiene una base con los siguientes hechos:
##### Hechos
```prolog
madre_de(ana, luis).
padre_de(juan, luis).
```
__Construir una regla para definir el predicado "progenitor_de__
##### Regla
```prolog

```

### Ejercicio 2
Definir un predicado ternario "mayor_o_igual" que relaciona dos números con el mayor de ambos, o con uno de ellos si son iguales.

### Ejercicio 3
Definir un predicado binario "paridad" que relaciona un número con la palabra "par" si el número es par, o con la palabra "impar" de otro modo
##### Predicado binario
```prolog
```
### Ejercicio 4
Escribir una regla para "cuñado_de" dada una base como:
```prolog
esposos(ana, luis).
hermanos(maria, juan)
```
##### Regla
```prolog
```
### Ejercicio 5
Preparar un predicado binario que sea verdadero cuando sus dos sujetos sean números tales que el primero es múltiplo del segundo.
##### Predicado binario
```prolog
```
### Ejercicio 6
Completar el predicado anterior para que sea verdadero si cualquiera de los números es
múltiplo del otro.

### Ejercicio 7
Desarrollar un predicado ternario cuyos sujetos representan las longitudes de tres
segmentos, y que sea verdadero si estos tres segmentos forman triángulo. Recordar que la
suma de las longitudes de dos lados cualesquiera de un triángulo siempre debe ser mayor que
la longitud del restante.

### Ejercicio 8
Un vendedor cobra una comisión del 3% sobre sus ventas, pero si vendió más de USD 50000 recibe un 1% más, además de un premio fijo de U$D 1200. Preparar un predicado que relacione
el total vendido con la comisión a cobrar.

### Ejercicio 9
A un tanque llega agua a través de una canilla, mientras que simultáneamente desagua a
través de un sumidero. La capacidad del tanque es de T litros, por la canilla llegan C litros por
minuto, y por el sumidero desaguan S litros por minuto. Inicialmente el tanque tiene L litros.
Desarrollar un predicado que vincule los valores T, C, S y L, con los minutos que tarda en
llenarse o vaciarse el tanque.



### Ejercicio 10
Escribir un predicado que relacione una hora dada en horas, minutos y segundos con la hora
será un segundo después.

##### Predicado
```prolog
```
### Ejercicio 11
Dados los siguientes datos sobre jugadores de basket:
```prolog
cantidad_de_dobles(juan, 15).
cantidad_de_triples(jose, 5).
cantidad_de_infracciones(juan, 6).
```
que representan la cantidad de dobles, triples e infracciones de los jugadores a lo largo del
campeonato, se requiere un predicado que relacione el nombre de un jugador con alguna de las siguientes categorías:
Posible NBA, cuando el jugador hizo al menos 10 triples, 30 dobles y cometió menos de 5 infracciones.
Bueno, cuando el jugador hizo al menos 20 dobles y cometió menos de 8 infracciones.
Regular, cuando el jugador hizo al menos 10 dobles y cometió menos de 12 infracciones.
Desastroso, cuando el jugador hizo menos de 10 dobles y cometió 12 o más infracciones.
