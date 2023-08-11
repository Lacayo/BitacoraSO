# Bitácora de Comandos de Sistemas Operativos 2CO23-162013G1
El presente documento corresponde a la bitácora de los comandos vistos durante las clases del curso de Sistemas Operativos de los martes 6 pm del II CO 2023

Para un mejor entendimiento se usará el siguiente marcado para los elementos adicionales a los comandos:

`{}`: Se colocará entre carácteres { y } los argumentos requeridos por el comando. Los mismos se utilizarán para parámetros que son requeridos al incluir una bandera. Ejemplo: `rm {ruta_de_archivo}`

`[]`: Se colocará entre carácteres [ y ] las banderas y los parámetros opcionales del comando. Ejemplo: `cd [ruta_de_directorio]` `openvpn [--config {ruta_de_archivo_configuracion}]`

`|`: Se separarán con | las opciones en un comando que se pueden usar de manera no exclusiva o en combinación. Ejemplo: `ps [-a|u|x]`

`/`: Se separarán con / las opciones en un comando que se pueden usar de manera exclusiva (una u otra, pero no a la vez). Ejemplo: `apt {install / remove}`

`^n`: Se indicará al final de un argumento la cantidad de datos que acepta con la misma función con ^n siendo n la cantidad. Si se coloca ^n explícitamente significa que todos los datos separados por espacio a partir de ese punto funcionan como dicho argumento. Ejemplo: `apt {install {paquete_a_instalar}^n/remove {paquete_a_desinstalar}^n}`

