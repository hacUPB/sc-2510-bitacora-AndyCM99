# Sistemas Computacionales.

## Experiencia de aprendizaje 1: Arquitectura del computador.
### La semana pasada comenzamos el curso realizando un análisis detallado de lo que es un computador y cómo funcionan sus componentes. 
   Utilizamos varias herramientas que nos ayudaron a comprender mejor su funcionamiento, lo que nos permitió obtener una visión más 
   clara sobre el rol de cada parte en el proceso general de la computación.

### Nos planteamos dos preguntas para comenzar con el análisis:

####  ¿Cómo funciona un computador digital moderno? Y ¿cómo hace este para ejecutar un programa?
Bueno, si lo viéramos desde el punto de vista de un programador en ensamblador, un computador moderno funciona como un sistema 
de procesamiento que maneja instrucciones a nivel de bits. La CPU es la unidad que ejecuta estas instrucciones, las cuales están 
codificadas en lenguaje de máquina (esencialmente 0s y 1s). Los registros de la CPU son pequeños espacios de almacenamiento 
ultra rápidos que usan para manejar datos temporales. La memoria RAM almacena datos y código mientras se ejecutan, 
pero es volátil, así que se pierde al apagar el equipo. Cuando ejecutas un programa, el computador carga el código desde el 
almacenamiento (HDD o SSD) a la RAM, y la CPU empieza a procesar las instrucciones una a una, accediendo a los registros y 
realizando operaciones de acuerdo con lo que el programa le indique.

# Investigación

## Actividad 1

### ¿Qué es un computador digital moderno y Cuáles son sus partes?

#### Como mencionaba antes, un computador moderno se basa en una serie de componentes que trabajan juntos para ejecutar programas.
La CPU, que es el cerebro del sistema, sigue las instrucciones en lenguaje de máquina, las cuales están almacenadas temporalmente 
en la memoria RAM. Cuando ejecutamos un programa, el computador carga el código desde el almacenamiento (HDD o SSD) a la memoria, 
y la CPU va procesando cada instrucción paso a paso, utilizando sus registros para manejar datos de manera rápida. Todo esto se 
lleva a cabo gracias a la interacción entre estos componentes, permitiendo que el programa funcione como esperamos.

#### Se utilizó Little Man Computer (LMC) como herramienta para entender el funcionamiento de un computador moderno. 
Este modelo simplificado nos permitió visualizar de manera más clara cómo la CPU y los demás componentes interactúan 
para ejecutar tareas o comandos. Al simular el proceso de ejecución de instrucciones, pudimos comprender con mayor 
facilidad cómo cada parte del sistema contribuye al procesamiento y la ejecución de un programa.

