
# Unidad 3 

Trabajaremos en nuevo lenguaje en C++ 
de que se trata?  Se trata de openframeworks.

OpenFrameworks es un conjunto de herramientas de código abierto diseñado para facilitar el desarrollo de proyectos 
creativos e interactivos, como instalaciones multimedia, arte generativo, visualizaciones, y más. Está basado en C++
y proporciona una serie de bibliotecas que permiten trabajar con gráficos 2D y 3D, sonido, video, interfaces de usuario,
sensores y dispositivos, entre otros.

La idea de OpenFrameworks es simplificar el proceso de creación de aplicaciones visuales e interactivas, brindando 
una plataforma robusta que los artistas, diseñadores y programadores puedan usar para desarrollar proyectos sin
necesidad de escribir código demasiado complejo. Es muy popular entre la comunidad de arte digital, diseño interactivo,
y entre aquellos interesados en el "media art".

Algunas de las características clave de OpenFrameworks incluyen:

Interacción en tiempo real: Soporte para trabajar con datos en vivo, como cámaras, micrófonos, sensores,
y otros dispositivos.

Compatibilidad multiplataforma: Se puede usar en Windows, macOS y Linux.

Bibliotecas y extensiones: Hay muchas bibliotecas adicionales que permiten integrar OpenFrameworks con otros
sistemas y tecnologías como Arduino, OpenCV, y OSC.

Comunidad activa: Una comunidad global que contribuye constantemente con nuevos ejemplos, tutoriales
y actualizaciones.

# Actividad 1

Se pide descargar un generador de proyectos de OpenFrameworks, instalarlo en C:/ y hacer un pequeño test,
que consiste en una pequeña modificación al archivo ofApp.cpp.

Pero primero quieria entender que hace la< funcion draw del codigo que tneemos en ofApp.cpp

### Función especial: draw()
La función draw() es clave en cualquier aplicación gráfica, ya que es la encargada de renderizar en pantalla todo
lo que deseas mostrar. Es invocada repetidamente en un ciclo para asegurar que la pantalla se actualice constantemente 
(generalmente a 60 fotogramas por segundo o más).

#### ofSetColor(255):

Establece el color para el siguiente dibujo. El valor 255 es blanco (en una escala de 0 a 255 para cada componente 
de color RGB). Esto asegura que cualquier cosa que se dibuje a continuación será de color blanco.

#### ofDrawCircle(ofGetMouseX(), ofGetMouseY(), 20):

Dibuja un círculo en las coordenadas actuales del ratón. ofGetMouseX() y ofGetMouseY() obtienen la posición del ratón
en la ventana, y el 20 es el radio del círculo (20 píxeles). El círculo se dibuja en la posición donde el ratón se
encuentra en ese momento, y se actualizará constantemente mientras mueves el ratón.

Esto hace que el programa dibuje un círculo blanco en la pantalla en la posición del ratón en todo momento, 
creando una interacción visual.

## Actividad 2 

se pide tener el proyecto generado por el generador 

ahora 
se pide realizar una modificacion al archvo 0fApp.cpp

```

#pragma once

#include "ofMain.h"

class ofApp : public ofBaseApp{

    public:
        void setup();
        void update();
        void draw();

        void mouseMoved(int x, int y );
        void mousePressed(int x, int y, int button);

    private:

        vector<ofVec2f> particles;
        ofColor particleColor;

};


```


![7eb0b73a-f5de-46f6-a9ba-4aad3102a53e](https://github.com/user-attachments/assets/8b69ffe7-98af-4be5-9360-f3d91b2fc511)

se realizaron diferentes cambios al archivo opApp.cpp y ofApp.h


- ¿Qué fue lo que incluimos en el archivo .h?
  Variables para almacenar las partículas:

  vector<ofVec2f> particles: Se añade un vector de partículas para almacenar las posiciones de las partículas. ofVec2f es
  una clase de OpenFrameworks que almacena un punto en 2D (coordenadas x, y). Esta variable es clave para almacenar las
  partículas que irás creando cuando el ratón se mueva.

  Color de las partículas:
  
  ofColor particleColor: Se añade esta variable para manejar el color de las partículas. ofColor es una clase de
  OpenFrameworks que representa un color en el espacio RGB.
  
- ¿Cómo funciona la aplicación?
  La aplicación que estás construyendo con OpenFrameworks tiene como objetivo mostrar partículas en la pantalla, las cuales son creadas y
  manipuladas por la interacción del ratón. A continuación, te voy a explicar cómo funciona la aplicación que hemos creado paso a paso,
  basándome en el código que has proporcionado hasta ahora.

  

- ¿Qué hace la función mouseMoved?
- ¿Qué hace la función mousePressed?
- ¿Qué hace la función setup?
- ¿Qué hace la función update?
- ¿Qué hace la función draw?



