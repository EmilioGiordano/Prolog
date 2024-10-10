## GUÍA DE EJERCICIOS: recursión y listas en Prolog

- [GUÍA DE EJERCICIOS: recursión y listas en Prolog](#guía-de-ejercicios-recursión-y-listas-en-prolog)
  - [Ejercicio 1](#ejercicio-1)
      - [Hechos](#hechos)
      - [Predicados](#predicados)
      - [Consulta](#consulta)
  - [Ejercicio 2](#ejercicio-2)
  - [Ejercicio 3](#ejercicio-3)
  - [Ejercicio 4](#ejercicio-4)

### Ejercicio 1
Dada una base de datos en la cual se describe una cadena de progenitores con hechos como:

##### Hechos
```prolog
progenitor_de(juan, luis).
progenitor_de(luis, maria).
progenitor_de(maria, ana).
progenitor_de(jose, hector).
```
__Escribir un predicado que relacione a una persona con un antepasado de la misma__

##### Predicados
```prolog
% Condicion de antepasados son padres
antepasado_de(Antepasado, Persona) :-
    progenitor_de(Antepasado, Persona).
% Condicion de antepasados son abuelos
    antepasado_de(Antepasado, Persona) :-
         progenitor_de(Antepasado, Intermedio),
         antepasado_de(Intermedio, Persona).
```
##### Consulta
```prolog
antepasado_de(juan, luis).
true
antepasado_de(juan, maria).
true
antepasado_de(juan, hector).
false
```
### Ejercicio 2
Resolver el problema de encontrar el MCD entre dos números, sabiendo que, si los números son iguales, el MCD es el mismo número, en otro caso el MCD es igual MCD entre el menor de ellos y la diferencia entre ambos
```prolog
```

### Ejercicio 3
Resolver el problema de encontrar el enésimo término de la sucesión de Fibonacci
```prolog
```

### Ejercicio 4
Predicado que relaciona una lista numérica de dos elementos con otra lista con esos dos elementos ordenados de menor a mayor.