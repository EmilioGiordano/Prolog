## GUÍA DE EJERCICIOS: recursión y listas en Prolog

- [GUÍA DE EJERCICIOS: recursión y listas en Prolog](#guía-de-ejercicios-recursión-y-listas-en-prolog)
  - [Ejemplo: Factorial](#ejemplo-factorial)
  - [Ejercicio 1](#ejercicio-1)
      - [Hechos](#hechos)
      - [Predicados](#predicados)
      - [Consulta](#consulta)
  - [Ejercicio 2](#ejercicio-2)
      - [Consulta](#consulta-1)
  - [Ejercicio 3](#ejercicio-3)
  - [Ejercicio 4](#ejercicio-4)

### Ejemplo: Factorial 
```prolog
% Caso base: el factorial de 0 es 1.
factorial(0, 1).

% Caso recursivo: factorial de N es N 
% multiplicado por el factorial de N-1.
factorial(N, Resultado) :-
    N > 0,
    N1 is N - 1,          % Decrementamos N
    factorial(N1, R1),    % Llamada recursiva
    Resultado is N * R1.  % Calculamos el resultado
```
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
?- antepasado_de(juan, luis).
true
?- antepasado_de(juan, maria).
true
?- antepasado_de(juan, hector).
false
```
### Ejercicio 2
Resolver el problema de encontrar el MCD entre dos números, sabiendo que, si los números son iguales, el MCD es el mismo número, en otro caso el MCD es igual MCD entre el menor de ellos y la diferencia entre ambos
```prolog
% Caso base: si los numeros son iguales el MCD es 
% el mismo número.
% MCD: Maximo Comun Divisor
mcd(A, A, A).

% Si A es diferente de B, llama recursivamente 
% a mcd con el menor de los dos números y la
% diferencia.
mcd(A, B, MCD) :-
    A \= B,
    (A > B ->  
    	MCD1 is A - B,
        mcd(B, MCD1, MCD)
    ;   MCD1 is B - A,
        mcd(A, MCD1, MCD)
    ).
```
##### Consulta
```prolog
?- mcd(4,12, MCD)
MCD = 4
```
### Ejercicio 3
Resolver el problema de encontrar el enésimo término de la sucesión de Fibonacci
```prolog
% Caso base: el primer término de Fibonacci es 0.
fibonacci(0, 0).
% Caso base: el segundo término de Fibonacci es 1.
fibonacci(1, 1).
% Caso recursivo: el enésimo término es la 
% suma de los dos anteriores.
fibonacci(N, F) :-
    N > 1,
    N1 is N - 1,    % Decrementamos N
    N2 is N - 2,    % Decrementamos N para el segundo término
    fibonacci(N1, F1),  % Llamada recursiva para N-1
    fibonacci(N2, F2),  % Llamada recursiva para N-2
    F is F1 + F2.  % Calculamos el término actual
```

| N | Resultado |
|----| ----|
| 0 | 0 |
| 1 | 1 |
| 2 | 1 |
| 3 | 2 |
| 4 | 3 |
| 5 | 5 |
| 6 | 8 |
| 7 | 13 |
| 8 | 21 |
| 9 | 34 |
| 10 | 55 |

```prolog
?- fibonacci(10, F).
F = 55
```
### Ejercicio 4
Predicado que relaciona una lista numérica de dos elementos con otra lista con esos dos elementos ordenados de menor a mayor.