
Calibración de tiempo
================

Velocidad de fotogramas de captura
------------------
Cuando se captura un vídeo con una cámara de alta velocidad (o usando la función de cámara lenta o alta velocidad de un teléfono inteligente),
El archivo de vídeo generado suele tener una velocidad de fotogramas diferente de la velocidad de fotogramas de captura.
Por ejemplo, un vídeo filmado a 1000 fps se puede guardar en un archivo con una velocidad de fotogramas de reproducción más típica de 25 fps.

En este caso, el vídeo se reproducirá más lento que en tiempo real, lo cual es de esperar.
pero la información y los cálculos relacionados con el tiempo serían erróneos si se basaran en la velocidad de fotogramas de reproducción.

Para trabajar con este tipo de vídeo es importante configurar (o "calibrar") la escala de tiempo.
Esto se hace yendo a :menuselection:`Herramientas --> Calibración del tiempo` y llenando la velocidad de fotogramas de captura.

.. image:: /images/observation/captureframerate.png

Cambiar esta opción no cambia la velocidad nominal a la que se reproduce el vídeo.
En otras palabras, configurar el control de velocidad en su punto medio seguirá reproduciendo el vídeo a la misma velocidad de cámara lenta que antes.
En cambio, esta opción cambia las coordenadas temporales de las imágenes.

Velocidad de fotogramas de reproducción rota
--------------------------
En algunos casos, un vídeo se guarda con una velocidad de fotogramas que simplemente es incorrecta o Kinovea no puede leerlo.
Por ejemplo, una cámara USB podría afirmar que está capturando vídeo a 25 fps, pero la transmisión de vídeo en realidad se transfiere a 15 fps.

En este caso, el vídeo se reproducirá a una velocidad incorrecta y la calibración del tiempo será incorrecta.
Si conoce la velocidad de cuadros de reproducción real a la que se supone que se reproducirá el video, puede ingresarla en :menuselection:`Herramientas --> Calibración del tiempo`.

.. image:: /images/observation/brokenframerate.png

Cambiar esta opción cambia la velocidad nominal a la que se reproduce el vídeo.

