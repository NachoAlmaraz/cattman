# Cattle manager

##### This is an early design for the entity relaitonship model

Se nos presenta una aplicación ganadera, la que quiere registrar los siguientes datos.

  - Todos los datos relativos al animal como su idanimal (crotal), fecha nacimiento, nombre, sexo, raza, partida nacimiento, numero de id sanitario, localización del animal.
  - Un registro de saneamientos(veterinario) de todos los animales con un idsaneamiento, la fecha del mismo, la medicina empleada y posibles notas. Las crías no están asociadas.
  - Los partos de los animales deben quedar registrados con la fecha de la fecundación, el padre y la madre del animal, la fecha del parto y los kilos aproximados de la cría.
  - Cuando la cría tenga 4 o 5 meses se le destetará, tenemos que guardar esta fecha junto con los kilos del ternero en ese momento.
  - Tenemos que tener un registro de ventas donde tendremos el idtransación, idanimal, precio de venta, el peso del canal y el precio por kilogramo.

##### Deberemos poder consultar de forma rápida:

  - Búsqueda de animal por id mostrando su información principal.
  - Listado ordenado de los próximos saneamientos, actividad recurrente.
  - Los partos que ha tenido cada animal.
  - La información del parto buscando por animal.
  - Listado de defunciones por año.
  - Ventas en un intervalo de tiempo.

______


![Entity relationship](/diagram/entity-relationship-1.png)
