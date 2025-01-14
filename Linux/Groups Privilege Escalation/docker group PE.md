# Docker Group Privilege Escalation.
If we are part of the Docker group we can do the next command to become root.

![31](https://github.com/user-attachments/assets/b7c9043b-0bf6-42ec-91cb-15c7dbd6710f)

```bash
docker run -it --rm -v /:/mnt <IMAGE_NAME> chroot /mnt bash
```

- docker run: This runs a new container from an image.
- -it: This flags allow you to run the container interactively (-i) and allocate a terminal (-t).
- --rm: Automatically removes the container when it exits.
- -v /:/mnt: This mounts the root directory (/) of your host machine to the /mnt directory inside the container.
- chroot /mnt bash: This changes the root filesystem of the container to /mnt (which is the root of your host machine, since it’s mounted) and then executes the bash shell.


This command will allow you to execute a chroot inside the Docker container, with the root filesystem being that of your host. <br />
Where `<image_name>` should be replaced with the actual image name you want to use (for example, ubuntu or debian), pentesters often use `alpine` which is an extremely lightweight distribution. 
Its base Docker image is only around 5 MB in size.


![32](https://github.com/user-attachments/assets/860c572c-1e44-4ccc-bef2-b5c6592617b4)




![33](https://github.com/user-attachments/assets/df22a0d9-6d89-46e2-a396-7ab4edc3a53a)

