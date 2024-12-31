# /etc/shadow Privilege Escalation.
If we can read the `/etc/shadow` file we can try to crack the hashes from the users.

## Detection.
In the next scenario we can see that we have reading privileges for the `/etc/passwd` file.
<p align="center">
  <img src="https://github.com/user-attachments/assets/e252761a-e5b3-4d76-bb94-9bb9a6ca0db7" width="800"><br />
</p>


![38](https://github.com/user-attachments/assets/eea6215f-6e48-4e36-8e5c-39567489ffd1)


## Exploitation.
### Obtaining the hashes.
We need to get the line on `/etc/shadow` of the user we want to crack:
![45](https://github.com/user-attachments/assets/07fc3597-90d5-4196-a729-831657aeaff2)
![46](https://github.com/user-attachments/assets/e2544b49-3ac7-4274-a05b-86d946a87d7f)

And we do the same with `/etc/passwd`: 
![55](https://github.com/user-attachments/assets/e4ee3b98-bef4-4beb-bccc-407e64cc0633)

We have to send the files back to our system. To do so, we can use different techniques depending on the situation we are facing.


## Unshadowing 
Once in our Attacker machine we have to unshadow the files as follows: 
![56](https://github.com/user-attachments/assets/748983c4-ece2-42ee-807d-54c716046407)

## Cracking hashes.
Finally we will make the brute force using `john`.
![51](https://github.com/user-attachments/assets/b4ed82e7-3ccd-4a74-8713-e1dfbc17ed31)

![52](https://github.com/user-attachments/assets/70c73f84-2f6a-4c47-a2e9-ae07516859f5)




