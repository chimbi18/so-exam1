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
