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
#### Gestión de E/S
Los dispositivos de E/S tales como periféricos y memorias auxiliares deben ser gestionados por el sistema operativo a través de diferentes métodos:
- Interrupciones y rutinas de atención: Una interrupción se produce cuando algún elemento hardware produce una señal al sistema para llamar su atención. Se las llaman IRQ (Interrupt Request), y tienen como función intemumpir el trabajo del procesador para destinario a otra actividad.
- Acceso directo a memoria (DMA): La realizan ciertos periféricos cuando la cantidad de información que quiere transferir es grande. Se realiza a través de unas líneas especiales llamadas DRQ (DMA Request) para dejar libre al procesador.
- Caching:  Consiste en almacenar en una caché temporal, de rápido acceso, los datos más frecuentemente solicitados o envados.
- Buffering: Consiste en utilizar un área de memoria simulando un dispositivo o un periférico que hará de dispositivo como buffer, entre el periférico real y el procesador.
- Spooling: Consiste en simultanear la E/S a los periféricos.
#### Gestión de archivos
Un archivo o fichero es un objeto que representa la unidad lógica de almacenamiento de información, para gestionar los archivos el sistema operativo cuenta con el sistema de ficheros, los más utilzados son los que se indican a continuación:
- FAT: Tabla de asignación de ficheros (File Allocation Table). Sistema de archivos introducido a partir del MS-DOS. Existen dos tipos de sistemas de archivos FAT:
  - FAT16
  - FAT32
- NTFS: Sistema de archivos de nueva tecnología (New Technology File System) de Windows. Mejora el sistema de ficheros al introducir mayor seguridad, mayor estabilidad, mayor tamaño de los archivos.
- EXT2, EXT3 y EXT4: Sistemas de archivos soportados por la mayoría de las distribuciones Linux. Cada uno es la evolución del anterior (EXT4 soporta *journaling* pararegistrar cambios y poder recuperar datos en caso de fallo)
- ReiserFS: Sistema de algunas distros de Linux.
- CDFS: Sistema de los CD-ROM (ISO 9660)
- UDF: Sistema de los DVD y los BluRay (ISO 13346)
- HFS: *Hierarchical File System* Sistema de archivos introducido por UNIX, actualmente usado por MacOS.
- HFS+: Sustituto de HFS y soporta journaling.

## Linux
El sistema operativo Linux es una versión que se basa en el sistema operativo Unix, desarrollada para ordenadores personales, es un sistema operativo multiusuario y multitarea.

El kernel es el núcleo del sistema operativo. Es la parte que interactúa directamente con el hardware, administra todos los recursos hardware del sistema, como la memoria, el microprocesador o los periféricos. 
Este kernel tiene una estructura que aísla al usuario del propio núcleo, es un proceso llamado shell que interpreta las órdenes o aplicaciones del usuario, bien desde una terminal en modo texto, o bien desde un entomo gráfico. Una misma versión de Linux puede tener instaladas distintas shells y un usuario puede cambiar entre una y otra.
Uno de los intérpretes de comandos más extendidos actualmente es el shell bash (Bourne Agaín Shell) que utilizan por defecto muchas distribuciones, aunque hay otros, como el shell sh (Bourne shell) creado para Unix.

Usaremos la shell de texto:

