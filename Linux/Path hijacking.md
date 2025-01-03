# Path hijacking
## What is the Path
In Linux, when we run a command, we usually use its relative path. For instance, instead of typing the full path "/usr/bin/whoami", we simply type "whoami" to execute the command. This works because our system knows where to find these commands through the $PATH variable.
![1](https://github.com/alejandro-pentest/Privilege-Escalation-Cheat-sheet/assets/161533623/b67fda05-b174-45ac-8747-1af72d9b3b02)

## Modifying $PATH
We can manipulate the $PATH variable in several ways:
- Adding a directory at the end of the path
`export PATH=$PATH:/usr/local/bin`
- Adding a directory at the beginning of the path:
`export PATH=/usr/local/bin:$PATH`
- Replacing the entire path:
`export PATH=/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin`

## Path Hijacking Privilege Escalation
If we find a script owned by a more privileged user that we can execute, we can exploit path hijacking to escalate privileges. By modifying the $PATH, we can manipulate which commands the script uses. For example, if the script executes whoami, we can change $PATH to `export PATH=/tmp:$PATH` and create a custom whoami script in the `/tmp` directory that gives us elevated privileges `echo "/bin/bash" > whoami`. When we run the script, we will inherit the privileges of its owner.

