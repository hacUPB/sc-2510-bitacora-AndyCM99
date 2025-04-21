
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
  
  La aplicación comienza con un fondo negro y un color de partículas blanco.

  Cuando el usuario mueve el mouse, se almacenan las posiciones en un vector y se dibujan círculos en esas posiciones.

  Si hay más de 100 partículas, se elimina la más antigua para evitar que el vector crezca indefinidamente.

  Cuando el usuario hace clic, el color de las partículas cambia a un color aleatorio.
  

- ¿Qué hace la función mouseMoved?

  Guarda la posición del mouse en el vector particles.

  Si hay más de 100 elementos en el vector, borra el primero (el más antiguo) para mantener el tamaño controlado.

Esto crea un efecto de "trazo" que sigue al cursor.
- ¿Qué hace la función mousePressed?

  Cambia el color de las partículas a un color aleatorio cuando se hace clic en la pantalla.
  
- ¿Qué hace la función setup?

  Cambia el color de las partículas a un color aleatorio cuando se hace clic en la pantalla.

- ¿Qué hace la función update?

 En este caso, no hace nada. Pero en una aplicación más compleja, aquí se actualizaría la lógica del programa.
 
- ¿Qué hace la función draw?

  Dibuja todas las partículas almacenadas en el vector particles como círculos de radio 50.

  Usa ofSetColor(particleColor) para que todas las partículas sean del mismo color.

## Actividad 3

cambie el color del fondo y el radio de cada bola, como ? 

modifique esta parte del codigo  

![image](https://github.com/user-attachments/assets/2994a9ab-1565-490c-bda1-31f2813c82a5)

el fondo 
```
ofBackground(200); //que antges era 0

```

y el radio 

```
 ofDrawCircle(pos.x, pos.y, 100); // que antes era 50

```

## Actividad 5 y 6

le agregue esta parte al codigo en el ofapp.ccp


```
void ofApp::mouseReleased(int x, int y, int button) {
    if (button == OF_MOUSE_BUTTON_LEFT) {
        selectedSphere = nullptr;
    }
}
```
y en of app.h agregue esto 
```
void mouseReleased(int x, int y, int button); 

```


Como corregir el error?
Agrega una función mouseReleased para que cuando sueltes el clic, la esfera deje de seguir el mouse.

Al final del archivo se agrega.

Cuando haces clic dentro de una esfera (mousePressed), la asigna como selectedSphere.

Mientras se mantiene ese puntero, en update la esfera se mueve con el mouse.

Cuando sueltas el botón del mouse (mouseReleased), se borra la selección, y la esfera ya no se mueve más.


- ¿Cuál es la definición de un puntero?
  
  Un puntero en C++ es una variable que almacena la dirección de memoria de otro dato u objeto.

  Es decir, en lugar de guardar directamente un objeto o número, guarda dónde está ubicado en la memoria.


- ¿Dónde está el puntero?
  
  vector<Sphere*> spheres;   // ← vector que guarda punteros a esferas
  
  Sphere* selectedSphere;    // ← puntero a una esfera "seleccionada"

- ¿Cómo se inicializa el puntero?

  Se inicializa con new, que crea el objeto dinámicamente en memoria y devuelve la dirección donde está:
  
  spheres.push_back(new Sphere(x, y, radius));
  
  Esto crea una nueva Sphere y guarda su dirección en el vector spheres
- ¿Para qué se está usando el puntero?

  vector<Sphere*> spheres: Guarda la dirección de muchas esferas. Es como una lista de referencias a objetos que tú creaste con new.

  selectedSphere: Se usa para guardar la esfera actual que estás moviendo con el mouse. Así sabes cuál debe seguir al cursor.

- ¿Qué es exactamente lo que está almacenado en el puntero?

  Un puntero no guarda el objeto en sí, sino su dirección en memoria.

  Sphere* selectedSphere;

  Aquí, selectedSphere guarda algo como una dirección, no la esfera completa. Para usar el objeto, se hace:

  selectedSphere->update(x, y);

  Esto quiere decir:

  “Ve a la dirección guardada en selectedSphere y actualiza el objeto que está ahí.”

  Pregunta | Respuesta breve
 ¿Qué es un puntero? | Variable que guarda una dirección de memoria de otro dato u objeto.
 ¿Dónde están los punteros? | En spheres (vector de punteros) y selectedSphere.
 ¿Cómo se inicializan? | Con new Sphere(...) o asignando otro puntero existente (selectedSphere = ...)
 ¿Para qué se usan? | Para manipular esferas dinámicas y seleccionar una para moverla.
 ¿Qué guarda un puntero? | La dirección de memoria donde vive el objeto real (Sphere).

## Actividad 7

inicialmente uso el codigo que se proporciona 

¿Qué hace el código originalmente? (cuando usas el stack)

¿Qué pasa?

Se crea una esfera local dentro de la función createObjectInStack. Como es local, vive en el stack.

Guardas un puntero a esa esfera en el globalVector.

Cuando termina la función, la variable localSphere desaparece porque el stack la elimina automáticamente.

El vector sigue teniendo un puntero que apunta a una zona de memoria que ya fue liberada. 

Luego, al dibujar o acceder a esa esfera, estás accediendo a basura, y pueden pasar cosas como:

La app se traba o se cierra.

Los valores son raros o aleatorios.

Se ve todo en negro o nada se dibuja.

¿Qué pasa cuando lo haces bien, usando el heap?

void ofApp::createObjectInStack() {
    Sphere* heapSphere = new Sphere(...);      // ← 1. Crea una esfera en el heap
    globalVector.push_back(heapSphere);        // ← 2. Guarda su dirección en el vector
}

¿Qué pasa?
Se crea una esfera dinámicamente en el heap.

Esa memoria no se borra automáticamente cuando termina la función.

Guardas el puntero en el vector.

Más tarde, cuando usas sphere->draw() en draw(), ¡el objeto sigue existiendo! 🎉

Puedes usarlo, moverlo, dibujarlo… todo sin errores.

Acción                    |                  Stack              |             Heap

¿Quién lo gestiona?       | El sistema, automáticamente         | Tú (debes usar new y delete)

¿Cuánto vive la variable? | Solo dentro de la función           | Hasta que tú la borres

¿Riesgo de fallos?        | Sí, si accedes después de que muera | No, si la gestionas bien

¿Más rápido?              | Sí                                  | Un poco más lento

## Actividad 8



