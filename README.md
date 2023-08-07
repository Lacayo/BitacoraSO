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
| `apt` | -- | ``|
| `neofetch` | -- | ``|
| `ip a` | -- | ``|
| `clear` | -- | ``|
| `pwd` | -- | ``|
| `ls [-l]` | -- | ``|
| `man {command_name}` | -- | ``|
| `su root` | -- | ``|
| `passwd` | -- | ``|
| `whoami` | -- | ``|
| `history` | -- | ``|
| `nano` | -- | ``|
| `vi` | -- | ``|
| `cat` | -- | ``|
| `mkdir` | -- | ``|
| `cd` | -- | ``|
| `rm` | -- | ``|
| `cp` | -- | ``|
| `mv` | -- | ``|
| `telnet` | -- | ``|
| `top` | -- | ``|
| `htop` | -- | ``|
| `tree` | -- | ``|
| `ps [-a\|u\|x]` | -- | ``|
| `python3` | -- | ``|
| `chmod` | -- | ``|
| `dmidecode` | -- | ``|
| `free` | -- | ``|
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
| `pwd` | -- | ``|
| `curl [-X {GET/POST/DELETE}] [-P {puerto}] [-L]` | Herramienta para transferir datos hacia un servidor. Permite usar diferentes protocolos como HTTP, HTTPS, FTP, DICT, etc. Incluye una amplia variedad de opciones como elegir el puerto (-P), el método HTTP que se usará (-X) o incluso si debe ser sensible a que la dirección utilizada indique un cambio de url | `curl -L google.com` Obtiene los datos que devuelve la dirección de google.com admitiendo redireccionamiento de los recursos. |
| `pacman {-D/Q/S[y] [paquete]/R}` | Comando correspondiente al administrador de paquetes de las distribuciones basadas en Arch Linux. Realiza operaciones como actualizar, instalar y desinstalar paquetes en la distribución | `sudo pacman -Sy` Actualiza la lista del paquetes del equipo |
| `yay {-Y/B/P/G/W/S {paquete}}` | yay es un asistente de Pacman que permite instalar paquetes del Arch User Repository (AUR), por lo tanto tiene sus propias opciones, pero se extiende de Pacman como la operación -S para instalar paquetes. Por defecto si solo se usa `yay` usará la opción -Y | `sudo yay -S google-chrome` Instala el paquete de Google Chrome desde el AUR |
| `systemctl {status/start/stop} {servicio}` | Este comando funciona para administrar los servicios del sistema operativo con operaciones para iniciar (start), detener (stop) o verificar el estado (status), entre otras. | `sudo systemctl start httpd` Inicia el servicio de Apache que muestra una página en localhost |
| `{comando_con_salida} > {ruta_archivo}` | -- | ``|
| `uname [-a/(s\|n\|r\|v\|m\|p)]` | Muestra cierta información del sistema como el nombre, version o release del kernel. La opción -a muestra todo, mientras que las otras corresponden a datos específicos | `uname -a` Muestra todos los datos del sistema disponibles en el comando |
| `useradd [-m {nombre_usuario}] [-G {grupo}] [-p {clave}]` | Crea un usuario nuevo asignandole nombre, grupo y clave | `useradd -m pepe -G clients -p elpepe` Crea un nuevo usuario llamado pepe, asignado al grupo clients y con la clave elpepe |
| `chown {usuario} {ruta}` | Cambia el usuario dueño de una carpeta o archivo | `chown pepe /home/admin/carpetapepe` Cambia el dueño de una carpeta ubicada en la carpeta home del usuario admin|
