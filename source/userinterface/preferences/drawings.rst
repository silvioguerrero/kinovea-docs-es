
Dibujos
========

General
-------
.. image:: /images/preferences/drawings_general.png

Mostrar dibujos cuando se reproduce el video
***********************************

Esta opción controla si los dibujos son visibles o no cuando el video está en reproducción continua.  

Habilitar filtrado de coordenadas
****************************

Esta opción controla el filtrado de coordenadas espaciales para trayectorias y dibujos rastreados.
Debido al proceso de digitalización, las coordenadas sin procesar son ruidosas y las cantidades resultantes, especialmente las derivadas como la velocidad y la aceleración, son menos precisas de lo que podrían ser.
El filtrado cuidadoso de las coordenadas elimina gran parte de este ruido y proporciona mediciones más precisas.

Puede desmarcar esta opción si prefiere exportar las coordenadas sin procesar y realizar el filtrado usted mismo.

.. tip:: Para obtener información más detallada sobre el enfoque de filtrado exacto y los algoritmos utilizados, consulte la página "Acerca de" de la ventana "Cinemática lineal".


Habilitar el modo de depuración de herramientas personalizadas
******************************

Cuando esta casilla de verificación está marcada, las herramientas personalizadas mostrarán información adicional sobre el nombre y las relaciones de puntos, puntos de control y segmentos.
Los autores de herramientas pueden utilizar esta opción para facilitar el diseño.

See also: :doc:`/annotation/tools`.


Opacidad
-------
.. image:: /images/preferences/drawings_opacity.png

Las opciones de esta pestaña controlan la visibilidad predeterminada de los dibujos. Estos se pueden personalizar de forma independiente trayendo su menú contextual y seleccionando opciones en los submenús de Visibilidad.

En el caso más general, la visibilidad de un dibujo a lo largo del tiempo sigue el siguiente patrón:

.. image:: /images/preferences/opacity.png


Visible para todo el video
****************************

Cuando esta opción está marcada, los nuevos dibujos son visibles para la totalidad del video. Las opciones de duración opaca y duración de desvanecimiento se ignoran.

Máxima opacidad
***************

Esta opción controla la opacidad utilizada durante la sección opaca.
Un valor del 100% significa que el dibujo no permitirá que se vea el fondo.
Un valor inferior al 100% significa que el dibujo tendrá cierto grado de transparencia.


Duración de la opcacidad
***************

Esta opción controla cuánto tiempo permanece el dibujo en su nivel máximo de opacidad antes de desaparecer. Esta sección comienza en el fotograma clave en el que se agregó el dibujo.

Duración del desvanecimiento
***************

Esta opción controla la duración de las rampas antes y después de la opacidad máxima, hasta que el dibujo se vuelve completamente invisible.


Seguimiento
--------
.. image:: /images/preferences/drawings_tracking.png

Las opciones de esta página controlan los parámetros predeterminados para las trayectorias y el seguimiento del dibujo.
Las trayectorias también se pueden configurar de forma independiente trayendo su menú contextual y accediendo a su ventana de configuración.
Los parámetros de seguimiento de otros dibujos no se pueden modificar después de la creación.

Ventana de objetos
*************
El tamaño de la ventana del objeto define el tamaño del parche de imagen alrededor del punto rastreado que se busca en otros marcos.
Esto debe establecerse para que sea lo más pequeño posible para evitar incluir el fondo en el parche rastreado.

Ventana de búsqueda
*************
El tamaño de la ventana de búsqueda define el área en la que se busca el punto.
Esto debería ser lo suficientemente grande para compensar el cambio de posición del objeto de un cuadro al siguiente.
Sin embargo, la ventana de búsqueda demasiado grande puede hacer que el algoritmo de seguimiento seleccione un objeto diferente en otra parte de la imagen, si este objeto se parece al objeto rastreado.

.. tip:: Utilice el cuadro de diálogo de configuración de la herramienta de trayectoria para determinar visualmente el tamaño adecuado del objeto y las ventanas de búsqueda.
