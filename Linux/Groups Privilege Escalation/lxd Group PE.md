# lxd Group Privilege Escalation.
## Automated method:
First of all we have to check the user group:<br />
![1](https://github.com/alejandro-pentest/Privilege-Escalation-Cheat-sheet/assets/161533623/36673518-cb7c-43ac-afe9-b8bad9ea132c)<br />

After cheking that we are in the `lxd` group we proceed to download the searchsploit script `Ubuntu 18.04 - 'lxd' Privilege Escalation`.
***It's important to delete the next command because it sometimes produce an error.***
<img src="https://github.com/alejandro-pentest/Privilege-Escalation-Cheat-sheet/assets/161533623/5ebc1826-59dc-4292-ac81-c0be52e47bc6" width="600">
<img src="https://github.com/alejandro-pentest/Privilege-Escalation-Cheat-sheet/assets/161533623/88ba5984-4032-4fb7-bc84-5180d03c07dc" width="600">

## Script steps:
- Step 1: Download build-alpine => wget https://raw.githubusercontent.com/saghul/lxd-alpine-builder/master/build-alpine [Attacker Machine]
- Step 2: Build alpine => bash build-alpine (as root user) [Attacker Machine]
- Step 3: Run this script and you will get root [Victim Machine]
<img src="https://github.com/alejandro-pentest/Privilege-Escalation-Cheat-sheet/assets/161533623/b07cbd83-094f-426a-9069-987a2a149e67" width="800">
  
- Step 4: Once inside the container, navigate to /mnt/root to see all resources from the host machine
<img src="https://github.com/alejandro-pentest/Privilege-Escalation-Cheat-sheet/assets/161533623/31153602-2034-4725-b638-da1b2a877c8a" width="800">




