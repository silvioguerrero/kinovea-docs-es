
Ejecutando múltiples instancias de Kinovea
=====================================

Es posible ejecutar múltiples Kinovea al mismo tiempo en la misma computadora. 
Esto se puede usar para grabar más de dos cámaras, reproducir más de dos videos al mismo tiempo o crear configuraciones más avanzadas para captura y reproducción o escenarios de instrumentación.


.. note:: De forma predeterminada, cada instancia tiene su propio conjunto de preferencias separadas de las demás.
    Este comportamiento está controlado por la opción bajo :menuselection:`Preferences --> General --> Instances have their own preferences`.
    Esta opción solo se puede cambiar desde la primera instancia de Kinovea.

Nombre de instancia
--------------
A cada instancia se le asigna un número en orden secuencial de lanzamiento y, de forma predeterminada, este número se convierte en el nombre de la instancia.

El nombre de la instancia se puede ver en la barra de título de la ventana entre corchetes.

.. image:: /images/ui/instancename2.png

Es posible personalizar el nombre de las instancias pasando el nuevo nombre en el :guilabel:`-name` argumento en la línea de comando.

.. code-block:: consola

    kinovea.exe -name "MiInstancia"

.. image:: /images/ui/instancenamecustom.png

Vea también: :doc:`/misc/command_line`.

.. tip:: Los argumentos de la línea de comandos también se pueden especificar creando un acceso directo de Windows en Kinovea.exe y editando el :guilabel:`Target` campo en las propiedades del acceso directo.



