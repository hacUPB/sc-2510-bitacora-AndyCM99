# Experiencia de aprendizaje 2: Lenguaje Ensamblador

## Actividad 1

## ¿Qué es la entrada-salida mapeada a memoria?
Imagina que la memoria de la computadora es como un gran tablero de notas adhesivas. Cada nota tiene una dirección única, como "Calle Memoria 1234". Normalmente, estas notas se usan para almacenar datos o instrucciones. Pero, ¿qué pasa si algunas de esas notas no son para almacenar datos, sino para comunicarse con dispositivos como el teclado o la pantalla? Eso es exactamente lo que hace la entrada-salida mapeada a memoria.

En lugar de tener un sistema separado para hablar con el teclado o la pantalla, la computadora usa direcciones de memoria especiales. Por ejemplo:

Si quiero saber qué tecla se presionó, lees una "nota" específica (una dirección de memoria) que está conectada al teclado.

Si quiero dibujar algo en la pantalla, escribes en un bloque de "notas" (direcciones de memoria) que controlan los píxeles de la pantalla.

Es como si, en lugar de llamar por teléfono al teclado o a la pantalla, simplemente dejaras un mensaje en su buzón de memoria. ¡Simple y eficiente!

### ¿Cómo se implementa en la plataforma Hack?
En la computadora Hack, esto funciona así:

#### El teclado: 
Cuando presionas una tecla, el código ASCII de esa tecla (un número que representa el carácter) se guarda en una dirección de memoria específica, digamos 0x6000. Si no hay ninguna tecla presionada, esa dirección tendrá el valor 0.

#### La pantalla: 
La pantalla está dividida en píxeles, y cada píxel se controla escribiendo en un bloque de memoria que va desde 0x4000 hasta 0x5FFF. Cada bit en este bloque controla si un píxel está encendido (1) o apagado (0).

#### En resumen, en Hack:

Leer del teclado: Miras la dirección 0x6000.

Escribir en la pantalla: Modificas las direcciones entre 0x4000 y 0x5FFF.

Un programa sencillo usando Memory-Mapped I/O
Vamos a crear un programa super simple que haga esto:

Espera a que presiones una tecla.

Muestra el carácter de esa tecla en la pantalla.


```
// Programa: Mostrar la tecla presionada en la pantalla

    @0x6000       // Dirección del teclado
    D=M           // Lee la tecla presionada (su código ASCII)

    @0x4000       // Dirección de la pantalla (primer píxel)
    M=D           // Escribe el código ASCII en la pantalla

(END)
    @END          // Bucle infinito para que el programa no termine
    0;JMP
```

#### ¿Cómo funciona esto en el simulador?
Vamos a simular este programa paso a paso, como si estuviéramos jugando con la computadora Hack:

#### Cargar el programa: 
Abres el simulador de Hack y pegas el código anterior. Es como preparar la computadora para ejecutar tu programa.

#### Ejecutar el programa: 
Le das al botón de "ejecutar". El programa empieza a correr y queda esperando a que hagas algo.

#### Presionar una tecla: 
Imagina que presionas la letra "A" en el teclado virtual del simulador. El código ASCII de "A" (que es 65) se guarda automáticamente en la dirección 0x6000.

#### Mostrar en pantalla: 
El programa lee ese valor (65) y lo escribe en la dirección 0x4000, que controla el primer píxel de la pantalla. Como resultado, verás la letra "A" aparecer en la esquina superior izquierda de la pantalla.

Bucle infinito: El programa entra en un bucle infinito, lo que significa que seguirá mostrando la última tecla que presionaste hasta que decidas detenerlo.

¿Por qué es útil esto?
Este sistema es muy práctico porque:

##### Simplifica el hardware: 
No necesitas circuitos especiales para manejar el teclado o la pantalla.

#### Es fácil de programar: 
Solo necesitas leer o escribir en direcciones de memoria, algo que ya sabes hacer.

#### Es flexible: 
Puedes agregar más dispositivos simplemente mapeándolos a nuevas direcciones de memoria.

### En resumen
La entrada-salida mapeada a memoria es como usar el mismo sistema de notas adhesivas para almacenar datos y comunicarte con dispositivos. En la plataforma Hack, esto te permite interactuar con el teclado y la pantalla de una manera sencilla y elegante. El programa que escribimos es un ejemplo básico, pero ¡las posibilidades son infinitas! Puedes crear cosas más complejas, como juegos o aplicaciones, usando este mismo principio.

## Actividad 2

