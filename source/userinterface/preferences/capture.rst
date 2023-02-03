
Captura
=======

General
-------
.. image:: /images/preferences/capture_general.png

Grabar video sin comprimir
*************************
Cuando esta opción está marcada, el video se graba sin comprimir primero los cuadros de video a JPEG.
Cuando esta opción no está marcada, los cuadros de video se comprimen a JPEG utilizando configuraciones de alta calidad para conservar la fidelidad.

Esta opción se puede utilizar para minimizar los fotogramas perdidos, intercambiando espacio por velocidad (debido a la configuración de JPEG utilizada, la calidad de la imagen no debería verse muy afectada por esta opción).
Cuando se utiliza un medio de almacenamiento rápido, puede ser más rápido almacenar las imágenes grandes sin comprimir en comparación con el tiempo que lleva comprimirlas.

Para instantáneas de imágenes, la compresión depende del formato de archivo.

.. note:: Cuando se configuran las cámaras para usar secuencias MJPEG, esta opción se ignora. Las transmisiones MJPEG siempre se guardan tal cual en su formato de contenedor.

.. note:: Al configurar las cámaras para usar imágenes de patrón Bayer sin procesar, debe habilitar esta opción para poder reconstruir la información de color en el momento de la reproducción.

.. warning:: No todos los reproductores de video pueden reproducir archivos sin comprimir.


Mostrar velocidad de fotogramas
*****************
Esta opción define la frecuencia con la que se actualizan las imágenes de la cámara en la pantalla de captura.

Mientras se graba, los recursos de la computadora se comparten entre mostrar el flujo de la cámara y grabarlo en el medio de almacenamiento.
La prioridad más alta siempre se le da a la grabación, pero reducir este valor puede ayudar a reducir la carga general en la computadora y mejorar el rendimiento de la grabación.

Formato de imagen
************
Esta opción define el formato de imagen predeterminado utilizado al guardar instantáneas.

Están disponibles los siguientes formatos de imagen:

- :guilabel:`JPG`
- :guilabel:`PNG`
- :guilabel:`BMP`


Formato de video
************
Esta opción define el formato de contenedor de video predeterminado que se usa al grabar videos comprimidos. Todos los videos están comprimidos usando un códec MJPEG.

Están disponibles los siguientes formatos de contenedor:

- :guilabel:`MP4`
- :guilabel:`AVI`
- :guilabel:`MKV`

Formato de video sin comprimir
*************************
Esta opción define el formato de contenedor de video predeterminado que se usa al grabar videos sin comprimir.

Están disponibles los siguientes formatos de contenedor:

- :guilabel:`MKV`
- :guilabel:`AVI`


Archivo de anotaciones predeterminado
************************
Esta opción le permite apuntar a un archivo .KVA que contiene anotaciones que se cargarán automáticamente cuando se abra cualquier flujo de cámara.

Todavía se pueden cargar otros archivos de anotaciones en la parte superior de la transmisión de la cámara usando el menú :menuselection:`Archivo --> Cargar anotaciones`. Se fusionarán entre sí.

See also: :doc:`/annotation/annotation_files`.

Memoria
------
.. image:: /images/preferences/capture_memory.png

Memoria asignada para búferes de retardo
**********************************

Esta opción controla la cantidad de memoria utilizada para recordar fotogramas antiguos, en el contexto de la vista retrasada de la transmisión de la cámara.
Por extensión, esta opción define el retardo máximo configurable en la pantalla de captura. El retraso máximo se basa en el tamaño de la imagen, el formato de la imagen y la velocidad de fotogramas de captura.

Cuando se usan dos capturas de pantalla al mismo tiempo, cada pantalla usa la mitad de la cantidad de memoria configurada.

En el caso de varias instancias de Kinovea, cada instancia tiene su propia memoria de búfer de retardo.

.. warning:: A diferencia de la memoria caché en la pantalla de reproducción, esta cantidad de memoria siempre se asigna y utiliza tan pronto como se abre una pantalla de captura.

Grabación
---------
.. image:: /images/preferences/capture_recording.png

Modo de grabación y retardo
************************

La opción de modo de grabación define cómo el subsistema de grabación interactúa con el búfer de retardo para crear el video de salida.

Cuando la cámara transmite un nuevo cuadro, siempre se coloca en el búfer de retardo y el subsistema de grabación siempre toma cuadros del búfer de retardo para crear el vídeo de salida.


Camara
^^^^^^
Cuando se utiliza este modo de grabación, se ignora el valor de retardo establecido en la pantalla de captura.

