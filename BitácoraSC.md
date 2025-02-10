# Sistemas Computacionales.

## Experiencia de aprendizaje 1: Arquitectura del computador.
###La semana pasada comenzamos el curso realizando un análisis detallado de lo que es un computador y cómo funcionan sus componentes. 
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

###¿Qué es un computador digital moderno y Cuáles son sus partes?

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
   
   ####¿Qué es la RAM?
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






   
   
