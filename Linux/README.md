# Post-explotation enumeration.
`uname -a` -> It will return the hostname of the target machine. In some cases, it can provide information about the target system’s role within the corporate network.<br />
`cat /etc/issue` -> Identifies the sistem version.<br />
`cat /etc/*release` -> Muestra aún mas información que el comando anterior sobre la distribución.<br />
`lscpu` -> Muestra información de la CPU.<br />
`df -h` -> El comando df **es la forma abreviada del disk filesystem**, este comando nos mostrará los discos conectados al sistema. El parámetro -h hará que la salida sea human readable.<br />
`dpkg -l` -> Muestra los paquetes instalados en el sistema y sus respectivas versiones.<br />
`cat /proc/version` -> Looking at /proc/version may give you information on the kernel version and additional data such as whether a compiler is installed.<br />
`cat /etc/issue` -> This file usually contains some information about the operating system.<br />
