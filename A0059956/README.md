### Examen 1
**Universidad ICESI**  
**Curso:** Sistemas Operativos  
**Estudiante:** Victor Andres Calambas Hurtado  
**Código:** A00059956  

**DESCARGA DE INSTALACIÓN DEBIAN 9**

Primero descargamos la imagen ISO de Debian 9.4 release que es la última versión, para el sistema operativo con arquitectura amd-64.
Segundo descargamos el programa MD5_and_SHA_Checksum_utility para realizar la verificación de la imagen ISO descargada el en primer paso.
Tercero procedemos a cargar la imagen del debian en formato .iso para realizar la verificación de los parámetros de los hash generados de los archivos con los originales de la pagina https://cdimage.debian.org/debian-cd/current/amd64/iso-cd/ Se verifico el MD5SUMS, SHA1SUMS,SHA256SUMS,SHA512SUMS


**INSTALACIÓN DEL SISTEMA OPERATIVO DEBIAN SERVER 9**

La instalación se inicia abriendo virtualBox y se añade el nuevo disco virtual dando click en nueva, luego escribimos el nombre del sistema operativo y seleccionamos el sistema operativo de la máquina que vamos a crear y el sistema operativo que vamos a usar y le damos click en siguiente.

Luego de hacer lo anterior seleccionamos el tamaño de la memoria Ram que asignaremos a nuestra nueva máquina. De acuerdo a las especificaciones de mi computador le asigne 512 Mb y damos click en siguiente. Luego seleccionamos la opción de crear un disco virtual y se crea, le deje el tamaño que viene por defecto fue de 8 GB y con ello creamos el nuevo disco duro virtual seleccionando la opción de VirtualBox Disk Image y posteriormente seleccionamos la opción de memoria fija que es la opción de "fixed size" luego damos click en la opción de crear. Con esta configuración estará lista la unidad virtual para ser arrancada luego.

Cuando este la configuración en el menú de de las máquinas que tenemos procedemos a seleccionar la unidad de disco, damos click derecho y seleccionamos la opción de iniciar, para correr la unidad virtual, cuando arranca la unidad virtual de forma correcta seleccionamos opción de instalar y seleccionamos el idioma deseado, el país o la región, y luego la configuración que deseamos definir al teclado, se solicita la configuración de red pero se dejó vacía esta opción. Luego creamos un usuario con una contraseña y confirmamos la contraseña, luego se selecciona la	zona horaria y se desplegará una ventana que muestra varias opciones de particionamiento del disco, seleccionamos la opción por defecto y continuamos la instalación, luego se elige el disco duro al que que se le va a realizar la instalación y damos click en el botón de continuar, seleccionamos la primera de las tres opciones, la que viene por defecto que consiste en todos los archivos en una sola partición  y continuamos dando Si a todas las otras opciones para que el instalador de forma automática termine el proceso de instalación de la configuración definida del sistema operativo, y luego automáticamente se descarga toda los complementos necesarios para que funcione el sistema operativo, luego seleccionamos el disco duro en el que vamos a instalar y posteriormente se habrá acabado la instalación y se finaliza con el reinicio de la máquina que creamos.


**CONFIGURACIÓN DE INTERFAZ PRIVADA**

Accedemos a la máquina virtual debian desde el virtualBOx y accedemos a la terminal para conocer la ip con el comando "ip a" el cual mostró una ip 192.168.1.52
Luego procedemos a abrir el MTPutty y seleccionamos la opción de añadir servidor e ingresamos en el nombre la ip que fue mostrada por el Debian con el comando anterior, y adicionalmente añadimos al campo del puerto el número 22, y el protocolo de comunicación SSH , adicionalmente agregamos la contraseña y el usuario que creamos en la instalación de Debian es opcional, los datos correspondientes a la máquina virtual son **usuario :** chimbi y **Contraseña:** 19970718chimbi , luego de haber realizado esta configuración procedemos a iniciar en MTPutty la sesión correspondiente a la IP.

**INSTALACIÓN DE GIT Y TIG**

Utilizamos el comando apt-get install git para la instalación de git 
Luego utilizamos el comando apt-get install tig para la instalación de tig.

Para obtener la evidencia de la instalación clonamos el repositorio al que estamos realizando los commits https://github.com/chimbi18/so-exam1.git y luego de que se haya clonado accedemos a la carpeta en la que estamos trabajando, nos movemos en la carpeta con el comando cd so-exam1/ y una vez ubicados en este directorio escribimos el comando **tig** para que nos muestre en la pantalla los commits que se han realizado.

**EXPORTACIÓN DE MAQUINA VIRTUAL**

Para la exportación de la máquina virtual en el VirtualBox seleccionamos en la pestaña de archivo la opción de exportar servicio virtualizado, y seleccionamos la máquina virtual que vamos a exportar que en el caso se llama Debian 9, damos click en siguiente y elegimos la ubicación en que queremos que guardar la máquina exportada, damos click exportar y esperamos que complete el proceso de exportación en el lugar definido.

**IMPORTACIÓN DE MÁQUINA VIRTUAL**
Abrimos VirtualBox seleccionamos la pestaña archivo y luego importar servicio virtualizado, luego buscamos la dirección en que se encuentra la unidad virtual exportada , damos click en siguiente y luego en el botón de importar y luego esperamos que cargue y posteriormente podemos inicializar la máquina virtual en cualquier otro computador

**CUADRO COMPARATIVO**

 **CentOS7** | **Debian 9** | **Explicacion**
 --- | --- | ---
 Peso mayor | Peso menor | Debian 9 es mejor debido a que trata de instalar solo lo más necesario
Mayor consumo de Disco duro| Menor consumo de disco duro |al no instalar paquetes que no usaremos jamás debian, se ahorra bastante espacio.
Es más usada que Debian | Es menos usada que CentOS 7 | CentOS7 es más usada por que cuenta con el respaldo de una compañia RedHat Enterprise
Actualización más complicada | Actualización más facil | la misma pagina de CentOS para actualizaciones prefiere que se instalen cosas desde cero e incluso en las instrucciones de hacer un upgrade te desea mucha suerte
Es una de las distribuciones más estables al igual que Debian|Es una de las distribuciones más estables al igual que CenOS7 | son versiones muy estables por que las empresas tienen el proposito de probar todo
frecuencia de actualizaciones menor Apache -> 2.2.15 PHP -> 5.3.3 MySQL -> 5.1.66 PostgreSQL -> 8.4.13 | frecuencia de actualizaciones mayor Apache -> 2.2.22 PHP -> 5.4.4 MySQL -> 5.5.30 PostgreSQL -> 9.1.9 | las frecuencias de actualización más recientes las tiene Debian debido a que por lo general tiene las versiones más recientes
tamaño instalador mayor|tamaño instalador menor| la diferencia entre los instaladores es de varias Gb favoreciendo a Debian en cerca de 4Gb de diferencia
Consume Ram y Procesador obligatoriamente por la GNU|ventaja de trabajar mediante mucho SSH porque puede usar menor recursos d eRAM y Proecesador al no usar interfaz| Debian supera a CentOS porque no instala un entorno gráfico por defecto 
utiliza un package manager Yum y la funcion yum install es más lento que el de debian| el package manager “apt-get install && apt-get upgrade”  es más rapido | son más rapidos los procesos de Instalacion del Debian que el CentOS7 en la instalacion de paquetes y actualizaciones porque descaga solo lo necesario

