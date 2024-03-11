# doas Privilege escalation.
Doas ***executes arbitrary commands as another user***. It's similar to sudo command. doas.conf is interesting to privilege escalation.

## Doas enumeration: 
First of all, search location of doas.conf.<br />
`find / -type f -name "doas.conf" 2>/dev/null`<br />
After that we can check the configuration.<br />
`cat /etc/doas.conf` <br /><br />
<img src="https://github.com/alejandro-pentest/Privilege-Escalation-Cheat-sheet/assets/161533623/c94fa90a-9009-48c9-b15b-ca0aa4111677" width="400"><br />

## Doas execution: 
`doas -u root <command> <arg>`

## Doas privilege escalation.
After discovering that our user has a doas assigned. We can refer to [GTFOBins](https://gtfobins.github.io/) and execute the assigned command ***using doas instead of sudo***.
