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
| ` ps [-a\|u\|x]` | -- | ``|
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
