
Reproducción
========


General
-------
.. image:: /images/preferences/playback_general.png

Importar secuencias de imágenes como videos
********************************

Cuando esta opción está habilitada y se abre un archivo de imagen, Kinovea intentará detectar una **secuencia de imágenes** buscando números consecutivos en el nombre de otros archivos de la misma carpeta.
Si se detecta una secuencia de imágenes, todos los archivos de imágenes se cargarán automáticamente y toda la colección se interpretará como un video.

Ejemplo de nombres de archivos interpretados como una secuencia:

- image_001.png, image_002.png, image_003.png, etc.
- test01.jpg, test02.jpg, test03.jpg, etc.

Los números pueden estar en cualquier parte del nombre del archivo. 
Aparte de los números, el resto del nombre debe ser idéntico para todos los archivos.
La cantidad de ceros iniciales en el esquema de numeración debe ser consistente entre todos los archivos de la secuencia.

Un hueco o un cambio en el sistema de numeración se interpretará como el final de la secuencia.
La detección es bidireccional: se puede usar cualquier archivo para cargar la secuencia, el video resultante siempre comenzará en el archivo con el número más bajo encontrado.

Controles deslizantes de velocidad de enlace al comparar videos
****************************************

Cuando se marca esta opción y se comparan dos videos, cambiar la velocidad de reproducción en un reproductor cambiará automáticamente la velocidad de reproducción en el otro reproductor para que coincida.

.. note:: La velocidad de reproducción se empareja de acuerdo con la velocidad en tiempo real, teniendo en cuenta las diferencias en la velocidad de fotogramas del archivo de video y :doc:`capture framerate <../../observation/time_calibration>`.
   Si un video está en cámara lenta y el otro está a velocidad normal, esta opción aún debería funcionar como se espera, siempre que la velocidad de fotogramas de captura del video en cámara lenta esté configurada correctamente. 

Actualizar imagen durante el movimiento del cursor de tiempo
****************************************

Cuando esta opción no está marcada, la visualización del video se pausará al mover manualmente el cursor de la línea de tiempo.

Relación de aspecto predeterminada
********************

Esta opción define la relación de aspecto de imagen predeterminada configurada cada vez que se abre un archivo de video. Es lo mismo que configurar manualmente el menú :menuselection:`Image --> Image format`.

Las siguientes opciones están disponibles:

- :guilabel:`Auto detección`
- :guilabel:`Forzar 4:3`
- :guilabel:`Forzar 16:9`

La opción :guilabel:`Auto detección` utiliza el tamaño de la imagen y la relación de aspecto de píxeles encontrada en los metadatos del archivo de video para calcular la altura de la imagen. 
Las otras opciones cambiarán la altura del video para que coincida con una relación de aspecto de 4:3 o 16:9.

Siempre desentrelazar al abrir un nuevo video
*******************************************

Esta opción obliga a habilitar el mecanismo de desentrelazado para todos los archivos abiertos. Es lo mismo que configurar manualmente el menú :menuselection:`Image --> Deinterlace`.


Archivo de anotaciones predeterminado
************************

Esta opción le permite apuntar a un archivo .KVA que contiene anotaciones de video que se cargarán automáticamente cuando se abra cualquier video.

Todavía se pueden cargar otros archivos de anotaciones sobre el video usando el método de archivo sidecar o a través del menú :menuselection:`File --> Load annotations`. Se fusionarán entre sí.

Vea también: :doc:`/annotation/annotation_files`.


Memory
------
.. image:: /images/preferences/playback_memory.png

Memoria caché asignada a cada pantalla de reproducción
**********************************************

La memoria caché se utiliza para cargar el contenido de video en la memoria del sistema y acelerar la navegación.
Cuando la sección de video activa (zona de trabajo) quepa en la memoria caché, se cargará automáticamente en esta caché. Si la sección de video no cabe en el caché, la memoria no se consumirá.

Cuando se usa la comparación lado a lado, cada pantalla de reproducción puede usar como máximo la mitad de la cantidad de memoria configurada.

En el caso de varias instancias de Kinovea, cada instancia tiene su propia memoria caché.


Unidades
-----
.. image:: /images/preferences/playback_units.png

.. tip:: La unidad de longitud se define durante el proceso de calibración.