| Comando	| Opciones | Descripción	| Ejemplo |
| - | - | - | - |
| ls	| N/A	| Lista los archivos y directorios en el directorio actual.	| ls |
| |	-l	| Lista en formato largo.	| ls -l |
| |	-a	| Incluye archivos ocultos.	| ls -a |
| |	-h	| Muestra tamaños en formato legible.	| ls -h |
| cd	| N/A	| Cambia el directorio actual.	| cd /home |
| pwd	| N/A	| Muestra la ruta completa del directorio actual.	| pwd |
| mkdir	| N/A	| Crea un nuevo directorio.	| mkdir nuevo_directorio |
|	| -p	| Crea directorios padres según sea necesario.	| mkdir -p ruta/nuevo_directorio |
| rmdir	| N/A	| Elimina un directorio vacío.	| rmdir viejo_directorio |
| rm	| N/A	| Elimina archivos o directorios.	| rm archivo.txt |
|	| -r	| Elimina directorios de forma recursiva.	| rm -r directorio |
| |	-f	| Fuerza la eliminación sin preguntar.	| rm -f archivo.txt |
| cp	| N/A	| Copia archivos o directorios.	| cp archivo.txt copia_archivo.txt |
|	| -r	| Copia directorios de forma recursiva. | cp -r directorio copia_directorio|
|	|-i	|Pregunta antes de sobrescribir.|	cp -i archivo.txt copia_archivo.txt|
|mv	|N/A	|Mueve o renombra archivos o directorios.|	mv archivo.txt nuevo_nombre.txt|
|	|-i	|Pregunta antes de sobrescribir.|	mv -i archivo.txt nuevo_nombre.txt|
|	|-u	|Solo mueve si el archivo de destino es más antiguo.	|mv -u archivo.txt nuevo_nombre.txt|
|touch	|N/A	|Crea un archivo vacío o actualiza la fecha de modificación de un archivo.|	touch nuevo_archivo.txt|
|cat	|N/A	|Muestra el contenido de un archivo.| cat archivo.txt|
|more	|N/A	|Muestra el contenido de un archivo página por página.|	more archivo.txt|
|less	|N/A	|Similar a more, pero permite desplazarse hacia arriba y hacia abajo.|	less archivo.txt|
|head	|N/A	|Muestra las primeras líneas de un archivo.| head archivo.txt|
|	|-n	|Especifica el número de líneas a mostrar.|	head -n 10 archivo.txt|
|tail	|N/A	|Muestra las últimas líneas de un archivo.|	tail archivo.txt|
|	|-n	|Especifica el número de líneas a mostrar.|	tail -n 10 archivo.txt|
|	|-f	|Muestra el contenido en tiempo real.|	tail -f archivo.txt|
|find	|N/A	|Busca archivos y directorios en una jerarquía de directorios.|	find /home -name archivo.txt|
|	|-name	|Busca por nombre.|	find /home -name archivo.txt|
|	|-type	|Busca por tipo de archivo.|	find /home -type d|
|grep	|N/A	|Busca texto dentro de archivos.|	grep "texto" archivo.txt|
|	|-i	|Ignora mayúsculas y minúsculas.|	grep -i "texto" archivo.txt|
|	|-r	|Busca de forma recursiva.|	grep -r "texto" /home|
|chmod	|N/A	|Cambia los permisos de un archivo o directorio.|	chmod 755 archivo.txt|
|	|-R	|Cambia permisos de forma recursiva.|	chmod -R 755 directorio|
|chown	|N/A	|Cambia el propietario de un archivo o directorio.|	chown usuario:grupo archivo.txt|
|	|-R	|Cambia propietario de forma recursiva.|	chown -R usuario:grupo directorio|
|df	|N/A	|Muestra el uso del espacio en disco.|	df|
|	|-h	|Muestra tamaños en formato legible.|	df -h|
|man	|N/A	|Muestra el manual de usuario de un comando.|	man ls|
|du	|N/A	|Muestra el uso del espacio en disco por archivos y directorios.|	du|
|	|-sh	|Muestra el tamaño total en formato legible.|	du -sh /home|
|ps	|N/A	|Muestra una lista de procesos en ejecución.|	ps|
|	|-aux	|Muestra todos los procesos en ejecución.|	ps aux|
|kill	|N/A	|Termina un proceso.|	kill 1234|
|	|-9	|Fuerza la terminación de un proceso.|	kill -9 1234|
|top	|N/A	|Muestra los procesos en ejecución en tiempo real.|	top|
|echo	|N/A	|Muestra un mensaje en la pantalla.|	echo "Hola, mundo"|
|nano	|N/A	|Editor de texto en la terminal.|	nano archivo.txt|
|vi	|N/A	|Otro editor de texto en la terminal.|	vi archivo.txt|
|wget	|N/A	|Descarga archivos desde la web.|	wget http://ejemplo.com/archivo.zip|
|curl	|N/A	|Transfiere datos desde o hacia un servidor.|	curl http://ejemplo.com|
|tar	|N/A	|Archiva varios archivos en uno solo.|	tar -cvf archivo.tar directorio|
|	|-cvf	|Crea un archivo tar.|	tar -cvf archivo.tar directorio|
|	|-xvf	|Extrae un archivo tar.|	tar -xvf archivo.tar|
|zip	|N/A	|Comprime archivos.|	zip archivo.zip archivo.txt|
|	|-r	|Comprime directorios de forma recursiva.|	zip -r archivo.zip directorio|
|unzip	|N/A	|Descomprime archivos.|	unzip archivo.zip|
|useradd|N/A	|Crea un nuevo usuario.|	useradd nuevo_usuario|
|	|-m	|Crea el directorio home del usuario.|	useradd -m nuevo_usuario|
|	|-d	vEspecifica el directorio home del usuario.|	useradd -d /ruta/home nuevo_usuario|
|	|-s	|Especifica el shell del usuario.|	useradd -s /bin/bash nuevo_usuario|
|	|-G	|Añade el usuario a uno o más grupos.|	useradd -G grupo1,grupo2 nuevo_usuario|
|usermod|N/A	|Modifica una cuenta de usuario existente.|	usermod -l nuevo_nombre usuario|
|	|-l	|Cambia el nombre de usuario.|	usermod -l nuevo_nombre usuario|
|	|-d	|Cambia el directorio home del usuario.|	usermod -d /nueva/ruta/home usuario|
|	|-s	|Cambia el shell del usuario.|	usermod -s /bin/zsh usuario|
|	|-G	|Cambia los grupos a los que pertenece el usuario.|	usermod -G grupo1,grupo2 usuario|
|passwd	|N/A	|Cambia la contraseña de un usuario.|	passwd usuario|
|userdel|N/A	|Elimina una cuenta de usuario.|	userdel usuario|
|	|-r	|Elimina el directorio home del usuario.|	userdel -r usuario|
|groupadd|N/A	|Crea un nuevo grupo.|	groupadd nuevo_grupo|
|groupdel|N/A	|Elimina un grupo existente.|	groupdel grupo|
|gpasswd|N/A	|Administra el archivo /etc/group.|	gpasswd -a usuario grupo|
|	|-a	|Añade un usuario a un grupo.|	gpasswd -a usuario grupo|
|	|-d	|Elimina un usuario de un grupo.|	gpasswd -d usuario grupo|