![image](https://github.com/user-attachments/assets/cc9cf39e-23a3-469d-af0f-8c348e8b9e83)

es un ejercicio donde sumamos dos enteros 
INP: Lee un número desde la entrada del usuario (teclado) y lo guarda en el acumulador.

STA 90: Almacena el valor del acumulador en la dirección de memoria 90.

ADD 90: Suma el número que está en la dirección de memoria 90 al acumulador.

OUT: Muestra el valor del acumulador (el resultado de la suma).

HLT: Termina la ejecución del programa.

DAT 5: Define el número 5 y lo guarda en la memoria en la dirección 90

## Actividad 2
nos planteamos estas preguntas durante la clase 


#### - ¿Qué es entonces un programa?
   Un programa es un conjunto de instrucciones escritas por un programador que le dice a una
   computadora cómo realizar una tarea específica. Estas instrucciones se escriben en un lenguaje
   de programación, que puede ser de alto nivel (como Python o Java) o de bajo nivel
   (como ensamblador o lenguaje de máquina). El propósito de un programa es ejecutar operaciones,
   procesar datos y producir resultados, ya sea interactuar con el usuario, realizar cálculos,
   o manipular información.
   
#### - ¿Qué es un lenguaje ensamblador?
   El lenguaje ensamblador (o assembly) es un lenguaje de programación de bajo nivel que está 
   muy cerca del lenguaje de máquina, pero más legible para los humanos. A diferencia de los 
   lenguajes de alto nivel, como Python o Java, que abstraen mucho del hardware, el ensamblador
   está diseñado para ser una representación más comprensible de las instrucciones que un 
   procesador entiende. Cada instrucción de ensamblador corresponde a una 
   operación simple que la CPU puede ejecutar directamente. Para convertir un programa en 
   ensamblador en un programa ejecutable, se utiliza un ensamblador, que es un tipo de compilador 
   especializado.
   
#### - ¿Qué es lenguaje de máquina?
   El lenguaje de máquina es el lenguaje nativo que entiende la CPU de un computador.
   Está compuesto por secuencias de códigos binarios (0s y 1s), que representan
   instrucciones específicas para la máquina. Estas instrucciones pueden incluir operaciones
   aritméticas, movimiento de datos entre registros, control de flujo del programa, entre
   otras. A diferencia del lenguaje ensamblador, que usa mnemónicos (como ADD o MOV),
   el lenguaje de máquina se presenta como una serie de números binarios que directamente
   indican las acciones que debe realizar el hardware de la computadora.

  
## Actividad 3

   Al estudiar cómo funciona un PC, entendemos que la CPU usa varios registros para manejar las instrucciones y los datos. 
   Uno de los más importantes es el PC (Program Counter), que guarda la dirección de la próxima instrucción a ejecutar. Cada 
   vez que la CPU procesa una instrucción, el PC se actualiza y apunta a la siguiente.

   Cuando la CPU necesita acceder a la memoria, el registro A (Address) se encarga de manejar las direcciones, indicando dónde están las 
   instrucciones o los datos que necesita. Además, el registro D (Data) guarda temporalmente los datos que la CPU va a procesar.

   En resumen, el PC ayuda a la CPU a seguir el flujo del programa, el A le dice dónde buscar en la memoria, y el D almacena los 
   datos mientras se procesan. Todo esto funciona de manera coordinada para que el PC pueda 
   ejecutar las instrucciones de manera eficiente.
   
## Actividad 4


   ```
   @100     // Carga el valor 100 en el registro A
   D = A    // Guarda ese valor en D
   @32      // Carga la dirección 32 en el registro A
   M = D    // Guarda el valor de D (100) en la dirección 32 de la RAM

   ```

   Comenzamos a profundizar en el lenguaje ensamblador para comprender cómo funciona el almacenamiento de acceso aleatorio.
   
   #### ¿Qué es la RAM?
   La RAM (memoria de acceso aleatorio) es como el espacio de trabajo temporal de la computadora. Guarda datos e instrucciones 
   que la CPU necesita de inmediato para realizar tareas. Es rápida, pero solo retiene la 
   información mientras el equipo está encendido. Cuando apagas la computadora, todo lo que está en la RAM se borra.


## Actividad 5

   Memoria y almacenamiento de instrucciones:

   El capítulo también explica cómo las instrucciones de un programa se almacenan en la memoria y cómo la CPU las accede
   para ejecutar el código. Este proceso involucra cargar instrucciones en la memoria RAM desde el 
   almacenamiento secundario (como el disco duro) para que la CPU las procese.
   El concepto de "memoria volátil":

   Se discute que la memoria RAM es volátil, lo que significa que pierde su contenido cuando el sistema se apaga. 
   Este tipo de memoria es rápida y eficiente para el almacenamiento temporal durante la ejecución de 
   programas, pero no mantiene los datos cuando la energía se corta.
   Gestión de la memoria en la arquitectura de computadoras:

   Se detalla cómo la memoria está organizada en bloques o celdas, y cómo se usan los registros de memoria para acceder a esas celdas.
   También se cubre cómo se realizan las operaciones de lectura y escritura en estas 
   celdas.
   Construcción de una memoria de acceso aleatorio (RAM):

   A través de ejemplos más prácticos, el capítulo presenta cómo se construye y organiza la memoria RAM a nivel de hardware,
   usando circuitos electrónicos para implementar el almacenamiento y el acceso a los datos.
   Memoria de 16-bit:

   El capítulo también cubre cómo se implementa una memoria de 16 bits, explicando cómo se manejan los bits y las palabras de memoria.
   Esto es importante para entender cómo los sistemas computacionales más simples pueden 
   gestionar información utilizando varios bits.
   Acceso a la memoria con instrucciones de ensamblador:

   Se profundiza en cómo las instrucciones en lenguaje ensamblador controlan el acceso a la memoria, mostrando cómo las direcciones 
   se cargan en los registros y cómo los valores se almacenan en la RAM utilizando 
   instrucciones como @ y M.
   El uso de la memoria para datos y programas:

   Se hace hincapié en cómo la memoria no solo se usa para almacenar instrucciones de programas, sino también para manejar datos 
   que el programa necesita durante su ejecución. Esto ayuda a la CPU a acceder y procesar 
   rápidamente la información en tiempo real.

   #### Emulador de hardware:
   El emulador que se presenta en el capítulo se utiliza para simular el comportamiento de la CPU y otros componentes del sistema,
   como la memoria. El propósito es permitir que los estudiantes comprendan cómo funcionan 
   estos sistemas a nivel de hardware sin necesidad de tener acceso a hardware físico real.

   El emulador permite simular:

   La ejecución de instrucciones en lenguaje ensamblador.
   El acceso a la memoria, donde se pueden observar las direcciones de memoria y cómo se almacenan o recuperan los valores.
   El comportamiento de la RAM y cómo las instrucciones de la CPU afectan a la memoria.
   El capítulo describe cómo este emulador puede usarse para probar y entender las operaciones de bajo nivel (como las que
   vimos antes con @ y M) antes de que un programa sea ejecutado en un sistema real. Este tipo de 
   emulador es una herramienta educativa muy útil para visualizar cómo interactúan los componentes y cómo las instrucciones 
   se ejecutan paso a paso.

   En resumen, el capítulo sí cubre la idea del emulador como una forma de simular el funcionamiento de la memoria y la CPU, 
   proporcionando un entorno donde los conceptos de la arquitectura de computadoras se pueden 
   entender y experimentar de manera más accesible.


# Reto

# 1. Comencé con el primer reto, el cual no pude resolver inicialmente sin antes consultar al profesor. Después de recibir
su orientación, implementé dos líneas simples de código en lenguaje de máquina para lograr el objetivo. Estas líneas fueron:

 ```

 @1978  // Carga el valor 1978 en el registro A
 D=A    // Copia el valor del registro A al registro D

 ```
y adjunto una evidencia del proceso con nan2

![image](https://github.com/user-attachments/assets/e41ee833-79db-4d6e-850f-7025f02c8540)


# 2. Se pide cargar el valor 100 en la posición 69 de la RAM. Para hacerlo, se puede utilizar el siguiente código en ensamblador

 ```
@100    // Cargar la dirección de memoria 100 en el registro A
D=A     // Copiar el valor de A (100) a D
@69     // Cargar la dirección de memoria 69 en el registro A
M=D     // Almacenar el valor de D (100) en la posición de memoria 69

 ```

Con esto, el valor 100 se almacena correctamente en la posición 69 de la RAM.

![image](https://github.com/user-attachments/assets/9953ab09-babf-4f63-97e6-7ef23bb20f7b)

# 3. basandome en el anteiror, continuo con este 

  Guarda en la posición 200 de la RAM el contenido de la posición 24 de la RAM
  Este ejercicio se resolvió cargando el valor 42 en la posición 24 de la RAM y luego copiandoese 
  valor a la posición 200. El proceso se realizó de la siguiente manera:

 Primero, se cargó el valor 42 en el registro D y se almacenó en la posición de memoria 24.
 Luego, se accedió al valor almacenado en la posición 24 de la RAM y se copió al registro D.
 Finalmente, el valor contenido en el registro D (que es 42) se almacenó en la posición de memoria 200.
 De esta forma, logramos trasladar el valor 42 de la posición 24 a la posición 200 de la RAM.

 ```
@42     // Cargar el valor 42 en el registro A
D=A     // Copiar el valor de A (42) a D
@24     // Cargar la dirección de memoria 24 en el registro A
M=D     // Almacenar el valor de D (42) en la posición de memoria 24

@24     // Cargar la dirección de memoria 24 en el registro A
D=M     // Copiar el valor de la posición de memoria 24 al registro D
@200    // Cargar la dirección de memoria 200 en el registro A
M=D     // Almacenar el valor de D (que contiene el valor de la posición 24) en la posición de memoria 200

 ```


![image](https://github.com/user-attachments/assets/bd647044-4e87-4b1d-8237-6a0b3580ae5a)


# 4. 
  Este ejercicio consistía en leer el valor que se encuentra en la posición 100 de la RAM, 
  restarle 15 y guardar el resultado en la misma posición 100. La solución se realizó de una
  manera muy simple, logrando lo siguiente:

  Se leyó el valor almacenado en la posición 100 de la RAM.
  A ese valor se le restaron 15.
  Finalmente, se guardó el resultado nuevamente en la misma dirección de memoria (100).
  De esta forma, logramos realizar la operación solicitada de manera eficiente


![image](https://github.com/user-attachments/assets/7dd2d6de-f8ac-426d-8387-90ebb924c1e0)

# 5. 
  Suma el contenido de la posición 0 de la RAM, el contenido de la posición 1 de la RAM
  y con la constante 69. Guarda el resultado en la posición 2 de la RAM.
  
   1.Para resolver este ejercicio, seguimos estos pasos:
   2.Cargar el valor de la posición 0 de la RAM.
   3.Cargar el valor de la posición 1 de la RAM.
   4.Sumar ambos valores junto con la constante 69.
   5.Almacenar el resultado en la posición 2 de la RAM.


```
@5      // Cargar el valor 5 en el registro A (ejemplo de valor inicial para la posición 0)
D=A     // Copiar el valor 5 al registro D
@0      // Cargar la dirección de memoria 0 en el registro A
M=D     // Almacenar el valor de D (5) en la posición 0

@10     // Cargar el valor 10 en el registro A (ejemplo de valor inicial para la posición 1)
D=A     // Copiar el valor 10 al registro D
@1      // Cargar la dirección de memoria 1 en el registro A
M=D     // Almacenar el valor de D (10) en la posición 1

@0      // Cargar la dirección de memoria 0 en el registro A
D=M     // Copiar el valor de la posición 0 (5) al registro D
@1      // Cargar la dirección de memoria 1 en el registro A
D=D+M   // Sumar el valor de la posición 1 (10) al registro D (D = 5 + 10)

@69     // Cargar el valor 69 en el registro A
D=D+A   // Sumar 69 al valor en D (D = 15 + 69)

@2      // Cargar la dirección de memoria 2 en el registro A
M=D     // Almacenar el resultado (D = 84) en la posición 2

```

![image](https://github.com/user-attachments/assets/b4046d86-765c-4ea5-8de0-fa90f582f39b)


# 6.
  continuando, tenemos  Si el valor almacenado en D es igual a 0 salta a la posición 100 de la ROM. 
  podemos encontrar esta posible solucion 
  
  ```

  @100
  D;JEQ

  ```

  que entendemos de esto??? 
  
  @100(Instrucción A), se cargara en el registro la posicion 100 es decir A=100
  luego de cualquier tarea se va ir a la direccion 100
  y luego, D;JEQ(Instrucción C con salto condicional), es un condicinal que me dice 
  si el valor D es == 0 salte a la direccion 100 si D es 0 

# 7. 
  ahora tnemeos este se nos pide Si el valor almacenado en la posición 100 de la RAM es menor
  a 100 salta a la posición 20 de la ROM.

  ```

  @100       
  D=M        // Cargar el valor almacenado en la RAM[100] en D
  @100
  D=D-A      // Restar 100 - RAM[100]
  @20
  D;JLT      // Si RAM[100] < 100, saltar a la posición 20 de la ROM


  ```
  primero cargamos el valor de 100 en D y lo igualamos 
  
  Explicación detallada
  1️. @100→ Carga en el registro Ala dirección de memoria 100.

  2️. D=M→ Guarda en Del valor almacenado en RAM[100].

  3️. @100→ Carga el número 100en el registro A(para poder hacer la comparación).

  4️. D=D-A→ Calcular D = RAM[100] - 100.
     Si D < 0, significa que RAM[100] < 100.

  5️. @20→ Carga en Ala dirección 20, que es donde queremos saltar.

  6️. D;JLT→ Si Des negativo ( RAM[100] < 100), el procesador salta a la ROM en la posición 20.

# 8. 
  las variables como var1, var2 y var3 son símbolos que representan direcciones de memoria en la RAM
  Cuando el ensamblador encuentra un símbolo como @var1, lo trata de dos maneras posibles:

  Si es una etiqueta predefinida (como @SP, @LCL, @ARG), la reemplaza por la dirección específica que tiene en la arquitectura de Nand2Tetris.
  Si es una variable que no ha sido definida antes, el ensamblador le asigna automáticamente una dirección en la RAM a partir de la posición 16.
  
  ```

  @var1
  D = M    // Carga en D el valor almacenado en RAM[var1]
  @var2
  D = D + M // Suma el valor almacenado en RAM[var2] al valor de D
  @var3
  M = D    // Guarda el resultado en RAM[var3]

  ```
   este codigo toma el valor de la Var1 lo carga en D, Seguido Le sumamos el calor almacenado en D con Var2 y el resultado sera 
   el Var 3 

   En Nand2Tetris, el ensamblador asigna direcciones de memoria a las variables automáticamente.
   Las variables se almacenan en la RAM a partir de la dirección 16.

   Esto significa que:

  La primera variable encontrada (var1) se asigna a RAM[16].
  La segunda (var2) se asigna a RAM[17].
  La tercera (var3) se asigna a RAM[18].  

# 9. 
  #### ¿Qué hace este programa?
  Este programa es una simple secuencia de suma en la que a una variable i le sumamos un valor asignado
  Inicializa la variable i en 1.
  Inicializa la variable sum en 0.
  Suma i al valor de sum.
  Incrementa i en 1.

  #### ¿En qué parte de la memoria RAM está la variable i y sum? ¿Por qué en esas posiciones?
  al igal que lo anterior sabemos que se almacenan apartir de la posicion 16 de la ram 
  Por lo tanto:
 ```
  i RAM[16]
  sum  RAM[17]
 ```
  para optimizarlo a solamente 2 instrucciones puede ser 
 ```
  @i
  M=M+1
```
  Esto funciona porque la ALU del hardware permite modificar M directamente sin necesidad de un paso intermedio en D.
  
# 10.

   Multiplicar el valor de R0 por 2 y guardarlo en R1

   ```

   @R0    // Apunta a la dirección RAM[0]
   D=M    // Carga el valor de R0 en el registro D
   D=D+M  // D = R0 + R0 (esto es 2 * R0)
   @R1    // Apunta a la dirección RAM[1]
   M=D    // Guarda el resultado en R1

  ```
# 11.
  #### ¿Qué hace este programa?
  Este programa cuenta hacia atrás desde 1000 hasta 0 y luego termina.

  Inicializa i = 1000.
  
  Entra en un bucle (LOOP) donde:
  
  Si i == 0, salta a CONT (fin del programa).
  
  Si i > 0, decrementa i (i = i - 1) y repite el bucle.
  
  Cuando i llega a 0, el programa termina.
  
  Este código implementa un contador regresivo de 1000 a 0.
  
 #### ¿En qué memoria está almacenada la variable i? ¿En qué dirección?
 
 En Nand2Tetris, las variables como i se almacenan en la RAM, empezando desde la dirección RAM[16] en adelante.

 Como i no es un registro predefinido (R0 - R15), el ensamblador le asignará 
 la primera posición disponible en la RAM, que es RAM[16].
 
 #### ¿En qué memoria y en qué dirección está almacenado el comentario // i = 1000?
 
 Los comentarios NO se almacenan en memoria.
 Son ignorados por el ensamblador y solo sirven para los programadores.
 

 #### ¿Cuál es la primera instrucción del programa? ¿Dónde está almacenada?

 La primera instrucción es:

  @1000
  Es una instrucción A-instruction que carga el valor 1000 en el registro D.
  Se almacena en la ROM, que es donde están las instrucciones ejecutables.
  
  Conclusion:
  Memoria: ROM (memoria de solo lectura).
  Dirección: ROM[0] (primera instrucción del programa).
  
  #### ¿Qué son CONT y LOOP?
  
  Son etiquetas (labels) que representan posiciones en la ROM.
  (LOOP) y (CONT) no se almacenan en memoria, sino que le dicen al
  ensamblador a qué dirección de la ROM se debe saltar cuando el 
  programa usa @LOOP o @CONT.

  #### ¿Cuál es la diferencia entre i y CONT?
  
  i es una variable, así que se almacena en la RAM (en RAM[16]).
  CONT es una etiqueta, así que NO ocupa espacio en RAM ni en ROM, pero el
  ensamblador la convierte en una dirección en ROM.


# 12. Implemente en ensamblador:

  ```
  R4 = R1 + R2 + 69
  ```

  SOLUCION :

  
```

       // R4 = R1 + R2 + 69

@1    // Cargar R1 en D (equivale a @R1)
D=M   

@2    // Sumar R2 a D (equivale a @R2)
D=D+M 

@69   // Sumar 69 a D
D=D+A 

@4    // Guardar el resultado en R4 (equivale a @R4)
M=D   


```  

# 13. Implemente en ensamblador:


```

if R0 >= 0 then R1 = 1
else R1 = –1

(LOOP)
goto LOOP

```
SOLUCION:

```



// Si R0 < 0, entonces R1 = -1
@1
M=-1
@LOOP
0;JMP   // Saltar al bucle infinito

(POSITIVE) //(POSITIVE): Etiqueta usada como punto de referencia en los 
                          saltos.
// Si R0 >= 0, entonces R1 = 1
@1
M=1

(LOOP)
// Bucle infinito
@LOOP
0;JMP


```

Si R0 >= 0, entonces R1 = 1.
Si R0 < 0, entonces R1 = -1.
Luego entra en un bucle infinito para detener la ejecución.

# 14. Implementa en ensamblador:

```
 R4 = RAM[R1]

```


```

// Guardamos el valor 55 en RAM[10]
@55
D=A
@10
M=D

// Guardamos la dirección 10 en R1 (RAM[1])
@10
D=A
@1
M=D

// Cargar el valor de R1 (RAM[1]) en D
@1
D=M

// Usar D como dirección de memoria y cargar el valor de RAM[R1] en D
A=D
D=M

// Guardar el valor en R4 (RAM[4])
@4
M=D


```

Hemos guardado el número 55 en RAM[10]
Hemos usado R1 (RAM[1]) para almacenar el numero 10
Hemos leído RAM[10] a traves de R1 y lo hemos copiado en R4 (RAM[4])

Este código funciona directamente en Nand2Tetris, puedes probarlo en el 
simulador y verificar que RAM[4] tenga el valor 55


# 15. Implementa en ensamblador:


```


// R0 contiene la dirección inicial de la región de memoria
// R1 contiene el tamaño de la región de memoria
// Debemos almacenar -1 en cada posición desde R0 hasta (R0 + R1 - 1)

@R0
D=M          // D = dirección inicial (R0)
@addr
M=D          // addr = R0 (guardamos la dirección actual)

// Comenzamos el loop
(LOOP)
  @R1
  D=M        // D = tamaño de la región
  @END
  D;JEQ      // Si R1 == 0, terminamos

  @addr
  A=M        // Apuntamos a la dirección actual
  M=-1       // Guardamos -1 en esa dirección

  @addr
  M=M+1      // Avanzamos a la siguiente dirección

  @R1
  M=M-1      // Reducimos el tamaño restante de la región

  @LOOP
  0;JMP      // Repetimos el proceso

(END)
@END
0;JMP        // Fin del programa, bucle infinito opcional


```

 Recorremos la memoria usando addr como dirección actual.
 Usamos R1 como contador de posiciones restantes.
 Almacenamos -1 en cada dirección hasta completar la región.
 Terminamos con un salto a (END).



# 16. Implementa en ensamblador:

```

// Definir dirección base del arreglo (por ejemplo, en RAM[20])
@20  
D=A    
@arr  
M=D    // Guardamos la dirección base en 'arr'

// Inicializar sum = 0
@sum  
M=0    

// Inicializar j = 0
@j  
M=0    

(LOOP)  
    // Si j >= 10, salir del bucle
    @j  
    D=M  
    @10  
    D=D-A  
    @END  
    D;JGE  // Si j - 10 >= 0, terminamos
    
    // Obtener arr[j]
    @j  
    D=M  
    @arr  
    A=M  
    A=A+D  // A = arr + j (posición del elemento)
    D=M    // D = arr[j]

    // sum = sum + arr[j]
    @sum  
    M=M+D  

    // j = j + 1
    @j  
    M=M+1  

    // Volver al inicio del bucle
    @LOOP  
    0;JMP  

(END)  
    @END  
    0;JMP  // Ciclo infinito

    
```


 Cargamos la dirección base del arreglo (arr = RAM[20]).
 Recorremos el arreglo usando j como índice.
 Sumamos cada elemento de arr en sum.
 Terminamos cuando j >= 10.

 ¿Qué hace este programa?

Este programa suma los primeros 10 elementos del arreglo arr y almacena el resultado en la variable sum. Al finalizar, el programa entra en un ciclo infinito (sin hacer nada más).

¿Cuál es la dirección base de arr en la memoria RAM?

La dirección base de arr en la memoria es 20. Esto se establece en el primer bloque de código con la instrucción @20 que asigna la dirección 20 a la etiqueta arr mediante la instrucción M=D.

¿Cuál es la dirección base de sum en la memoria RAM y por qué?

La dirección base de sum es la siguiente dirección libre después de la dirección 20.

En este caso, como no se especifica explícitamente una dirección para sum, se asume que las direcciones anteriores están ocupadas por otros datos.

Es común que el sistema asigna una dirección consecutiva para sum, por ejemplo, si arr ocupa desde la dirección 20, sum podría estar en la dirección 21.

Sin embargo, como el programa no indica la dirección de sum, se puede inferir que la dirección de sum es una dirección libre inmediatamente después de la dirección 20.

¿Cuál es la dirección base de j en la memoria RAM y por qué?

Al igual que sum, la dirección de j es una dirección libre después de la dirección 21 (que puede ser la de sum). El programa no asigna explícitamente una dirección a j, pero siguiendo el mismo razonamiento, j se ubicará en la siguiente dirección libre disponible en la memoria.

# 17. Implementa en ensamblador:

```
 @7  
D=D-A    // D = D - 7
@69  
D;JEQ    // Si D == 0, saltar a ROM[69]


```

El programa verifica si el valor en el registro D es igual a 7.

 Si D == 7, el programa salta a la instrucción almacenada en la posición ROM[69].
 Si D ≠ 7, el programa sigue ejecutando las instrucciones que vienen después en la ROM.


# 18. Utiliza esta herramienta para dibujar un bitmap en la pantalla.

 usamos Jack Bitmap Editor v2.5 para plasmar una imagen en pantalla la cual nos dio este codigo en Hack Assembly.

```
(draw)
	// put bitmap location value in R12
	// put code return address in R13
	@SCREEN
	D=A
	@R12
	AD=D+M
	// row 6
	@15390 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	// row 7
	D=A // D holds previous addr
	@32
	AD=D+A
	@15390 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	// row 8
	D=A // D holds previous addr
	@32
	AD=D+A
	@15390 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	// row 9
	D=A // D holds previous addr
	@32
	AD=D+A
	@15390 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	// row 10
	D=A // D holds previous addr
	@32
	AD=D+A
	@15390 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	// row 11
	D=A // D holds previous addr
	@32
	AD=D+A
	@15390 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	// row 12
	D=A // D holds previous addr
	@32
	AD=D+A
	@15390 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	// row 13
	D=A // D holds previous addr
	@32
	AD=D+A
	@15390 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	// row 14
	D=A // D holds previous addr
	@32
	AD=D+A
	@15390 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	// row 15
	D=A // D holds previous addr
	@31
	AD=D+A
	@31744 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	AD=A+1 // D holds addr
	@32767
	A=!A // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	AD=A+1 // D holds addr
	@15 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	// row 16
	D=A // D holds previous addr
	@30
	AD=D+A
	@31744 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	AD=A+1 // D holds addr
	@32767
	A=!A // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	AD=A+1 // D holds addr
	@15 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	// row 17
	D=A // D holds previous addr
	@30
	AD=D+A
	@14336 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	AD=A+1 // D holds addr
	M=0
	AD=A+1 // D holds addr
	@7 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	// row 18
	D=A // D holds previous addr
	@30
	AD=D+A
	@14336 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	AD=A+1 // D holds addr
	M=0
	AD=A+1 // D holds addr
	@7 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	// row 19
	D=A // D holds previous addr
	@30
	AD=D+A
	@14336 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	AD=A+1 // D holds addr
	M=0
	AD=A+1 // D holds addr
	@7 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	// row 20
	D=A // D holds previous addr
	@30
	AD=D+A
	@14336 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	AD=A+1 // D holds addr
	M=0
	AD=A+1 // D holds addr
	@7 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	// row 21
	D=A // D holds previous addr
	@30
	AD=D+A
	@2048 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=A-D // RAM[addr]=-val
	AD=A+1 // D holds addr
	M=-1
	AD=A+1 // D holds addr
	@7 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	// row 22
	D=A // D holds previous addr
	@30
	AD=D+A
	@2048 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=A-D // RAM[addr]=-val
	AD=A+1 // D holds addr
	M=-1
	AD=A+1 // D holds addr
	@7 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	// row 23
	D=A // D holds previous addr
	@30
	AD=D+A
	@2048 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=A-D // RAM[addr]=-val
	AD=A+1 // D holds addr
	M=-1
	AD=A+1 // D holds addr
	@7 // A holds val
	D=D+A // D = addr + val
	A=D-A // A=addr + val - val = addr
	M=D-A // RAM[addr] = val
	// row 24
	D=A // D holds previous addr
	@30
	AD=D+A
	M=0
	AD=A+1 // D holds addr
	M=0
	AD=A+1 // D holds addr
	M=0
	// row 25
	D=A // D holds previous addr
	@30
	AD=D+A
	M=0
	AD=A+1 // D holds addr
	M=0
	AD=A+1 // D holds addr
	M=0
	// row 26
	D=A // D holds previous addr
	@30
	AD=D+A
	M=0
	AD=A+1 // D holds addr
	M=0
	AD=A+1 // D holds addr
	M=0
	// return
	@R13
	A=M
	D;JMP


```
   
que nos dio esta imagen 

![image](https://github.com/user-attachments/assets/bb612cf4-4774-4404-9ff9-d1d2a09eb991)

hice un pequeñp test para ver como interactua con la cpu emulator 


![image](https://github.com/user-attachments/assets/2715170e-34a7-44b2-8e0e-a5f6d29669c6)


# 19 . se pide analizar este codigo.

0100000000000000

1110110000010000

0000000000010000

1110001100001000

0110000000000000

1111110000010000

0000000000010011

1110001100000101

0000000000010000

1111110000010000

0100000000000000

1110010011010000

0000000000000100

1110001100000110

0000000000010000

1111110010101000

1110101010001000

0000000000000100

1110101010000111

0000000000010000

1111110000010000

0110000000000000

1110010011010000

0000000000000100

1110001100000011

0000000000010000

1111110000100000

1110111010001000

0000000000010000

1111110111001000

0000000000000100

1110101010000111

el cual al cargarlo como un .hack en nan2T
mostro este codigo 

```
    
// Inicialización
@16384          // Carga la dirección de inicio de la pantalla (16384) en A
D=A             // Almacena 16384 en D

@16             // Selecciona la posición de memoria 16 (usada como variable)
M=D             // Guarda 16384 en M[16] (inicializa el puntero)

// Bucle principal
(LOOP)
@24576          // Carga la dirección del teclado (24576) en A
D=M             // Lee el estado del teclado (0 si no hay presión)

@19             // Prepara salto a la dirección 19 (tecla presionada)
D;JNE           // Si D != 0 (tecla presionada), salta a HANDLE_INPUT

@16             // Carga la dirección de la variable (16) en A
D=M             // Lee el valor del puntero en D

@16384          // Carga el límite inferior (inicio pantalla)
D=D-A           // Calcula D = puntero - 16384

@4              // Prepara salto a la dirección 4 (CONTINUE)
D;JLT           // Si D < 0 (puntero < 16384), salta a CONTINUE

@16             // Carga dirección de la variable (16)
M=0             // Si puntero es menor que 16384, lo resetea a 0
@8              // Prepara salto a la dirección 8 (UPDATE)
0;JMP           // Salto incondicional a UPDATE

(CONTINUE)
@4              // Prepara salto a la dirección 4 (LOOP)
0;JMP           // Salto incondicional de vuelta al LOOP

// Manejo de entrada
(HANDLE_INPUT)
@16             // Carga dirección de la variable (16)
D=M             // Lee el valor del puntero en D

@24576          // Carga el límite superior (teclado)
D=D-A           // Calcula D = puntero - 24576

@4              // Prepara salto a la dirección 4 (LOOP)
D;JGT           // Si D > 0 (puntero > 24576), salta a LOOP

@16             // Carga dirección de la variable (16)
D=M+1           // Incrementa el puntero en 1
M=D             // Guarda el nuevo valor

@16             // Carga dirección de la variable (16)
MD=M-1          // Decrementa el puntero en 1 (y guarda en MD)

@4              // Prepara salto a la dirección 4 (LOOP)
0;JMP           // Salto incondicional de vuelta al LOOP

```

me da una condicion para que un codigo haga un salto si preciono una tecla

# 20
```
(draw)
    // Verifica si la tecla "D" está presionada
    @KBD
    D=M
    @68
    D=D-A
    @DRAW
    D;JEQ

    // Si no es "D", borra la pantalla
    @CLEAR
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

En la etiqueta (draw), se accede a la memoria del teclado, donde se almacenó la última tecla presionada,
y se lee el valor de la tecla. Este valor se guarda en el registro D. Luego, se carga el valor 68 en A 
(que es el valor de la letra "D" en ASCII) para restarlo al valor almacenado en D. Si el resultado de esta
resta es 0, significa que se presionó la tecla "D". Si es así, el programa salta a la etiqueta DRAW para 
ejecutar el código de dibujo.

Si la tecla no es "D", el programa salta a la etiqueta CLEAR para borrar la pantalla

@SCREEN: Accede a la dirección base de la pantalla (16384).
D=A: Guarda la dirección de la pantalla en el registro D.
@R12: Accede al registro R12, que contiene un valor adicional para ajustar la posición en la pantalla.
AD=D+M: Suma el valor de R12 con la dirección base de la pantalla y guarda el resultado en A y D.

El código continúa dibujando fila por fila, asignando valores de 1 y 0 en las posiciones de memoria correspondientes para formar la imagen.

M=0: Escribe 0 en la posición de memoria actual, lo que apaga los píxeles.
@32: Avanza a la siguiente fila (cada fila tiene 32 palabras de 16 bits en Nand2Tetris).

Este proceso se repite para cada fila, borrando o dibujando en toda la pantalla.