La grabación se realiza sobre la marcha, el cuadro guardado es siempre el cuadro más reciente enviado por la cámara.

.. tip:: Si no necesita la grabación de imágenes retrasadas, esta opción puede resultar en un rendimiento ligeramente mejor que el método Retrasado.

Retrasado
^^^^^^^
Cuando se utiliza este modo de grabación, se tiene en cuenta el valor de retardo establecido en la pantalla de captura.

La grabación se realiza sobre la marcha, el cuadro guardado se toma del búfer de retraso en función del valor de retraso.

Esto se puede usar para registrar acciones que suceden antes del momento en que se presiona o activa el botón de grabación.

Retroactivo
^^^^^^^^^^^
Cuando se utiliza este modo de grabación, la grabación no se realiza sobre la marcha.
En cambio, al final del proceso de grabación, al hacer clic en el botón de detener la grabación o cuando se alcanza la duración máxima de la grabación, la transmisión de la cámara se detiene, el búfer de demora se congela y el archivo de video se crea todo a la vez.

El valor de retardo se tiene en cuenta para crear la grabación.

Este modo ofrece los mejores rendimientos de grabación y minimiza los cuadros perdidos, a costa de una duración máxima reducida para los videos creados y una congelación temporal de la transmisión de la cámara.

.. tip:: La duración máxima de los videos grabados con este modo de grabación depende del tamaño del búfer de demora. Esto se puede configurar desde la página de preferencias de memoria.

Cámaras de alta velocidad
******************
Las opciones de este grupo le permiten modificar la velocidad de fotogramas escrita en los metadatos del archivo de salida.
Esto influye en la cantidad de recursos necesarios para reproducir el archivo y la velocidad aparente de la acción.

Una cámara puede ser capaz de producir y transmitir 1000 fotogramas por segundo, pero la computadora no podrá reproducir el archivo a esa velocidad y el monitor tampoco podrá actualizarse lo suficientemente rápido.
Para evitar este problema, es habitual reducir la velocidad de fotogramas del archivo de salida a una más típica. Los dispositivos de grabación normalmente aplican esta transformación automáticamente. Esto da como resultado un video que parece estar en cámara lenta.


Umbral de reemplazo de velocidad de fotogramas
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Esta opción controla la velocidad de fotogramas a partir de la cual se modifica el archivo de salida para utilizar uno más bajo.

Si la cámara está configurada para enviar imágenes a una velocidad de fotogramas superior a este valor, la velocidad de fotogramas real almacenada en los metadatos del archivo será la velocidad de fotogramas de reemplazo.
Si la cámara está configurada para enviar imágenes a una velocidad de fotogramas inferior a este valor, no se producirá ningún cambio.

Velocidad de fotogramas de reemplazo
^^^^^^^^^^^^^^^^^^^^^
Este valor define la velocidad de fotogramas final escrita en los metadatos del archivo cuando la velocidad de fotogramas configurada en la cámara está por encima del umbral.

Nombre de la imagen
------------
.. image:: /images/preferences/capture_imagenaming.png

Las opciones de esta página le permiten configurar el sistema de nombres automatizado para instantáneas de imágenes de la transmisión de la cámara.

La ruta final y el nombre del archivo se crean concatenando los valores :guilabel:`Raíz`, :guilabel:`Subdirectorio` and :guilabel:`Archivo`. 
Cada campo puede contener macros especiales que hacen referencia a variables de contexto que se insertan automáticamente en la ruta final.

Si no se utiliza ninguna variable de contexto, el sistema de nombres de archivos preparará la siguiente grabación incrementando automáticamente un contador y agregando un número al nombre del archivo.

Si el valor calculado da como resultado el mismo nombre que un archivo existente, la pantalla de captura solicitará una confirmación de sobrescritura.

Para ver la lista de variables de contexto disponibles, haga clic en el botón :guilabel:`%` al lado de :guilabel:`Subdirectorio` o del campo de :guilabel:`Archivo`.

Están disponibles las siguientes variables de contexto:

===========   ============= 
Macro           Description
===========   =============
%year          El año actual
%month         El mes actual como un número del 01 a 12.
%day           El día actual del mes desde 01 a 31.
%hour          La hora actual de 00 a 23.
%minute        El minuto actual de 00 a 59.
%second        El segundo actual de 00 a 59.
%date          La fecha actual en el formato "YYYYMMDD".
%time          La hora actual en el formato "HHMMSS".
%datetime      La fecha y hora actual como "YYYYMMDD-HHMMSS".
%camalias      El alias de la cámara.
%camfps        La velocidad de fotogramas configurada para la cámara.
%recvfps       La velocidad de fotogramas real recibida de la cámara.
%%             Esto se reemplaza por una cadena vacía.
===========   =============

