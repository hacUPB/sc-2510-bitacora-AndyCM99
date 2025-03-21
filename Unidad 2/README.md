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

#### Aquí está el código en ensamblador de Hack:

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

## Actividad 2 y 3 

Como respuesta a la pregunta 20 del reto, parece ser que no comprendí la instrucción, así que 
realicé todo completo. Es decir, que en la 20 mi respuesta ilustra la figura de la 18, solo
que al soltar la tecla se borra la ilustración del bitmap

## Actividad 4 

```
(draw)
    // Verifica si la tecla "D" está presionada
    @KBD
    D=M
    @68
    D=D-A
    @DRAW
    D;JEQ

    // Verifica si la tecla "E" está presionada
    @KBD
    D=M
    @69
    D=D-A
    @CLEAR
    D;JEQ

    // Si no es "D" ni "E", no hacer nada
    @END
    0;JMP

(DRAW)
    // Dibuja un patrón en la pantalla (filas 6 a 26)
    @SCREEN
    D=A
    @R12
    AD=D+M
    @15390
    D=D+A
    A=D-A
    M=D-A
    // Fila 7
    D=A
    @32
    AD=D+A
    @15390
    D=D+A
    A=D-A
    M=D-A
    // Fila 8
    D=A
    @32
    AD=D+A
    @15390
    D=D+A
    A=D-A
    M=D-A
    // Fila 9
    D=A
    @32
    AD=D+A
    @15390
    D=D+A
    A=D-A
    M=D-A
    // Fila 10
    D=A
    @32
    AD=D+A
    @15390
    D=D+A
    A=D-A
    M=D-A
    // Fila 11
    D=A
    @32
    AD=D+A
    @15390
    D=D+A
    A=D-A
    M=D-A
    // Fila 12
    D=A
    @32
    AD=D+A
    @15390
    D=D+A
    A=D-A
    M=D-A
    // Fila 13
    D=A
    @32
    AD=D+A
    @15390
    D=D+A
    A=D-A
    M=D-A
    // Fila 14
    D=A
    @32
    AD=D+A
    @15390
    D=D+A
    A=D-A
    M=D-A
    // Fila 15
    D=A
    @31
    AD=D+A
    @31744
    D=D+A
    A=D-A
    M=D-A
    AD=A+1
    @32767
    A=!A
    D=D+A
    A=D-A
    M=D-A
    AD=A+1
    @15
    D=D+A
    A=D-A
    M=D-A
    // Fila 16
    D=A
    @30
    AD=D+A
    @31744
    D=D+A
    A=D-A
    M=D-A
    AD=A+1
    @32767
    A=!A
    D=D+A
    A=D-A
    M=D-A
    AD=A+1
    @15
    D=D+A
    A=D-A
    M=D-A
    // Fila 17
    D=A
    @30
    AD=D+A
    @14336
    D=D+A
    A=D-A
    M=D-A
    AD=A+1
    M=0
    AD=A+1
    @7
    D=D+A
    A=D-A
    M=D-A
    // Fila 18
    D=A
    @30
    AD=D+A
    @14336
    D=D+A
    A=D-A
    M=D-A
    AD=A+1
    M=0
    AD=A+1
    @7
    D=D+A
    A=D-A
    M=D-A
    // Fila 19
    D=A
    @30
    AD=D+A
    @14336
    D=D+A
    A=D-A
    M=D-A
    AD=A+1
    M=0
    AD=A+1
    @7
    D=D+A
    A=D-A
    M=D-A
    // Fila 20
    D=A
    @30
    AD=D+A
    @14336
    D=D+A
    A=D-A
    M=D-A
    AD=A+1
    M=0
    AD=A+1
    @7
    D=D+A
    A=D-A
    M=D-A
    // Fila 21
    D=A
    @30
    AD=D+A
    @2048
    D=D+A
    A=D-A
    M=A-D
    AD=A+1
    M=-1
    AD=A+1
    @7
    D=D+A
    A=D-A
    M=D-A
    // Fila 22
    D=A
    @30
    AD=D+A
    @2048
    D=D+A
    A=D-A
    M=A-D
    AD=A+1
    M=-1
    AD=A+1
    @7
    D=D+A
    A=D-A
    M=D-A
    // Fila 23
    D=A
    @30
    AD=D+A
    @2048
    D=D+A
    A=D-A
    M=A-D
    AD=A+1
    M=-1
    AD=A+1
    @7
    D=D+A
    A=D-A
    M=D-A
    // Fila 24
    D=A
    @30
    AD=D+A
    M=0
    AD=A+1
    M=0
    AD=A+1
    M=0
    // Fila 25
    D=A
    @30
    AD=D+A
    M=0
    AD=A+1
    M=0
    AD=A+1
    M=0
    // Fila 26
    D=A
    @30
    AD=D+A
    M=0
    AD=A+1
    M=0
    AD=A+1
    M=0
    @END
    0;JMP

(CLEAR)
    // Borra la pantalla (escribe 0 en todas las filas)
    @SCREEN
    D=A
    @R12
    AD=D+M
    // Fila 6
    M=0
    @32
    AD=D+A
    // Fila 7
    M=0
    @32
    AD=D+A
    // Fila 8
    M=0
    @32
    AD=D+A
    // Fila 9
    M=0
    @32
    AD=D+A
    // Fila 10
    M=0
    @32
    AD=D+A
    // Fila 11
    M=0
    @32
    AD=D+A
    // Fila 12
    M=0
    @32
    AD=D+A
    // Fila 13
    M=0
    @32
    AD=D+A
    // Fila 14
    M=0
    @32
    AD=D+A
    // Fila 15
    M=0
    @31
    AD=D+A
    M=0
    AD=A+1
    M=0
    AD=A+1
    M=0
    // Fila 16
    @30
    AD=D+A
    M=0
    AD=A+1
    M=0
    AD=A+1
    M=0
    // Fila 17
    @30
    AD=D+A
    M=0
    AD=A+1
    M=0
    AD=A+1
    M=0
    // Fila 18
    @30
    AD=D+A
    M=0
    AD=A+1
    M=0
    AD=A+1
    M=0
    // Fila 19
    @30
    AD=D+A
    M=0
    AD=A+1
    M=0
    AD=A+1
    M=0
    // Fila 20
    @30
    AD=D+A
    M=0
    AD=A+1
    M=0
    AD=A+1
    M=0
    // Fila 21
    @30
    AD=D+A
    M=0
    AD=A+1
    M=0
    AD=A+1
    M=0
    // Fila 22
    @30
    AD=D+A
    M=0
    AD=A+1
    M=0
    AD=A+1
    M=0
    // Fila 23
    @30
    AD=D+A
    M=0
    AD=A+1
    M=0
    AD=A+1
    M=0
    // Fila 24
    @30
    AD=D+A
    M=0
    AD=A+1
    M=0
    AD=A+1
    M=0
    // Fila 25
    @30
    AD=D+A
    M=0
    AD=A+1
    M=0
    AD=A+1
    M=0
    // Fila 26
    @30
    AD=D+A
    M=0
    AD=A+1
    M=0
    AD=A+1
    M=0
    @END
    0;JMP

(END)
    // Retorna al programa principal
    @R13
    A=M
    D;JMP


```

