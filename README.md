# Tarea2.3-LenguajeMarcas
La presente tarea para la asignatura *Lenguaje de Marcas* consiste en la construcción de una página estática para el proyecto *Lunar Lander*, tomando como referencia el proyecto de otro compañero de clase.

En este caso, el punto de partida es este [proyecto](https://github.com/shamshir/Lunar_Lander).
## Visualización
El presente repositorio cuenta con tres ramas distintas. La primera, *master*, es la versión principal y se encuentra correctamente indentada. La segunda rama, *minify* es idéntica a la rama *master*, salvo que todos los archivos HTML y CSS están comprimidos en una sola lía de código cada uno. Por último, la rama *noMenu* es igual que la rama *master* pero con el menú oculto, para facilitar la visualización de la página sin tener que añadir el atributo "display:none" en el inspector del navegador.

[Visualizar la página con menú (rama *master*)](https://rawgit.com/shamshir/Tarea2.3-LenguajeMarcas/master/index.html)

[Visualizar la página sin menú (rama *noMenu*)](https://rawgit.com/shamshir/Tarea2.3-LenguajeMarcas/noMenu/index.html)

## Funcionamiento
Para poder ver cómo cambian los indicadores de velocidad, fuel y altura tanto en la versión de escritorio como en la versión de móvil, se pueden seguir las siguientes instrucciones. Cabe destacar que, en la versión para móvil, la velocidad se expresará intercambiando tres imágenes distintas, por lo que actualmente (sin javascript) no es posible cambiar entre esas imágenes.

En escritorio:
* Velocidad > Modificar los grados de rotación de la imagen que se encuentra en el div con Id "aguja"
* Fuel > Modificar la altura del div con Id "fondoFuel"
* Altura > Modificar la distancia al "bottom" del div con Id "fondoAltura"

En móvil:
* Fuel > Modificar la anchura del div con Id "fondoFuel"
* Altura > Modificar la distancia al "bottom" del div con Id "fondoAltura"

## Localización de Elementos
Tanto en la versión de escritorio como en la versión de móvil, la nave centrada encabeza la página y la luna ocupa la parte inferior de la pantalla, ocupando cada una un 20% de la altura disponible.

Asímismo, los botones de play/pause y de restart, también ocupan el mismo lugar en ambas versiones: el botón de menú(play/pause) en la esquina superior derecha y el botón de restart debajo.

Las opciones "About" e "Instrucciones" del menú, enlazan dos páginas de información en ambas versiones. Mientras que en la versión de escritorio la página carece de scroll ya que el texto cabe sin problema, en la versión para móvil se ha aplicado un scroll automático para poder ver correctamente todo el texto en dispositivos de menos resolución. Además, el botón de retorno al menú, que podemos encontrar al final de ambas páginas de texto, tiene un tamaño más grande en la versión de móvil, para facilitar su utilización. Cabe destacar que en ambas versiones está visible el botón de play/pause que, en la versión con javacript de este proyecto, nos devolverá al juego, en vez de al menú.

### Indicadores Escritorio
Los indicadores de velocidad, fuel y altura en la versión de escritorio están contenidos en un div que ocupa la parte izquierda de la pantalla. Los indicadores de fuel y altura comparten espacio horizontal, ocupando cada uno la mitad del div. Encima de ambos, encontramos el indicador de velocidad, compuesto por dos imágenes distintas: la imágen del velocímetro y la imagen de la aguja, esta última ya preparada para poder rotarse.

Cabe destacar que los indicadores de fuel y altura están constituidos por un div que engloba la imagen correpondiente y otro div detrás que "llena" o "vacía" el indicador.
### Indicadores Móvil
Los indicadores de velocidad, fuel y altura en la versión de móvil también están contenidos en un div que ocupa la parte izquierda de la pantalla. En este caso, no obstante, ningún indicador comparte espacio horizontal y están situados, de arriba a abajo: fuel, velocidad y altura. Mientras que los indicadores de altura y fuel funcionan y están construidos de igual forma que en la versión de escritorio (salvo que el indicador de fuel se encuentra horizontal y no vertical), el indicador de velocidad está compuesto por una imagen de fondo transparente que irá alternandose entre tres imágenes distintas, en función de la velocidad que lleve la nave.
## Cambios respecto al Proyecto de partida
Se han realizado diversos cambios respecto al proyecto de base, proporcionado por un compañero, y éstos se recogen en los siguientes apartados.
### Menú
El menú que aparece en el centro de la pantalla también ha sido rediseñado, respetando la combinación de colores azul-naranja. En cuanto a las opciones que en él aparecen, éstas son "About", "Instrucciones" y Dificultad (esta última dividida en fácil o difícil). Estas opciones se han especificado a posteriori ja que el proyecto no especifica cuáles deben ser.

Se ha desestimado la propuesta de introducir sonido en el juego, debido a la falta de realismo de dicha idea, ya que en el vacío del espacio no se propaga el sonido.

Los enlaces de "About" e "Instrucciones", enlazan otras dos páginas en las que solo se muestra texto informativo acerca del juego. Ya que todavía desconocemos cómo funcionará, ambas páginas están llenas de texto sin sentido.
### Imágenes
Las siguientes imágenes han sufrido cambios estéticos o han sido creadas de nuevo desde el principio. Después de la creación de las nuevas imágenes, éstas han sido optimizadas utilizando la herramienta Online [TinyPNG](https://tinypng.com/).
#### Fondo
La imagen del espacio del fondo ha sido cambiada por un lienzo negro con algunas estrellas debido a que el fondo propuesto en el proyecto ofrecía una imagen con mucha resolución y profundidad, en comparación a la nave, hecha con pixel art. Además, la imagen de fondo propuesta no tiene la resolución suficiente para quedar bien en pantallas a partir de HD, ya que la imagen llega a pixelarse al estirarla tanto.
#### Luna
La imagen de la luna ha sido creada de nuevo, con la finalidad de darle cierta curvatura, lo que añade realismo al diseño. Los colores originales, no obstante, han sido mantenidos en la nueva luna, que ha sido realizada siguiendo el mismo procedimiento que fue utilizado en mi análisis y propuesta de *Lunar Lander*.
#### Indicadores de Fuel y Altura
Los indicadores de Fuel y Altura han sido creados de nuevo, con la finalidad de que ambos sean del mismo tamaño, compartan la misma estética, y tengan un fondo transparente.

En el caso del móvil, mientras que el indicador de altura se mantiene igual, el indicador de fuel pasa a presentarse de forma horizontal, de modo que también se ha creado la imagen correspondiente.
#### Indicador de Velocidad
El indicador de velocidad ha sido modificado ligeramente. En primer lugar, mediante Photoshop, se ha separado la aguja del resto del velocímetro y se le ha dado un color naranja. En segundo lugar, se han eliminado los números del velocímetro, debido a su tamaño y que tampoco son necesarios para que el indicador de velocidad funcione de forma ergonómica.

En el caso del móvil, se han creado tres imágenes triangulares inspirandas en la proporcionada en el proyecto. Se trata de tres imágenes con fondo transparente que irán intercambiandose a medida que aumente/disminuya la velocidad.
#### Botones
Los botones del juego (play/pause y menú) han sido creados de nuevo para garantizar una estética global en torno al color azul. Los símbolos dentro de los botones se han representado en naranja, debido a que es el color complementario del azul, resultado de mezclar rojo y amarillo.
Se ha incrustado el símbolo de play y de pause en la imagen lisa que simula un planeta. De esta forma, para cambiar entre pausa y play, habrá que cambiar toda la imagen.

Los colores de ambos botones se han alternado para darles contraste y diferenciarlos más a nivel visual.