Tiempo
****
Esta opción controla el formato de toda la información relacionada con el tiempo que se muestra en el programa [#f1]_. Se utiliza en la posición y duración de la línea de tiempo, en cronómetros y relojes, y en archivos exportados.

Las siguientes opciones están disponibles:

================================    ==============   =========================
Formato                               Ejemplo         Descripción
================================    ==============   =========================
[h:][mm:]ss.xx[x]                   1:10.48           Código de tiempo textual.
Número de cuadro                    1762              Rango del cuadro actual.
Milisegundos totales                70480             Número entero de milisegundos.
Microsegundos totales               1284              Número entero de microsegundos.
Diez milésimas de hora              904               Diez milésimas de hora
Centésima de minuto                 542               Centésima de minuto
[h:][mm:]ss.xx[x] + N° de cuadro    1:10.48 (1762)    
================================    ==============   =========================

Al usar el código de tiempo textual si la velocidad de fotogramas en tiempo real es superior a 100 fps, se muestran las milésimas de segundo. Las horas y los minutos solo se muestran cuando es necesario.

.. note:: El tiempo comienza en el **origen del tiempo**. El origen de tiempo se puede configurar para que esté en cualquier parte del video.
   Las ubicaciones de video anteriores al origen de la hora se muestran como números negativos.
   Si el origen del tiempo no se define manualmente, el origen del tiempo se establece automáticamente al inicio de la sección de video actual.

Velocidad
*****

La unidad de velocidad se utiliza en la herramienta de trayectoria y en la :guilabel:`Cinemática lineal` ventana al configurar la opción de visualización de la medición en :guilabel:`Velocidad`, :guilabel:`Velocidad horizontal` or :guilabel:`Velocidad vertical`.
También se usa en la ventana Cinemática angular cuando se usa la velocidad tangencial.

Las siguientes opciones están disponibles:

================================   ============= 
Unidad                               Simbolo
================================   =============
Metros por segundo                  m/s
Kilometros por hora                 km/h
Pies por segundo                    ft/s
Millas por hora                     mph
================================   =============

.. note:: Si no se ha realizado ninguna calibración espacial, la unidad de velocidad será automáticamente **píxeles por segundo (px/s)**.

Aceleración
************

La unidad de aceleración se utiliza en la herramienta de trayectoria y en la ventana :guilabel:`Cinemática lineal` al configurar la opción de visualización de medidas en :guilabel:`Aceleración`, :guilabel:`Aceleración horizontal` o :guilabel:`Aceleración vertical` .
También se utiliza en la ventana :guilabel:`Cinemática angular` al utilizar :guilabel:`Aceleración tangencial`, :guilabel:`Aceleración centrípeta` o :guilabel:`Aceleración resultante`.

Las siguientes opciones están disponibles:

================================   ============= 
Unidad                             Simbolo
================================   =============
Metros por segundos al cuadrado     m/s²
Pies por segundos al cuadrado       ft/s²
================================   =============

.. note:: Si no se ha realizado ninguna calibración espacial, la unidad de aceleración será automáticamente **píxeles por segundo al cuadrado (px/s²)**.

Ángulo
*****

La unidad de ángulo se utiliza en las herramientas de medida de ángulos y en la ventana :guilabel:`Cinemática angular` al configurar la opción de fuente de datos en :guilabel:`Ángulo` o :guilabel:`Desplazamiento total`.

Las siguientes opciones están disponibles:

================================   ============= 
Unidad                             Simbolo
================================   =============
Grados                              °
Radianes                            rad
================================   =============

Velocidad angular
****************

La unidad para la velocidad angular se utiliza en la ventana :guilabel:`Cinemática angular` al establecer la opción de fuente de datos en :guilabel:`Velocidad angular`.

Las siguientes opciones están disponibles:

================================   ============= 
Unidad                             Simbolo
================================   =============
Grados por segundo                  deg/s
Radianes por segundo                rad/s
Revoluciones por minuto             rpm
================================   =============


Aceleración angular
********************

La unidad para la aceleración angular se utiliza en la ventana :guilabel:`Cinemática angular` al establecer la fuente de datos en :guilabel:`Aceleración angular`.

Las siguientes opciones están disponibles:

==================================   ============= 
Unidad                               Simbolo
==================================   =============
Grados por segundos al cuadrado         deg/s²
Radianes por segundos al cuadrado       rad/s²
==================================   =============


Unidad de longitud personalizada
******************

Esta opción define el nombre y el símbolo de una unidad de longitud adicional.
Las unidades de longitud incorporadas son: milímetros, centímetros, metros, pulgadas, pies y yardas.

Esta unidad de longitud personalizada aparecerá en la parte inferior del menú desplegable de unidades de longitud en los cuadros de diálogo de calibración espacial.

El factor de escala entre píxeles y esta unidad se define durante el proceso de calibración de la misma manera que para otras unidades de longitud.

.. figure:: /images/preferences/playback_units_custom.png
   :align: center
   
   Uso de la unidad de longitud personalizada para agregar micrómetros a la lista de unidades de longitud integradas.


.. rubric:: Notas

.. [#f1] Con la excepción del eje de tiempo en los diálogos de análisis cinemático. En estos cuadros de diálogo, el tiempo siempre se muestra numéricamente, ya sea en milisegundos o normalizado.