| Comando | Descripción | Ejemplo de uso |
|--|--|--|
| `sudo {comando}` | Ejecuta el comando argumento con permisos de super usuario. La primera vez que se utiliza en una consola solicita credenciales del usuario administrador | `sudo apt update` Actualiza la lista de paquetes del equipo |
| `apt {install {paquete}/remove {paquete}/update/upgrade}` | Este comando corresponde al administrador de paquetes de las distibuciones basadas en Debian. Permite instalar, desinstalar, buscar y actualizar los paquetes en el equipo | `apt install vlc` Instala el paquete de VLC Media Player|
| `neofetch` | Paquete que muestra de forma personalizada la información del sistema como el Kernel, nombre de distribución, CPU, Memoria, etc. | `neofetch` Muestra la información del equipo de forma personalizada |
| `ip {a/address}` | Permite mostrar la información de los adaptadores de red | `ip address` Muestra las direcciones IP de los adaptadores de red conectados. |
| `clear` | Limpia la pantalla de la consola, lo cual elimina todas las salidas de comandos anteriores a clear y el uso de clear en la consola. | `clear` Limpia la consola |
| `pwd` | Muestra la ruta actual en la que se encuentra la consola | `pwd` Imprime la Ubicación actual de la sesión de la consola |
| `ls [-l\|a\|h] [directorio]` | Imprime los contenidos de la carpeta ingresada por parámetro. Si no se coloca parámetro imprime el contenido de la carpeta actual de la consola. Permite usar opciones que despliegan información adicional, filtran u ordenan los archivos listados | `ls -a` Imprime los nombres de todos los archivos y directorios en la carpeta actual|
| `man {command_name}` | Imprime el manual de usuario del comando ingresado por parámetro. Despliega tanto la documentación del comando o paquete como las opciones que tiene disponibles en cuanto argumentos u opciones del comando. | `man apt` Muestra el manual del comando apt |
| `su [usuario]` | Permite ejecutar comandos como otro usuario diferente al de la sesión actual del sistema. Si no se le coloca el argumento de usuario cambiará por defecto al usuario root. | `su root` Pasa a ejecutar comandos como el super usuario (root) |
| `passwd [usuario]` | Permite cambiar las contraseñas de los usuarios. Solo el super usuario puede cambiar las contraseñas de otros usuarios, en caso contrario se cambiará la contraseña del usuario en sesión | `passwd` Cambia la contraseña del usuario actual |
| `whoami` | Muestra el nombre de usuario que se está usando actualmente. | `whoami` Muestra el usuario actual |
| `history` | Muestra el historial de comandos utilizados en la consola en esta y anteriores sesiones con un límite de 1000 comandos, una vez alcanzado ese límite se borran las entradas más antiguas para ingresar los más recientes | `history` Imprime en consola la lista de comandos usados. |
| `nano [archivo]` | Es un paquete que permite la edición de archivos de texto plano por medio de la consola. Si se coloca un archivo por parámetro lo abre y carga el contenido para edición, si no existe o no se coloca un archivo como parametro crea uno nuevo. En caso que no se colocó el nombre del archivo en el parámetro, lo solicita para guardar al final de la edición | `nano autorun.sh` Abre para modificar o crea un archivo autorun.sh |
| `vi` | Hace lo mismo que nano, pero más feo | `vi test.txt` Carga el archivo para editarlo. |
| `cat` | Imprime el contenido de un archivo de texto plano en consola | `cat autorun.sh` Muestra el contenido del archivo autorun.sh sin ejecutarlo |
| `mkdir {ruta_directorio}` | Crea un directorio en la ruta especificada. Si solo se coloca un nombre, se creará una carpeta con ese nombre en el directorio actual de la terminal | `mkdir Lab03` Crea una carpeta llamada Lab03 en la ruta actual de la terminal |
| `cd [ruta]` | Mueve la ubicación actual de la terminal a la ruta especificada. La ruta puede ser el nombre de una carpeta en la ubicación actual o una ruta relativa como .. (carpeta arriba) o ~ (carpeta home del usuario). Si no se le coloca argumento de ruta, usa la ruta de la carpeta home del usuario actual por defecto | `cd Descargas` se mueve a la carpeta llamada Descargas del directorio actual |
| `rm {archivo}` | Elimina el archivo que se encuentra en la ruta o con el nombre que recibe por parámetro si existe en la carpeta actual | `rm Descargas.rar` Borra el archivo comprimido Descargas.rar|
| `cp {archivo_original} {ruta_copia}` | Copia el archivo de la ruta original a la del segundo argumento. En el segundo argumento se le puede colocar un nuevo nombre al archivo o se mantiene el mismo si solo se especifica un directorio | `cp Descargas/Curriculum.docx Documentos/` Copia el archivo Curriculum.docx de la carpeta Descargas a la carpeta Documentos |
| `mv {ruta_original} {ruta_nueva}` | Mueve el archivo en la ruta del primer parámetro a la ubicación del segundo parámetro, ya sea cambiando o manteniendo el mismo nombre al igual que el comando cp | `mv Descargas/índice.png Imágenes/Fondo.png` Mueve el archivo índice.png de la carpeta Descargas a Imágenes y le cambia el nombre a Fondo.png |
| `telnet [open] [host [puerto]]` | Comando para usar la herramienta de comunicación Telnet que permite probar conexiones y enviar datos entre equipos. Si se utiliza solo el comando telnet, abrirá una consola donde se pueden utilizar variedad de comandos como auth, display, open, close para manejar la comunicación con equipos. También se pueden utilizar directamente estas opciones al colocar la acción después del comando. Si se llama telnet con una dirección de dominio o IP, opcionalmente agregándole puerto, utilizará por defecto la acción open para crear una conexión con el equipo y enviar datos. | `telnet 192.168.0.25 22` Se conecta al puerto 22 del equipo con la IP 192.168.0.25 en la red local |
| `top` | -- | ``|
| `htop` | -- | ``|
| `tree` | -- | ``|
| `ps [-a\|u\|x]` | -- | ``|
| `python3` | -- | ``|
| `chmod` | -- | ``|
| `dmidecode` | -- | ``|
| `free [-h\|b/k/m/g]` | | ``|
| `swapon` | -- | ``|
| `sysctl` | -- | ``|
| `mount` | -- | ``|
| `scp` | -- | ``|
| `git` | -- | ``|
| `grep` | -- | ``|
| `find` | -- | ``|
| `wget` | -- | ``|
| `nmap` | -- | ``|
| `nslookup` | -- | ``|
| `zip` | -- | ``|
| `unzip` | -- | ``|
| `curl [-X {GET/POST/DELETE}] [-P {puerto}] [-L]` | Herramienta para transferir datos hacia un servidor. Permite usar diferentes protocolos como HTTP, HTTPS, FTP, DICT, etc. Incluye una amplia variedad de opciones como elegir el puerto (-P), el método HTTP que se usará (-X) o incluso si debe ser sensible a que la dirección utilizada indique un cambio de url | `curl -L google.com` Obtiene los datos que devuelve la dirección de google.com admitiendo redireccionamiento de los recursos. |
| `pacman {-D/Q/S[y] [paquete]/R}` | Comando correspondiente al administrador de paquetes de las distribuciones basadas en Arch Linux. Realiza operaciones como actualizar, instalar y desinstalar paquetes en la distribución | `sudo pacman -Sy` Actualiza la lista del paquetes del equipo |
| `yay {-Y/B/P/G/W/S {paquete}}` | yay es un asistente de Pacman que permite instalar paquetes del Arch User Repository (AUR), por lo tanto tiene sus propias opciones, pero se extiende de Pacman como la operación -S para instalar paquetes. Por defecto si solo se usa `yay` usará la opción -Y | `sudo yay -S google-chrome` Instala el paquete de Google Chrome desde el AUR |
| `systemctl {status/start/stop} {servicio}` | Este comando funciona para administrar los servicios del sistema operativo con operaciones para iniciar (start), detener (stop) o verificar el estado (status), entre otras. | `sudo systemctl start httpd` Inicia el servicio de Apache que muestra una página en localhost |
| `{comando_con_salida} > {ruta_archivo}` | -- | ``|
| `uname [-a/(s\|n\|r\|v\|m\|p)]` | Muestra cierta información del sistema como el nombre, version o release del kernel. La opción -a muestra todo, mientras que las otras corresponden a datos específicos | `uname -a` Muestra todos los datos del sistema disponibles en el comando |
| `useradd [-m {nombre_usuario}] [-G {grupo}] [-p {clave}]` | Crea un usuario nuevo asignandole nombre, grupo y clave | `useradd -m pepe -G clients -p elpepe` Crea un nuevo usuario llamado pepe, asignado al grupo clients y con la clave elpepe |
| `chown {usuario} {ruta}` | Cambia el usuario dueño de una carpeta o archivo | `chown pepe /home/admin/carpetapepe` Cambia el dueño de una carpeta ubicada en la carpeta home del usuario admin|
