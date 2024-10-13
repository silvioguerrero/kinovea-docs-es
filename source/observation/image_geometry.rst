
Transformación de imagen
====================

Orientación de la imagen
-----------------
Para cambiar la orientación de la imagen utilice los menús debajo :menuselection:`Imagen --> Rotación`.

Están disponibles las siguientes opciones:

- :guilabel:`Sin rotación`
- :guilabel:`90° en sentido horario`
- :guilabel:`90° en sentido antihorario`
- :guilabel:`180°`

Los videos filmados en modo retrato en un teléfono inteligente generalmente ya tienen una bandera incrustada en el archivo de video y no es necesario girarlos manualmente.

Imagen reflejada (espejo)
---------------
Para reflejar la imagen, es decir, voltearla a lo largo del eje vertical, utilice el menú Espejo.

Zoom y ampliación
--------------------
Para ampliar la imagen utilice :kbd:`CTRL` + **rueda del ratón** o :kbd:`CTRL` + :kbd:`Menos` and :kbd:`CTRL` + :kbd:`Más`.

:kbd:`CTRL` + :kbd:`Numpad0` restablece el nivel de zoom.

La herramienta de lupa también se puede utilizar para crear una imagen en un área ampliada.

.. image:: /images/observation/magnifier.png

Relación de aspecto de la imagen
------------------
Para cambiar la relación de aspecto de la imagen utilice los menús debajo :menuselection:`Imagen --> Formato de imagen`.

Algunos dispositivos utilizan píxeles no rectangulares y no completan el valor de relación de aspecto de píxeles correspondiente en los metadatos del archivo.
En estos casos, podría ser necesario forzar la relación de aspecto a un valor conocido.

Están disponibles las siguientes opciones:

- :guilabel:`Auto detección`
- :guilabel:`Forzar 4:3`
- :guilabel:`Forzar 16:9`

Desentrelazado
-------------
Para desentrelazar el vídeo utilice el menú :menuselection:`Imagen --> Desentrelazar`.

Algunos dispositivos de captura almacenan vídeo en formato entrelazado.
Los vídeos entrelazados almacenan la mitad de las imágenes al doble de velocidad de fotogramas, alternando filas pares e impares.
Esto provoca un artefacto de peinado cuando el movimiento filmado es rápido cuando los objetos o sujetos se mueven durante el intervalo de medio fotograma.

El algoritmo de desentrelazado reconstruye imágenes completas combinando filas de fotogramas adyacentes.

.. image:: /images/observation/deinterlacing.png

Debayering
----------
Los vídeos guardados en modo Bayer contienen los datos sin procesar del sensor antes de la reconstrucción del color.
El color se puede reconstruir usando el menú debajo :menuselection:`Imagen --> Mosaico de Bayer`.

.. image:: /images/observation/debayering.png

Están disponibles las siguientes opciones:

- :guilabel:`RGGB`
- :guilabel:`BGGR`
- :guilabel:`GRBG`
- :guilabel:`GBRG`

La opción apropiada para seleccionar depende del dispositivo y modo utilizado durante la grabación.
