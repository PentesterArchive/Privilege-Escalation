# NFS Privilege Escalation
## How does it work?
NFS privilege escalation involves _exploiting misconfigured NFS shares by mounting them locally_, manipulating files or directories within the share to gain unauthorized access or escalate privileges.
In this example **we will create a shared suid script owned by our local system root, when we execute it in the target machine we will get root priviliges in the target too.**

## Enumeration.
The `/etc/exports` file controls which file systems are exported to remote hosts and specifies options, we will execute it in the target machine. For the nfs privilege escalation we have to check for the no_root_Squash options.
![1](https://github.com/alejandro-pentest/Privilege-Escalation-Cheat-sheet/assets/161533623/c2c53348-0fd8-41a1-a8ad-479f14e3123b)
In our machine we can check the file systems exported by the target running `showmount -e <TargetIP>`.
![`2](https://github.com/alejandro-pentest/Privilege-Escalation-Cheat-sheet/assets/161533623/585db69d-4045-4620-ae4d-c40c247543b2)

## Mounting.
To do the mounting we have to choose a folder in our local machine and run `mount -o rw <TargetIP>:<TargetMountFolder> <OurFolder>`
![3](https://github.com/alejandro-pentest/Privilege-Escalation-Cheat-sheet/assets/161533623/04064d0f-fa94-4438-9f51-dacdd6d8165e)
After that all the files we create in our local system will be shared with the target.

## Privilege Escalation.
After this process we have to create a script [C PivEsc Script](https://github.com/alejandro-pentest/Fundamentals/blob/main/Privilege%20Escalation%20Code.md) _It's important to be root_ and give the rigth permissions `chmod +xs <script>`. When we go back to the target machine we can run it and check our privileges.
