11. En un negocio se desea armar una oferta para fin de año combinando un artículo de bazar, uno de perfumería y uno de juguetería, con la condición de que la oferta no supere un cierto precio máximo. Para ello contamos con la siguiente base de datos:
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
Hacer una consulta para encontrar todas las ofertas de menos de $50.