Cualquier cosa que no sea exactamente parte de una macro se copia literalmente en la salida.
Algunos ejemplos asumiendo que la fecha y hora actual es octubre 20, 1968 a las 16:00:00 (4 PM):

.. code-block::

    %year-%month-%day: 1968-10-20.
    %hour-%minute-%second: 16-00-00.
    %datetime: 19681020-160000
    %date_text: 19681020_text
    %date-%camalias: 19681020-mycamcorder
    

.. note:: Si desea utilizar un nombre de archivo completamente estático y omitir el incremento automático del contador para grabaciones consecutivas, utilice el macro variable :guilabel:`%%`. 
    Tenga en cuenta que esto requerirá que ingrese el nombre de archivo manualmente para cada grabación o sobrescriba un archivo existente.


Nombramiento de videos
------------
.. image:: /images/preferences/capture_videonaming.png

Las opciones de esta página le permiten configurar el sistema de nombres automatizado para las grabaciones de video de las secuencias de las cámaras.

Las opciones son similares a las de Nomenclatura de imágenes.

.. warning:: Evite usar la unidad del sistema de Windows como destino para la grabación de la cámara para minimizar el acceso simultáneo y el uso compartido de recursos.

.. tip:: Para mejorar el rendimiento en escenarios de grabación dual, utilice dos medios de almacenamiento físico diferentes para las cámaras izquierda y derecha.

Automation
----------
.. image:: /images/preferences/capture_automation.png

Disparador de audio
*************

Habilitar disparador de audio
^^^^^^^^^^^^^^^^^^^^
Cuando esta opción está marcada, Kinovea mide el nivel de volumen en el micrófono y activa el inicio de la grabación cuando este volumen supera el umbral configurado.

.. note:: El mecanismo de disparo de audio se puede desactivar para cámaras individuales desde los controles de la pantalla de captura.

Dispositivo de entrada
^^^^^^^^^^^^
Esta opción le permite seleccionar qué micrófono se utiliza para activar las grabaciones.

.. tip:: Asegúrese de que Kinovea pueda acceder a su micrófono abriendo :guilabel:`Configuración de sonido de Windows`, yendo a :guilabel:`Configuración de privacidad del micrófono` y encendiendo :guilabel:`Permita que las aplicaciones accedan a su micrófono`.

Trigger threshold
^^^^^^^^^^^^^^^^^
The trigger threshold defines the volume level required to trigger recordings. 
You should see the black line moving laterally as the microphone picks up sounds. The vertical red line represents the trigger level.

The counter on the right is incremented each time the trigger is reached and reset when the threshold value is changed. 
You can use this to get immediate feedback while figuring out the appropriate configuration.

Idle time
^^^^^^^^^^^^

The idle time defines the amount of time after each recording during which the audio trigger is automatically disarmed.


Stop recording by duration
**************************
This option defines the maximum duration for recordings. 
Recordings started manually or by audio trigger will be stopped right after they reach this duration. 
Setting the value to 0 disables the option and requires manually stopping the recording process.

This option is orthogonal to delayed recording. 
For example if the camera is configured with a 2-second delay and the maximum duration is set to 5 seconds, the created video will last 5 seconds as configured: 
the first 2 seconds are actions that happened before the recording trigger and the last 3 seconds are actions that happened after the recording trigger.

In combination with the audio trigger this option lets you record multiple sequences without manually interacting with the computer.

.. note:: This value is a lower bound, the final video might be slightly longer than configured due to internal processing and alignment with frame boundaries.

Post recording command
**********************
This option lets you set up a program that will be run at the end of every recording. This can be used to automatically copy the file to a different location, perform compression or apply post-processing.

The command line can contain special macros referring to context variables that are automatically inserted in the final command.

The following context variables are available:

===========   ============= 
Macro           Description
===========   =============
%directory     The directory where the recording was saved.
%filename      The name of the recorded file.
===========   =============

Ignore file overwrite warning
*****************************
This option bypasses the overwrite confirmation dialog when the recording about to start points to an existing file. If the option is checked the existing file is irremediably deleted and overwritten by the new one.

This option can be used if you are limited in space and do not need to save all sequences. 
In this scenario you can continuously record to a single file and manually copy it to a different location only when you really want to keep it.