si se presiona "E", el programa salta a la etiqueta CLEAR para borrar la pantalla.
Además, si no se presiona ni "D" ni "E", el programa salta a END sin hacer nada. 
Esto permite borrar la pantalla solo al presionar "E"

# Reto 

## 1

para este punto me base en un codigo que tenemos en el libro 

![image](https://github.com/user-attachments/assets/807aa089-d972-4f7d-884a-b709a4bafa82)

```
// Inicialización de variables
@i      // Carga la dirección de la variable i
M=1     // i = 1
@sum    // Carga la dirección de la variable sum
M=0     // sum = 0

(LOOP)
    // Condición del bucle (i <= 100)
    @i
    D=M     // D = i
    @100
    D=D-A   // D = i - 100
    @END
    D;JGT   // Si i > 100, salta a END

    // sum += i
    @i
    D=M     // D = i
    @sum
    M=D+M   // sum = sum + i

    // i++
    @i
    M=M+1   // i = i + 1

    // Repetir el bucle
    @LOOP
    0;JMP

(END)
    // Fin del programa
    @END
    0;JMP
 
```

al cual le pedi a chat gtp que le agregara unas anotaciones para facilitar su comprencion, 

¿Cómo están implementadas las variables i y sum?

tenemos que recordar que las variables estan representadas por direcciones de la memoria ram 

como lo Testeamos? 

![image](https://github.com/user-attachments/assets/f3e6689c-ec54-404b-8b5a-3f5bbf11251d)

el programa recorrio 100 veces su ciclo sumando iteradas veces hasta lograr el valor esperado 

1 y 2¿Cómo están implementadas las variables i y sum? y ¿En qué direcciones de memoria están estas variables?

Las variables i y sum se implementan como posiciones de memoria. En ensamblador,
 no hay variables como en los lenguajes de alto nivel, sino que se usan direcciones 
de memoria para almacenar valores, como se ve en la foto, se guardan apartir de la ranura 16.

3 ¿Cómo está implementado el ciclo while?

El ciclo while se implementa con una etiqueta (LOOP) y un salto condicional D;JGT.
El programa verifica si i <= 100 y, si es verdadero, ejecuta el cuerpo del ciclo.

4 ¿Cómo se implementa la variable i?

La variable i se implementa como una posición de memoria (@i).
Su valor se actualiza en cada iteración del ciclo con M=M+1.

5 ¿En qué parte de la memoria se almacena la variable i?

La variable i se almacena en una dirección de memoria asignada por el ensamblador 
(por ejemplo, la dirección 16).

6 Después de todo lo que has hecho, ¿Qué es entonces una variable?

Una variable es una posición de memoria que almacena un valor. En ensamblador, 
no hay nombres de variables como en los lenguajes de alto nivel, sino direcciones de memoria.

¿Qué es la dirección de una variable?

La dirección de una variable es la ubicación en memoria donde se almacena su valor. 
Por ejemplo, @i representa la dirección de la variable i.

¿Qué es el contenido de una variable?

El contenido de una variable es el valor almacenado en su dirección de memoria.
Por ejemplo, si i está en la dirección 16, su contenido sería 1 al inicio del programa.

## 2



```

int sum = 0;
for (int i = 1; i <= 100; i++) {
    sum += i;
}

```
le pedi ayuda a chat gtp ene ste punto, para cambair el while por for, 
pero podmeos entender facilmente como es su cambio 
podemos ver que el contador inicia dentro del bucle for, y el condicional int i = 1 esta incluida dentro del mismo 
le da un aspecto mas ordenado y corto y la suma se çhace automaticamente al final de cada ciclo, segun entiendo, es mejor 
usar un ciclo for cuando el ciclo depende de un contador 


## 3



```
// Inicialización de variables
@sum    // Carga la dirección de la variable sum
M=0     // sum = 0
@i      // Carga la dirección de la variable i
M=1     // i = 1

(FOR)
    // Condición del for (i <= 100)
    @i
    D=M     // D = i
    @100
    D=D-A   // D = i - 100
    @END
    D;JGT   // Si i > 100, salta a END

    // sum += i
    @i
    D=M     // D = i
    @sum
    M=D+M   // sum = sum + i

    // i++
    @i
    M=M+1   // i = i + 1

    // Repetir el bucle
    @FOR
    0;JMP

(END)
    // Fin del programa
    @END
    0;JMP


```
aqui hice unja prueva con el mismo 

![image](https://github.com/user-attachments/assets/87f93f45-b01e-4e3c-97f3-18277104c1bb)

tiene unja diferencia importante, y es que primero se suma el valor de i a sum y luego se incrementa i
Este orden es crucial para obtener el resultado correcto. Si se hiciera al revés el cálculo de la suma
sería incorrecto.



## 4 


```

int a = 10;  // Declara una variable 'a' y le asigna el valor 10.
int *p;      // Declara un puntero 'p' que puede apuntar a una variable de tipo int.
p = &a;      // Asigna la dirección de memoria de 'a' al puntero 'p'.
*p = 20;     // Cambia el valor de 'a' a 20 a través del puntero 'p'.


```


## 5 

En ensamblador no explican como tal que exista algo como un puntero pero si tenemos las direcciones de la memoria 
que pues pienso que las podmeos usar de la misma manera, indicandole connde esta guardado un dato en concreto


```
// Declara una variable 'a' y le asigna el valor 10.
@10         // Carga el valor 10 en el registro A.
D=A         // Guarda el valor 10 en el registro D.
@a          // Carga la dirección de la variable 'a' en el registro A.
M=D         // Almacena el valor 10 en la dirección de 'a'.

// Declara un puntero 'p' y le asigna la dirección de 'a'.
@a          // Carga la dirección de 'a' en el registro A.
D=A         // Guarda la dirección de 'a' en el registro D.
@p          // Carga la dirección de 'p' en el registro A.
M=D         // Almacena la dirección de 'a' en 'p'.

// Cambia el valor de 'a' a 20 a través del puntero 'p'.
@20         // Carga el valor 20 en el registro A.
D=A         // Guarda el valor 20 en el registro D.
@p          // Carga la dirección de 'p' en el registro A.
A=M         // Carga la dirección almacenada en 'p' (la dirección de 'a') en el registro A.
M=D         // Almacena el valor 20 en la dirección de 'a'.

```

![image](https://github.com/user-attachments/assets/55a4494f-ef6a-40ec-937f-bcf9d6b906ec)

realice una prueba de como funciona dicho codigo, pues vemos que las bariables como @a y @p se comvierten en direcciones de la ram 
las 16 y 17 las cuales como sabemos son destinadas al uso de variables y los usa para direccionar un valor, que en este caso es 10 inicialmete 
que esta guardo en una ranura de la ram, y que le pedimos que con la ayuda de un p que sirve de puntero con la direccion de ese 10, vaya i busque ese 10
para cambiarlo por un 20, asi sobrescribiendo por asi decirlo el dato 




## 7 
```


// Declara una variable 'a' y le asigna el valor 10.
@10         // Carga el valor 10 en el registro A.
D=A         // Guarda el valor 10 en el registro D.
@a          // Carga la dirección de la variable 'a' en el registro A.
M=D         // Almacena el valor 10 en la dirección de 'a'.

// Declara una variable 'b' y le asigna el valor 5.
@5          // Carga el valor 5 en el registro A.
D=A         // Guarda el valor 5 en el registro D.
@b          // Carga la dirección de la variable 'b' en el registro A.
M=D         // Almacena el valor 5 en la dirección de 'b'.

// Declara un puntero 'p' y le asigna la dirección de 'a'.
@a          // Carga la dirección de 'a' en el registro A.
D=A         // Guarda la dirección de 'a' en el registro D.
@p          // Carga la dirección de 'p' en el registro A.
M=D         // Almacena la dirección de 'a' en 'p'.

// Asigna el valor de 'a' a 'b' a través del puntero 'p'.
@p          // Carga la dirección de 'p' en el registro A.
A=M         // Carga la dirección almacenada en 'p' (la dirección de 'a') en el registro A.
D=M         // Guarda el valor almacenado en la dirección de 'a' en el registro D.
@b          // Carga la dirección de 'b' en el registro A.
M=D         // Almacena el valor de D (10) en la dirección de 'b'.

```

Como lo vimos en el ejercicio 5, es lo mismo: declaramos dos variables que se guardan en las ranuras 16 y 17 de la RAM, 
como es la regla en la lógica de este emulador. Luego, declaramos una variable p que toma la dirección de la primera 
variable guardada en @16 y la guarda en la ranura 18 de la RAM. Para finalizar, tomamos esa variable p, que guarda 
la dirección, y hacemos que tome lo que hay en esa dirección y lo cargue en b.


![image](https://github.com/user-attachments/assets/8438fc8d-99c8-40d9-bca0-abdf7bbcdcb0)



## 8

1. int *pvar;
Explicación: Esta línea declara un puntero llamado pvar que apunta a un valor de tipo int.

Qué hace:

int * indica que pvar es un puntero a un entero (int).

pvar es una variable que almacenará la dirección de memoria de un valor de tipo int.

En este momento, pvar no está inicializado, por lo que apunta a una dirección de memoria no definida (puede ser basura o NULL si se inicializa explícitamente).

2. pvar = var;
Explicación: Esta línea asigna el valor de var al puntero pvar.

Qué hace:

Aquí, var debe ser una variable de tipo int o una expresión que devuelva un valor de tipo int.

Sin embargo, esta línea no es válida en C/C++ porque pvar es un puntero (almacena direcciones de memoria), y var es un valor entero. No puedes asignar un valor entero directamente a un puntero.

Si quisieras asignar la dirección de memoria de var a pvar, deberías usar el operador de dirección &

3. var2 = *pvar;
Explicación: Esta línea asigna el valor apuntado por pvar a la variable var2.

Qué hace:

*pvar es el operador de desreferenciación, que accede al valor almacenado en la dirección de memoria a la que apunta pvar.

Si pvar apunta a un valor de tipo int, entonces *pvar devuelve ese valor.

var2 debe ser una variable de tipo int para almacenar el valor desreferenciado.

4. pvar = &var3;
Explicación: Esta línea asigna la dirección de memoria de la variable var3 al puntero pvar.

Qué hace:

&var3 es el operador de dirección, que devuelve la dirección de memoria donde está almacenada la variable var3.

pvar ahora apunta a la dirección de memoria de var3.

Si var3 es de tipo int, entonces pvar puede almacenar su dirección porque pvar es un puntero a int.



## 9



```

// Programa principal (main)
(main)
    // Declarar variables
    @6        // Cargar el valor 6 en D
    D=A
    @a        // Guardar en la variable a
    M=D

    @9        // Cargar el valor 9 en D
    D=A
    @b        // Guardar en la variable b
    M=D

    // Llamar a la función suma
    @suma     // Saltar a la etiqueta suma
    0;JMP

(suma)
    // Cargar el valor de a en D
    @a
    D=M

    // Cargar el valor de b y sumarlo a D
    @b
    D=D+M

    // Guardar el resultado en c
    @c
    M=D

    // Regresar a main
    @main_after_suma
    0;JMP

(main_after_suma)
    // Finalizar el proceso
    @END
    0;JMP

(END)
    @END      // Bucle infinito para terminar
    0;JMP
```

la idea es tratar de emuolar el comportamiento de el codigo que se nos mostro en c, que pasa o mejor dicho que tenemos 
primero tenemos una etiqueta mainq ue declara las variables  a y b las guarda en la ram, declaramos un salto 0;jmp que le pide al codigo continuar en la etiqueda suma declarada 
busque lo que hay guardado en a es decir @16 y @17 los suma y guarda el resultado en @18 para finalizar con un nuevo salto para cerrar el bucle en una funcion main secundaria 

lo verificamos en la consola de naan2tetris  


![image](https://github.com/user-attachments/assets/9562c78b-8aae-4580-a12b-f14c8f482561)

como vemos al final se quda en un bucle infinito en las ultimas dos lineas mostrando como un fin al proceso ejecutando satisfactoriamente la suma 
