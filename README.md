# Full Ítems Advancements
Consigue todos los ítems de Minecraft y visualízalo con este datapack. Un logro por cada ítem.

Un reto con muchas aventuras.

<p align="center">
  <img src="imagenes/flayer.png" alt="Texto alternativo" style="width:50%;">
</p>



## Descripción
Este datapack posee las funciones necesarias para tener **un logro por cada ítem de Minecraft**. Incluye conteo y visualización de los ítems conseguidos y de los restantes. El total de estos logros en la primera versión son; **1148 ítems**.

Se puede jugar en multijugador y sigleplayer. 

![](imagenes/boton_l.jpg)



## Descarga
- Datadack en github [Descargar pulsando en download](https://github.com/iSeeQR/fullitem_advancements/blob/main/descargas/fullitem_advancements_1_20.zip)
- Datadack [Drive](https://drive.google.com/file/d/1EnOIU2QD-jJFW2aaZKJhFLgtvGSCvZ9j/view?usp=drive_link)
- MapJamRichMaps [Drive](https://drive.google.com/file/d/1oxZULKsCVq-iL0I0GLAwALWOWfY4Xu1v/view?usp=drive_link)
  
El mundo de MapJamRichMaps es para testeo. El **datapack** se ha creado **para mundos vanilla**. No puedo asegurar que se puedan conseguir todos los ítems en este mundo. Pero si podrás testearlo.


<p align="center">
  <img src="imagenes/flayeraventura.png" style="width:50%;">
</p>

---

  
## Índice

- [Descripción](#Descripción)
- [Descarga](#Descarga)
- [Descripción general](#Descripción-general)
- [Recompensa](#Recompensa)
- [Otras ventajas](#Otras-ventajas)
- [Descripción técnica](#Descripción-técnica)
- [Generación datapack](#Generación-datapack)
- [Mantenimiento y soporte](#Mantenimiento-y-soporte)
- [RoadMap](#RoadMap)
- [Testeo](#Testeo)
- [Descripción concurso](#Descripción-concurso)
- [Speed Run](#Speed-Run)
- [Como instalar un datapack](#Como-instalar-un-datapack)
- [Contacto](#Contacto)
  


## Descripción general
El jugador iniciará el mundo con el datapack incluido y ya estará listo para comenzar la aventura. 

Al detectar un cambio en el inventario se activarán los logros.

![](imagenes/enjuego.png)

En la siguiente imagen se pueden ver los texto que componen el principio y el fin de la obtención de todos los logros. (Simulado en test. Los texto han sido mejorados en la versión final)

![](imagenes/ultimostextos.png)

Los ítems están dividido en las siguientes secciones:

Construcción, decoración, redstone, transporte, objetos varios, alimentación, herramientas, combate, pociones y honestidad.

![](imagenes/secciones.jpg)



## Recompensa
¡Si consigues todos los ítems tendrás un buen premio!

![](imagenes/recompensa.png)

La persona que a dedicado el tiempo al estudio, búsqueda y crafteo de cada ítem. Querrá un **Debug Stick** para admirar fácilmente la preciada colección de su museo.



## Otras ventajas 
Si quieres conseguir el logro de comer todos los alimentos. Este datapack puede ayudarte con esa tarea.

![](imagenes/boton_l_alimentacion.jpg)



## Descripción técnica
Cada ítem tiene su logro, el cual se define como en el siguiente ejemplo


```json
{
  "display": {
    "description": {
      "text": "Has obtenido Cod.",
      "color": "yellow"
    },
    "title": {
      "text": " Cod ",
      "color": "white"
    },
    "icon": {
      "ítem": "minecraft:cod"
    },
      "frame": "goal",
      "show_toast": true,
      "announce_to_chat": true,
      "hidden": false
  },
  "criteria": {
    "stone": {
      "trigger": "minecraft:inventory_changed",
      "conditions": {
        "ítems": [
          {
           "ítems":[ "minecraft:cod" ]}          
        ]
      }
    }
  },
  "rewards": {
    "function": "function:alimentacion/cod"
  },
  "parent": "fullítem:alimentacion/root"
}
```

Al conseguir este logro se dispara la lectura por ejemplo de la siguiente función

    ...
    execute as @p[scores={Advancements=10}] run tellraw @p {"color":"light_purple","text":"Quedan 10 ítems."} 
    ...

El conteo de ítems se hace mediante scoreborad dummy



## Generación datapack.
El datapack se genera mediante un proceso en Java que crea todos los directorios y ficheros. En dicho código se encuentran los comandos que serán escritos en los ficheros del datapack. 

__De otra manera sería imposible crear este proyecto. Es un proceso Java que genera código para Minecraft Java.__

El datapack también puede generarse con ítems de mods.



## Mantenimiento y soporte
Gracias al proceso Java creado se procura un **soporte y mantenimiento** del datapack con el paso del tiempo. Incluyendo versiones futuras.



## RoadMap
- **Añadir ítems que faltan:** ítems como los cuernos, cuadros, flechas encantadas, libros encantados y pociones deben distinguirse en logros individuales. Estos ítems están recogidos en la pestaña "honestidad" de los logros.
- **Organización de los logros:** Hay que reestructurar las ítems.
- **Goals:** Para ítems como el banner de creeper, la mena negra de esmeralda, cabeza de piglin, etc hay que poner un Goal legendario
- **Añadir el banner ominous:** Estudiar como incluirlo en un logro.



## Testeo
1. Se ha testeado el logro de cada ítem
2. Se ha testeado la aparición de la recompensa al conseguir todos los ítems
3. Se ha testeado que el contador llegue a cero cuando se consigan todos los ítems
4. Se ha testeado que el datapack dispare un logro con el ítem de un mod. Ejemplo: conquest:slate



## Descripción concurso
Map Jam Hispana: Comandos Creativos 2023

[Bases de concurso](https://www.patreon.com/posts/86402247)
- Una frase de qué es lo que más te gusta de lo que has creado:

    Satisfacer una necesidad de algunos jugadores. Incluido yo. En mi mundo survival juego a conseguir todos los ítems. Crear este datapack es lo que más me ha gustado.
  
    Estudiar, aprender y trastear con /execute
  
- Una frase de qué añadirías si tuvieses quince días más.
  
    Añadir los ítems que faltan. Las flechas encantadas, pociones, libros encantados... Hay que dedicarle tiempo a estos ítems ya que su diferenciación no es sencilla. En 15 días sería mi objetivo principal.



## Speed Run
¿Cúanto tiempo tardas en conseguir todos los ítems de Minecraft?

| Jugador | Tiempo | Vídeo/Serie | Versión |
|---------|--------|-------|---------|
|     |    |  |    |


<p align="center">
  <img src="imagenes/flayerspeedrun.png" style="width:50%;">
</p>



## Como instalar un datapack
1. Una vez descargado el Datapack
2. Ir al directorio saves de Minecraft. Puedes ir a esta carpeta pulsando sobre un mundo y en 'Editar' pulsar en 'Abrir carpeta del mundo'
3. En esta carpeta hay que incluir el Datapack dentro de la carpeta 'datapacks'. No olvides descomprimir el zip 'fullitem_advancements_1_20.zip'
4. Inicia el mundo y todo estará listo para vivir nuevas aventuras.



## Contacto

Si tienes alguna pregunta, contáctame en Twitter: [@fullItemsMc](https://twitter.com/fullItemsMc).

---

__Proyecto desarrollado 100% por un humano. 0% IA.__

---
