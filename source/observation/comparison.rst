Comparación y sincronización
==============================

Comparación
----------
Se pueden abrir dos vídeos uno al lado del otro usando el botón :guilabel:`Dos pantallas de reproducción` o el menú :menuselection:`Vista --> Dos pantallas de reproducción`.

El cursor de la línea de tiempo en cada pantalla de reproducción se puede mover de forma independiente.

.. image:: /images/observation/compare-desync.png

Mecanismo de sincronización
-------------------------
Se pueden sincronizar dos videos configurando su origen temporal en un evento común visible en ambos videos.
Cuando los vídeos estén sincronizados pasarán por su origen temporal al mismo tiempo.

Para establecer el origen del tiempo en un video, muévase a ese punto del video y haga clic en el botón 
:guilabel:`Marcar tiempo actual como origen de tiempo` o haga clic derecho en el fondo del vídeo y elija el menú :menuselection:`Marcar tiempo actual como origen de tiempo`.
Alternativamente, puedes mover cada video al punto correcto de forma independiente y usar el botón :guilabel:`Sincronizar videos en los fotogramas actuales` en el área de controles conjuntos.

.. image:: /images/observation/compare-syncpoint.png

Durante la reproducción conjunta, el mecanismo de sincronización significa que un vídeo puede comenzar y/o finalizar la reproducción antes que el otro.

Para realizar una navegación conjunta cuadro por cuadro, mueva el cursor en la línea de tiempo conjunta o utilice los botones de control conjunto.

.. image:: /images/observation/compare-synched.png

Controles conjuntos
--------------
.. image:: /images/observation/joint-controls.png

Los controles de reproducción son los mismos que para las pantallas de reproducción individuales pero actúan en ambos vídeos al mismo tiempo.

Los demás botones tienen las siguientes funciones:

- |JointOrigin| Establezca el origen del tiempo en ambos videos en su respectiva hora actual.
- |Merge| Habilite o deshabilite la superposición de los videos entre sí.
- |Swap| Cambie las pantallas de reproducción.

.. |JointOrigin| image:: /images/observation/icons/jointorigin.png
.. |Merge| image:: /images/observation/icons/syncmerge.png
.. |Swap| image:: /images/observation/icons/swap.png

Controles de velocidad vinculados
---------------------
De forma predeterminada, los controles de velocidad en cada pantalla de reproducción están vinculados entre sí:
Bajar la velocidad de reproducción en un video la reduce en el otro.

Los controles de velocidad son independientes de la velocidad de fotogramas de los archivos de vídeo, por lo que
esto debería aplicar un factor de cámara lenta similar a ambos videos y mantener la comparación significativa.

.. tip:: Si uno de los videos fue capturado con una cámara de alta velocidad y tiene una velocidad de fotogramas de captura diferente,
    esta velocidad de fotogramas debe configurarse para este vídeo a través del menú. :menuselection:`Herramientas --> Configuración de la velocidad de video`.
    Una vez realizada esta configuración, ambos controles seguirán siendo coherentes entre sí.

Si está seguro de que no desea que los controles deslizantes de velocidad estén vinculados, puede cambiar la opción en :menuselection:`Opciones --> Preferencias --> Lectura --> General --> Controles deslizantes de velocidad de enlace al comparar videos`.

Superposición
-------------
La superposición pinta cada video encima del otro con un 50% de opacidad.
Este es un mecanismo básico para comparar el movimiento in situ si los videos se filmaron en el mismo entorno con una cámara estática.

.. image:: /images/observation/merge.png




