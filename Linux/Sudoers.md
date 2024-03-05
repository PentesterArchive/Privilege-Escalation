`sudo -l` -> When you run sudo -l, it checks the sudoers configuration file (typically located at /etc/sudoers)<br />
to determine what commands the current user is allowed to run with elevated privileges.<br />
After that we can try to check [gtfobins](https://gtfobins.github.io/) to see if we can obtain a shell, read a file or execute some interesting <br />
commands as the sudo user.

## /etc/sudoers
"If we have sufficient permissions, we can attempt to modify the /etc/sudoers file to gain additional privileges."
`user ALL=(ALL:ALL) ALL`



