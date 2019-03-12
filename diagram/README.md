# Cattle manager

##### This is an early design for the entity relaitonship model

Se nos presenta una aplicación ganadera, la que quiere registrar los siguientes datos.

  - Todos los datos relativos al animal como su idanimal (crotal), fecha nacimiento, nombre, sexo, raza, partida nacimiento, numero de id sanitario, localización del animal.
  - Un registro de saneamientos(veterinario) de todos los animales con un idsaneamiento, la fecha del mismo, la medicina empleada, el veterinario que la realiza, el lugar y posibles notas sobre patologías. Las crías no están asociadas.
  - Los partos de los animales deben quedar registrados con la fecha de la fecundación, el padre y la madre del animal, la fecha del parto y los kilos aproximados de la cría.
  - Cuando la cría tenga 7 o 8 meses se le destetará, tenemos que guardar esta fecha junto con los kilos del ternero en ese momento.
  - Tenemos que tener un registro de ventas donde tendremos el idventas, idanimal, fecha, precio de venta, el peso del canal y el precio por kilogramo.

##### Deberemos poder consultar de forma rápida:

  - Búsqueda de animal por id mostrando su información principal.
  - Listado ordenado de los próximos saneamientos, actividad recurrente.
  - Los partos que ha tenido cada animal.
  - La información del parto buscando por animal.
  - Listado de defunciones por año.
  - Ventas en un intervalo de tiempo.
  - Consulta de producción total por animal, crías y beneficios económicos.
  - Contabilizar y mostrar todos los terneros menores de X edad

______

##### Modelo entidad relación:
![Entity relationship](/diagram/entity-relationship-1.svg)

______

##### Modelo relacional:

Tras los cambios efectuados recientemente en la entidad 'Animales' en el modelo de entidad relación, he decidido realizar una concatenación en la relación 'Parto' con las tres claves primarias necesarias para registrarlo y así normalizar su redundancia con el id de la hebra, del toro y del ternero.   

![Relationship model](/diagram/relationship-model.svg)
