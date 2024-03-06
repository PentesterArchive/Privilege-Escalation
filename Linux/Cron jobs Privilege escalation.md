# Cron jobs enumeration
`crontab -l` -> This command lists our user cron jobs.<br />
`cat /etc/crontab` -> Displays the contents of the /etc/crontab file, which contains scheduled tasks.<br />
`ls -la /etc/cron*` ->  Lists files and directories in the /etc directory starting with "cron".<br />

# Cron jobs exploitation
## Cron jobs exploitation 1
If our current user can access a cron script and we can modify it, we can perform any action as if the script<br />
executor were doing it. <br />
Using this technique we can easily create a reverse shell.[Reverse shell](https://github.com/alejandro-pentest/Fundamentals/blob/main/Reverse%20shells.md)

## Cron jobs exploitation 2
In some situations we can find an existing cron job where the script is deleted.
If the full path of the script is not defined cron will refer to the paths listed under the PATH variable <br />
in the /etc/crontab file. In this case, we should be able to create a script under our user’s home folder<br />
and it should be run by the cron job owner.


<img src=https://github.com/alejandro-pentest/Privilege-Escalation-Cheat-sheet/assets/161533623/5e0a3d91-a4ed-4fd4-9216-dd247cb8dd06 width="100" height="100">