> [!NOTE]
> El comando ls -l en Linux muestra una lista detallada de los archivos y directorios en el directorio actual. Cada columna en la salida tiene un significado específico:
> - Permisos: Indica los permisos de lectura, escritura y ejecución para el propietario, el grupo y otros usuarios. El primer carácter indica el tipo de archivo (por ejemplo, - para archivos regulares, d para directorios).
> - Número de enlaces: Muestra el número de enlaces duros al archivo o directorio.
> - Propietario: Indica el nombre del usuario propietario del archivo o directorio.
> - Grupo: Indica el nombre del grupo propietario del archivo o directorio.
> - Tamaño: Muestra el tamaño del archivo en bytes.
> - Fecha y hora de la última modificación: Indica cuándo fue la última vez que se modificó el archivo o directorio.
> - Nombre del archivo o directorio: Muestra el nombre del archivo o directorio.

Con respecto al almacenamiento, la gestión del sistema archivos se realiza utilizando una estructura de datos propia de los sistemas operativos tipo Unix llamada **inodos**.

Un inodo es como una ficha de información sobre un archivo o directorio en un sistema de archivos de Linux. ***No contiene los datos del archivo, sino información sobre el archivo.*** Cada archivo o directorio tiene su propio inodo, identificado por un número único. De esta manera existen dos tipos de enlaces en Linux:
- Enlace duro (Hard Link):
  - Son referencias directas al mismo inodo.
  - Varios nombres de archivo pueden apuntar al mismo inodo.
  - Si eliminas un nombre, los datos no se borran hasta que se eliminen todos los enlaces duros.
- Enlace blando (Soft Link ó Symbolic Link):
  - Son archivos especiales que contienen una ruta hacia otro archivo o directorio.
  - Funcionan como accesos directos.
  - Si eliminas el archivo original, el enlace simbólico se rompe y apunta a un destino inexistente.
Es decir: Los enlaces duros comparten el mismo inodo que el archivo original. Todos los nombres (enlaces duros) que apuntan al mismo inodo son equivalentes mientras que los enlaces blandos tienen su propio inodo y contienen una ruta al archivo original. No comparten el inodo con el archivo al que apuntan.

Partiendo del directorio raíz ```/``` están todas las carpetas y estructura del sistema operativo:

| Carpeta | Descripción |
| --- | --- |
| /bin | Estático y compartido, contiene archivos binarios ejecutables necesarios para el funcionamiento del SO. Estos archivos los pueden usar todos los usuarios. NO PUEDE CONTENER SUBDIRECTORIOS |
| /boot | Estático y no compartible, contiene todos los archivos necesarios para el arranque del ordenador excepto los archivos de configuración |
| /dev | Aqui estarán los dispositivos, a los que unix trata como un archivo |
| /etc | Directorio estatico con archivos de configuración del sistema operativo y diversos programas |
| /home | Variable y compartible donde se encuentran los ficheros de todos los usuarios salvo root. Cada usuario tendrá su carpeta en /home |
| /lib | Estático y compartible. Contiene bibliotecas necesarias para ejecutar los ejecutables de /bin y /sbin. Tambien contiene módulos kernel y controladores necesarios durante el arranque y funcionamiento del SO |
| /mnt | Alberga los puntos de montaje de los diferentes dispositivos |
| /media | Similar a /mnt. Punto de montaje de medios extraibles |
| /opt | Estático y compartible. Almacena programas que no vienen con nuestro SO y no siguen estándares para almacenar en /usr |
| /proc | Sistema de archivos virtual que proporciona info de procesos y aplicaciones por cada proceso existe un subdirectorio. Esta carpeta está en la RAM |
| /root | Variable y no compartible. Es el /home del usuario root |
| /sbin | Estático y compartible. Similar a /bin pero su contenido sólo puede ser usado por root |
| /srv | Almacena datos y directorios que usan los servidores instalados en el equipo (p.ej. ftp, servidor web...|
| /tmp | Aqui se crean y almacenan los archivos temporales. Se vacía con cada reinicio |
| /usr | Compartido y estático. Contiene la mayoría de los programas instalados en el equipo. Accesible solo de lectura para todos los usuarios |
| /var | Archivos de datos variables y temporales como logs, cache, etc. |
| /sys | Similar a /proc. Información sobre el kernel, particiones,sistemas de archivo... |
| /lost+found | Se crea después de ejecutar herramioentas para restaurar y recuperar (p.ej. ```fsch```) |
