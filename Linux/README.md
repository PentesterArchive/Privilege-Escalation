# Post-explotation basic enumeration.<br />
### User enumeration<br />
`uname -a` -> It will return the hostname of the target machine, kernel version, architecture...<br />
`id` -> The id command will provide a general overview of the user’s privilege level and group memberships.<br />
### Groups enumeration<br />
`groups <user>`-> Ver el grupo del usuario que indiquemos.<br />

## Interesting Post-explotation files.<br />
`cat /etc/passwd` -> <br />
`cat /etc/shadow` -> <br />
`cat /etc/*issue` -> Identifies the sistem version.<br />
`cat /etc/*release` -> Muestra aún mas información que el comando anterior sobre la distribución.<br />
`cat /proc/version` -> Looking at /proc/version may give you information on the kernel version and additional data such as whether a compiler is installed.<br />
`cat /etc/issue` -> This file usually contains some information about the operating system.<br />

### Net enumeration<br />
#### Netstat<br />
`netstat -a` -> Shows all listening ports and established connections.<br />
netstat -at or netstat -au can also be used to list TCP or UDP protocols respectively.<br />
`netstat -l` -> List ports in “listening” mode. These ports are open and ready to accept incoming connections.<br />
`netstat -tp` -> List connections with the service name and PID information.<br />
`netstat -i`: Shows interface statistics.<br />
`netstat -ano`:<br />
    -a: Display all sockets<br />
    -n: Do not resolve names<br />
    -o: Display timers<br />
`ip route`<br />
`cat /etc/networks`<br />
`cat /etc/hostname`<br />
`cat /etc/hosts`<br />


## Ps (Process Status).<br />
`ps -A` -> View all running processes.<br />
`ps axjf` -> View process tree (see the tree formation until ps axjf is run below)<br />
`ps aux` -> The aux option will show processes for all users (a), display the user that launched the process (u), and show processes that are not attached to a terminal (x). Looking at the ps aux command output, we can have a better understanding of the system and potential vulnerabilities.<br />

## Otros<br />
`lscpu` -> Shows CPU info.<br />
`dpkg -l` -> Muestra los paquetes instalados en el sistema y sus respectivas versiones.<br />
`df -h` -> El comando df **es la forma abreviada del disk filesystem**, este comando nos mostrará los discos conectados al sistema. El parámetro -h hará que la salida sea human readable.<br />






    
