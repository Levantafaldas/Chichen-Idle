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

Se puede incrementar el número de gallinas haciendo que incremente la cantidad de huevos producidos, ejemplo:

- Se inicia la partida con una Gallina común considerada de Tier 1, esto quiere decir que generara 1 huevo cada vez que coma. Al llegar a 100 huevos podremos obtar a comprar una gallina del mismo tipo, lo que hara que tengamos 2 gallinas y eso nos generara 2 huevos cada vez que coman. En este caso la formula seria H = C * F, donde H es la cantidad de huevos, C es la cantidad de gallinas que tenemos y F el factor de producción. 
- El valor de compra de las gallinas se incrementaria en un 2.1 por cada gallina comprada, la formula seria la siguiente V = (100 * 2.1)(C-1), la compra de la primera gallina estaria siempre fijo en 100, miestras que las siguientes se incrementaria siguiendo esa formula, esto de aplica para las gallinas comunes, que es el caso de mecanica que estamos tratando ahora.
- También se podran adquirir mejoras, que podran hacer que se cree generación pasiva, incremente la producción base o reduzca el precio de compra.


### Tipos de Gallinas

- Basicas
    - Estas son las que no tienen peculiaridades especiales, por asi decirlo las auctoctonas de la zona, por ejemplo:
        - Gallina común
        - Gallina marrón
        - Gallina amarilla
    - Dentro de estas podemos encontrar subcategorias de rareza, dado que hay gallinas basicas menos comunes que pueden hacer que su puesta de huevos sea mas valiosa.
    - Posible tabla de valores por rareza de gallina:    
        |Tier|Factor de produción base|
        |:---:|:---:|
        |1|1| 
        |2|1.2|
        |3|1.5|
        |4|1.8|
        |5|2.2|