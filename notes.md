### Room : https://tryhackme.com/room/recovery
---
### Flag 0 :

```console
ssh alex@MACHINE_IP "/bin/bash"
```
moving `.bashrc` to `.bashrc.backup` and from it removing the `while` loop. And then moving again to `.bashrc` from `.bashrc.backup`.

We get the first flag.

---
### Flag 1 :

When we are logging in we are automatically logged out by the ssh session that is strange thing. 
But we can do one thing, we can use `pspy64` tool that show us the processes which are running in the background. 
So we will transfer the `pspy64` tool first to victim's machine via simple python server and then we can change the permissions of the `pspy64` to executable and will run that script. 
So we get the information about the script which is in `/opt` directory called `brilliant_script.sh` which is running in the background kills the processes which are related to bash via for loop present in the script and also we have the write permissions so we can easily use a reverse shell oneliner in place of for loop present. 
So I did that I got a reverse shell back. And then I got the second flag.

---

### Flag 2 :

As the message was given to fix the `fixutil` binary so I transferred that binary to my local machine for analyzing via Ghidra. 
While analyzing it I got to know about two bianries which are located in `/bin` directory and in the `/lib/x86_64-linux-gnu` directory which are named as `admin` and `liblogging.so`. 
So I transferred that both binary to my local machine and after analyzing the binaries I came to know about the `cron jobs` which is running by a `root` user by transferring their `authorized keys` in the `ssh` directory and adding the user to `/etc/passwd` as `UID=0`. 
Also it is confirmed that the bash file named `brilliant_script.sh` is involved in the getting the root shell. 
So as I have added bash oneliner in that bash script I got the root shell in some minutes.
And boom I got the third flag.

---

### Flag 3 :
When I analyze the two binaries I also notice that the attacker echoed his public key in the `authorized_keys`. 
So when I removed that public key I got the fourth flag.

---

### Flag 4 :

I created a private and public key pair in my local machine and I echoed public key over the root's `authorized_keys` directory and I was successfully logged in the ssh session of root by using the private key. 
After that I removed the user named security which possess the `UID=0` as per the analysis of the binaries from the `/etc/passwd` and `/etc/shadow` file and boom I got the fifth flag.

---

### Flag 5 :

As per the analysis of the binary there is one backup.txt file in the `/opt/.fixutil` directory where the backed up key was stored.
And also when we look at the main page it is some gibberish weird things written over there. 
So I used the find command to find the path of the main page and I made a tar file of all the files which are present in the `/usr/local/apache2/htdocs` in one single file and I transferred the same to my local machine and I untar the file. Also from the analysis of the binary we can get an idea that string is a `XOR` and we need a key for that. 
So I visited the `/opt/.fixutil/backup.txt` and I found out the key. 
So for the XOR decryption I used this key `AdsipPewFlfkmll` to decrypt the files content using `CyberChef`. 
( https://gchq.github.io/CyberChef/#recipe=XOR(%7B'option':'UTF8','string':'AdsipPewFlfkmll'%7D,'Standard',false ) . 
And after decryption of all the files, I got the final flag.

---
