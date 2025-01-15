# Sistemas Operativos
Apuntes de la asignatura de Sistemas Operativos

## Introducción
Un sistema informático es un conjunto de componentes físicos (hardware) y lógicos (software). El elemento central del sistema informático es el ordenador.

La parte física o hardware está formada por todos los elementos electrónicos y mecánicos.

Físicamente, de mayor a menor precio, tamaño, potencia, velocidad y prestaciones, podemos hacer una clasificación de los sistemas informáticos en:
- **Superordenadores**: Son ordenadores que no se encuentran en el mercado, sino que se fabrican pera grandes organizaciones nacionales o Intemacionales con el fin de realizar tareas especificas evanzadas, como cientificas, militares, tecnológicas...
- **Macroordenadores (mainframes)**: Son ordenadores que pueden ocupar grandes espacios y pueden dar servicios a cientos de usuarios simultáneamente.
- **Servidores y estaciones de trabajo (workstation)**: Son ordenadores que puedan ofrecer servicios a otros ordenadores dentro de una red, como conexión a internet, acceso a los periféricos, acceso a bases de datos compartidas...
- **Ordenadores personales o PC**: Son ordenadores que surglerontras la Incorporación de los microprocesadores. Se utilizan tanto en el ámbito domestico como en el profesional. A su vez pueden ser de sobremesa, portátiles, tablets, smartpnones

La parte lógica o sofware está formada por todos los elementos no físicos como el sistema operatvo, los programas y los datos almacenados dentro del ordenador.

Se puede considerar que aparecen los primeros ordenadores cuando se desarrolla el concepto de programa interno, es decir, se administran unos datos de entrada, un programa los procesa y se obtienen unos datos de salida.

Podemos diferenciar 5 generaciones de ordenadores:
- 1ª Generación: En esta generación los ordenadores funcionaban con válvulas de vacio y el uso era exclusivo para fines cientícos y militares, no comerciales.
- 2ª Generación: Surge por la introducción del transistor, los ordenadores se vuelven más pequeñas y económicos. En esta generación aparece el concepto de periférico.
- 3ª Generación: Se caracteriza por la utilización de los circuitos integrados o chips, circuitos compuestos por transistores miniaturizados.
- 4ª Generación: Se caracteriza por la alta integración de los componentes electrónicos y esto dio lugar a la aparición del microprocesador, que es la integración de todos los elementos básicos del ordenador en un solo circuito integrado.
- 5ª Generación: Comenzó en 1981 tras la agarición del PC, comercializado por IBM. Este ordenador, que posteriormente creó un estándar de ordenadores
### Componentes Hardware
Podemos diferenciar diferentes partes en el ordenador:
#### Carcasa
- Placa base (*motherboard*): En ella encontramos el micoprocesados, la memoria RAM, las tarjetas de expansión y los conectores para periféricos y componentes que no estén dentro de la carcasa.
- Fuente de alimentación
- Unidades de almacenamiento externas (HDD, CD, DVD..)
#### Periféricos
Se dividen en varios tipos:
- Entrada: Introducen información (teclado, ratón, webcam...)
- Salida: Permiten obtener información del ordenador (pantalla, altavoces, impresora...)
- Entrada y Salida (*E/S*): Permiten tanto introducir como obtener información (pantalla táctil, impresora multifunción...)
#### Memorias auxiliares
Se pueden considerar periféricos de E/S (discos duros, CD, DVD, tarjetas de memoria, pendrives...)

### Componentes Funcionales
Funcionalmente las partes del ordenador se pueden clasificaren:
- Unidad central de proceso (CPU)
  - Unidad aritmético-lógica (UAL)
  - Unidad de control (UC)
- Memoria principal (la memoria RAM)
- Buses
- Unidad de E/S
- Periféricos
- Memoria auxiliar
El nivel funcional no se trata en esta asignatura.

### Componentes Software
El software de un sistema informático son todos los programas y datos. El sistema operativo es el primer software que se ejecuta al encender un ordenador (si no contamos BIOS y bootstrap) para controlar todo el equipo.

