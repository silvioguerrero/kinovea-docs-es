
Interfaz de usuario de la pantalla de reproducción
==============================

La pantalla de reproducción está dividida en las siguientes áreas:

.. image:: /images/observation/ui-playback.png

1. Ventana gráfica de imagen
-----------------
La ventana de visualización de imágenes es el área principal donde se reproduce el vídeo.

Al hacer doble clic en la imagen, se maximiza en el área de la ventana gráfica.
Los tiradores en las cuatro esquinas de la imagen se pueden utilizar para cambiar su tamaño.

2. Infobar (barra de información)
----------

La barra de información contiene el nombre del archivo, el tamaño de la imagen y la velocidad de fotogramas.

Se puede hacer clic en el nombre del archivo para acceder a un menú contextual para cambiar entre el modo de vídeo normal y el modo de observador de carpeta de reproducción.

.. image:: /images/capture/menuobserver.png


3. Barra de herramientas de dibujos
-------------------
La barra de herramientas de dibujos contiene botones para crear nuevas imágenes clave, seleccionar la herramienta activa y abrir el perfil de color.

.. image:: /images/observation/toolbar.png

La barra de herramientas contiene más herramientas que las inmediatamente visibles.
Los botones que albergan herramientas adicionales tienen un pequeño triángulo negro en la esquina superior izquierda.
Se puede acceder a las herramientas adicionales haciendo clic derecho o manteniendo presionado el botón principal.

.. image:: /images/observation/subtools.png

4. Área de la zona de trabajo
--------------------
La zona de trabajo define el segmento del vídeo con el que está trabajando el reproductor.
El cabezal de reproducción gira dentro de la zona de trabajo.

.. image:: /images/observation/workingzone.png

|TimeOrigin| Marca la hora actual como origen de la hora. Esto hace que los valores de tiempo sean relativos a este momento.

|WZLock| Bloquea el punto de inicio y fin de la zona de trabajo para evitar cambiarlos por error.

|WZStart| Establece el punto de inicio de la zona de trabajo dentro del vídeo.

|WZEnd| Establece el punto final de la zona de trabajo dentro del vídeo.

|WZReset| Restablece la zona de trabajo a todo el vídeo.

.. |TimeOrigin| image:: /images/observation/icons/timeorigin.png
.. |WZLock| image:: /images/observation/icons/wz_lock.png
.. |WZStart| image:: /images/observation/icons/wz_left.png
.. |WZEnd| image:: /images/observation/icons/wz_right.png
.. |WZReset| image:: /images/observation/icons/wz_reset.png

También puede actualizar los límites de la zona de trabajo manipulando directamente los puntos finales azules.

.. tip:: Si la cantidad de datos cabe en la memoria caché, la zona de trabajo se cargará en la memoria.

    Esto mejora el rendimiento de la reproducción y permite la selección de menú: `Video --> Descripción general` and :menuselection:`Video --> Inverso` menús.
    La memoria caché se puede configurar en :menuselection:`Opciones --> Preferencias --> Lectura --> Memoria`.

5. Área de línea de tiempo
----------------
El área de la línea de tiempo muestra la posición actual dentro del vídeo, los marcadores de tiempo y el control de velocidad.

.. image:: /images/observation/timeline.png

Marcadores de tiempo
**************************
Los marcadores de tiempo son rectángulos de colores dentro del margen de la línea de tiempo y proporcionan información sobre las anotaciones.
Utilizan el siguiente código de colores:

- Rojo: el origen del tiempo.
- Verde: una imagen clave.
- Azul: un cronómetro.
- Púrpura: una trayectoria.

Control de velocidad
*************

El control deslizante de velocidad va de 0 al doble de la velocidad nominal del vídeo.

El valor de velocidad mostrado tiene en cuenta el factor de cámara lenta configurado de manera que la velocidad se muestra como un porcentaje de la velocidad de acción en el mundo real.
Por ejemplo, si un vídeo se filma a 240 fps y se guarda en un archivo a 24 fps, el vídeo normalmente se reproducirá al 10% de la velocidad real. 
En este caso el control de velocidad irá del 0 al 20% con un punto medio en el 10%.

.. warning:: Si el vídeo no se puede reproducir a su velocidad nominal por motivos de rendimiento, el valor de la velocidad de reproducción se reducirá automáticamente.

    El rendimiento de la reproducción depende del tamaño de la imagen mostrada, la velocidad de fotogramas y el formato del archivo.

6. Controles de reproducción
--------------------

.. image:: /images/observation/playbackcontrols.png

De izquierda a derecha, los botones proporcionan las siguientes funciones:

- Regresa al inicio del vídeo o zona de trabajo.
- Retrocede un fotograma.
- Inicia la reproducción.
- Avanza un fotograma.
- Va al final del vídeo o zona de trabajo.

La reproducción regresa al inicio cuando llega al final del video o zona de trabajo.

Navegación
**********

También es posible moverse en el vídeo usando los siguientes atajos:

- Utilice la **rueda del mouse** para avanzar y retroceder.
- Utilice :kbd:`←` y :kbd:`→` teclas de flecha del teclado para moverse cuadro por cuadro.
- Utilice :kbd:`↟` (Page up) y :kbd:`↡` Teclas (Av Pág) para saltar un 10% hacia adelante.
- Utilice :kbd:`⇱` (Home) and :kbd:`⇲` Teclas (Fin) para saltar al inicio y al final.

 
7. Controles de exportación
------------------
Los controles de exportación brindan formas de exportar videos e imágenes del archivo actual.

.. image:: /images/observation/exportcontrols.png

Ver también: :doc:`/export/video`.

8. Menú contextual
---------------
El menú contextual proporciona acceso rápido a más funciones.

.. image:: /images/observation/contextmenu.png


