%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
    Manual de referencia de Kinovea
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

Bienvenido al manual para `Kinovea <https://www.kinovea.org>`__.

Kinovea es una herramienta de anotación de video diseñada para el análisis del movimiento.
Cuenta con utilidades para capturar, ralentizar, comparar, anotar y medir el movimiento en videos.

Para obtener una descripción general de una sola página de las funciones de Kinovea, puede consultar la `página de características en el sitio web. <https://www.kinovea.org/features.html>`__ 

.. tip:: 
    Este manual puede ser utilizado sin conexión: `descargue el manual (comprimido en Zip) <Kinovea-Manual-0.9.5.zip>`__.

Las secciones a continuación y la tabla de contenido en la barra lateral deberían permitirle acceder a la documentación de su tema de interés.
También puede utilizar la función de búsqueda en la esquina superior izquierda.

    .. container:: tocdescr

        .. container:: descr

            .. figure:: /images/home/userinterface.jpg
                :target: userinterface/index.html

            :doc:`/userinterface/index`
                Descripción de la ventana principal, los espacios de trabajo y las páginas de preferencias.

        .. container:: descr

            .. figure:: /images/home/observation.jpg
                :target: observation/index.html

            :doc:`/observation/index` 
                Funciones para controlar el tiempo de video, el aspecto de la imagen y sincronizar dos videos.

        .. container:: descr

            .. figure:: /images/home/annotation.png
                :target: annotation/index.html

            :doc:`/annotation/index`
                Herramientas para anotar videos con dibujos, texto, resaltar momentos clave y usar referencias de postura.

        .. container:: descr

            .. figure:: /images/home/measurement.png
                :target: measurement/index.html

            :doc:`/measurement/index`
                Funciones para calibrar espacio y tiempo, medir intervalos, posiciones, distancias, ángulos y seguir cinemáticas.
                
        .. container:: descr

            .. figure:: /images/home/capture.jpg
                :target: capture/index.html

            :doc:`/capture/index`
                Subsistema para capturar, retardar y grabar cámaras en vivo.

        .. container:: descr

            .. figure:: /images/home/export.png
                :target: export/index.html

            :doc:`/export/index`
                Funciones para guardar videos y medidas para otras aplicaciones.

        .. container:: descr

            :doc:`/misc/index`
                Diversos temas relacionados con el control programático de Kinovea e información general sobre el proyecto.


Este manual es mantenido por voluntarios.
Si encuentra algo que es confuso, incorrecto o necesita ser editado, háganoslo saber
`aqui <https://github.com/Kinovea/kinovea-docs/issues>`__.


.. toctree::
    :titlesonly:
    :hidden:
    :caption: Interfaz de usuario

    userinterface/overview
    userinterface/workspaces
    userinterface/instances
    userinterface/preferences

.. toctree::
    :titlesonly:
    :hidden:
    :caption: Observación y comparación

    observation/loading
    observation/playback_ui
    observation/image_geometry
    observation/time_calibration
    observation/comparison
    observation/overview
    observation/reverse

.. toctree::
    :titlesonly:
    :hidden:
    :caption: Anotación

    annotation/general
    annotation/tools
    annotation/style_and_opacity
    annotation/time_origin
    annotation/importing_images
    annotation/annotation_files
    annotation/importing_data

.. toctree::
    :titlesonly:
    :hidden:
    :caption: Medición

    measurement/calibration
    measurement/guidelines
    measurement/coordinatesystem
    measurement/lensdistortion
    measurement/time
    measurement/distance
    measurement/angle
    measurement/trajectory
    measurement/tracking
    measurement/kinematics
    
.. toctree::
    :titlesonly:
    :hidden:
    :caption: Captura

    capture/listing
    capture/userinterface
    capture/hardware
    capture/livedelay
    capture/recording
    capture/replay

.. toctree::
    :titlesonly:
    :hidden:
    :caption: Exportación
    
    export/video
    export/data
    
.. toctree::
    :titlesonly:
    :hidden:
    :caption: Temas variados

    misc/faq
    misc/update
    misc/command_line
    misc/copydata
    misc/comms

