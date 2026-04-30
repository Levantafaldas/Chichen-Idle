# Chichen-Idle

## Concepto inicial

Juego desatendido (Idle) donde se gestiona una granja de gallinas.

La generación pasiva serian los propios huevos puestos por las gallinas y el incremental seria la cantidad de gallinas, aunque solo se representaria 1 unica gallina visualmente.

Dudas de estos, se puede utilizar las gallinas realistas, investigar razas de gallinas por territorio y explotar estar razas en cada uno de sus territorios o tambien se puede inventar el tipo de gallina por territorio basandonos en esteriotipos o curiosidades de las zonas.

El mapa/territorio serio el propio goblo terraqueo, pero para simplificar el inicio se seleccionaria una region dentro de España, porque esto, porque me tira la tierra (jejeje).

## Stack

Para el desarrollo se utiliza Unity con scripts en C#. Por el momento no se guarda información en ningún sistema externo, todo los guardados se realizan de manera interna en ficheros JSON.

## MVP

### Pantalla inicial 

menú con 3 botones:
- iniciar/cargar
- opciones
- salir

### Pantalla de juego

menú lateral de mejoras y pantalla donde poder realizar acciones sobre las gallinas.

### Menú de pausa

nos permite acceder a las opciones, guardar la partida o salir.

## Mecanica del juego

Al principio del juego se te pedira que selecciones un pais y region de una lista, despues de eso se te regalara una gallina de la seleccion basica.

Después de estas selecciones se iniciara el juego, se tendra que dar de comer a la gallina para que esta ponga huevos, al tener los primeros 100 podremos obtar a comprar mas gallinas, a los 500 podremos automatizar el dar de comer a la gallina, lo que iniciara la parte idle del juego.