Los programas son conjuntos de instrucciones que se cargarán el la memoria principal para ejecutarse, el procesador leerá cada instrucción e irá ejecutando el programa. Para realizar estos programas se utilizan diferentes lenguajes de programación:
- **Lenguajes de bajo nivel**
  - ***Lenguaje máquina***: Es el que comprende directamente el ordenador. Depende del hardware utilizado (cualquier otro lenguaje debe ser traducido a lenguaje máquina para ser ejecutado) Se trata de 0 y 1.
  - ***Lenguaje ensamblador***: Está basado en el lenguaje máquina ya que cada instrucción de ensamblador equivale a una instrucción de lenguaje máquina. Utiliza instrucciones básicas pero varía dependiendo del microprocesador.
- **Lenguajes de alto nivel**: Son lenguajes independientes del hardware que pueden llevarse de un ordenador a otro, no varían sus instrucciones, aun así deben ser traducidos a lenguaje máquina, para lo que hay dos métodos en función del lenguaje:
  - Interpretar: Se va traduciendo y ejecutando las instrucciones directamente (es más lento)
  - Compilar: Todo el programa se traduce y posteriormente se ejecuta entero. Hay que hacer la compilación previa a la ejecución pero es más rápido luego.

## Elementos, estructura y funciones
El sistema operativo es un conjunto de programas que se inician al arrancar el ordenador y cuya función principal es desvincular al usuario de las características hardware de su equipo y facilitarle así la ejecución de otros programas, es decir, simplificar al usuario el uso del ordenador.

En cada generación de ordenadores existieron diferentes sistemas operativos:
- 1ª Generación: Sin sistema operativo algunos, EXEC I
- 2ª Generación: EXEC II, EXEC 8, CTSS...
- 3ª Generación: OS/360, TOPS-10, MULTICS, UNIX...
- 4ª Generación: TOPS-20, BSD...
- 5ª Generación: MS-DOS, Windows, XENIX, OS/400, Solaris, MAC OS, Linux...

### Tipos de sistemas operativos
Hay diferentes formas de clasificar los sistemas operativos en función de:
- Tiempo de respuesta:
  - Procesamiento por lotes
  - Interactivos
  - Tiempo real
- Número de usuarios:
  - Monousuario
  - Multiusuario
- Número de procesos:
  - Monoprogramación
  - Multiprogramación
- Número de procesadores:
  - Monoproceso
  - Multiproceso
    - Simétricos
    - Asimétricos
- Trabajo en red:
  - Centralizados
  - En red
  - Distribuidos
- Estructura del sistema operativo:
  - Monolíticos
  - En capas (o en niveles)
  - Máquina virtual
  - Cliente-Servidor

### Funciones del sistema operativo
Las principales funciones de un sistema operativo son:
#### Gestión de procesos
Un proceso es un programa en ejecución (un programa del sistema, los programas "normales" o aplicaciones, pueden tener muchisimos procesos). Existen dos tipos de procesos con diferentes estados:
- Procesos del sistema: Se ejecutan por el sistema y proporcionan servicios al usuario o al propio sistema.
- Procesos de usuario: Procesos que manda ejecutar el propio usuario.

Los procesos pueden estar:
- Listos: Preparados para ser ejecutados, a la espera de que la CPU quede libre.
- Bloqueados: El proceso está esperando un recurso ocupado por otro proceso.
- En ejecución: Está ocupando CPU.
#### Gestión de memoria
Un sistema operativo debe ser capaz de gestionar la memoria del sistema. Los procesos que se ejecutan en el sistema necesitan que se les asigne una zona de memoria para su ejecución y que se le proteja esa zona de otros accesos o poder compartila.
- Protección
- Particionamiento
  - Paginación
  - Segmentación
- Intercambio (*swapping*)
- Compartción
- Reubicación
- Memoria Virtual
- Fragmentación (interna/externa)
## Linux
