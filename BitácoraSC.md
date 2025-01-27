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


- ¿Qué es entonces un programa?
   Un programa es un conjunto de instrucciones escritas por un programador que le dice a una
   computadora cómo realizar una tarea específica. Estas instrucciones se escriben en un lenguaje
   de programación, que puede ser de alto nivel (como Python o Java) o de bajo nivel
   (como ensamblador o lenguaje de máquina). El propósito de un programa es ejecutar operaciones,
   procesar datos y producir resultados, ya sea interactuar con el usuario, realizar cálculos,
   o manipular información.
- ¿Qué es un lenguaje ensamblador?
   El lenguaje ensamblador (o assembly) es un lenguaje de programación de bajo nivel que está 
   muy cerca del lenguaje de máquina, pero más legible para los humanos. A diferencia de los 
   lenguajes de alto nivel, como Python o Java, que abstraen mucho del hardware, el ensamblador
   está diseñado para ser una representación más comprensible de las instrucciones que un 
   procesador entiende. Cada instrucción de ensamblador corresponde a una 
   operación simple que la CPU puede ejecutar directamente. Para convertir un programa en 
   ensamblador en un programa ejecutable, se utiliza un ensamblador, que es un tipo de compilador 
   especializado.
- ¿Qué es lenguaje de máquina?
   El lenguaje de máquina es el lenguaje nativo que entiende la CPU de un computador.
   Está compuesto por secuencias de códigos binarios (0s y 1s), que representan
   instrucciones específicas para la máquina. Estas instrucciones pueden incluir operaciones
   aritméticas, movimiento de datos entre registros, control de flujo del programa, entre
   otras. A diferencia del lenguaje ensamblador, que usa mnemónicos (como ADD o MOV),
   el lenguaje de máquina se presenta como una serie de números binarios que directamente
   indican las acciones que debe realizar el hardware de la computadora.
