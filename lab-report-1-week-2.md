# Lab Report 1
> Tutorial of how to log into a course-specific account on ieng6

## First step: Installing VScode
* VS code is a useful tool that we can use  terminal or modify files by coding on it.
1. search VS code in google, then click the _download_ button;
2. download the version you need.(windows, linux, Mac)
3. Once you done, it should be look like the image below:

![Image](report1Image\vsCodeDownload.png)

## Second step: Remotely Connecting
* There are diferent course-specific accounts for different courses.In order to connect our computer with the remote computer over the internet (or connect to the "server"), we need to use a program called openSSH.
1. Download OpenSSH from google.
2. Find our specific user name for the specific course.
3. Before we start, remember to reset our password for the course; then, in terminal, use `ssh cs15lsp22zz@ieng6.ucsd.edu`(replace zz with specific username) and password to connect. once we done, it should be like:

![Image](report1Image\Remotely-Connecting.png)

## Third step: Trying Some Commands
* There are diferent ssh commands we can use to access firectories or files.
1. `cd ~`: go to the first folder in path
2. `cd path` go to a specific folder in this folder
3. `ls` list all folder&file in this folder
4. `ls -a` list files include the hidden file
5. `cp path` copy
6. `cat path` show contents 

Example of command: ls

![Image](report1Image\Remotely-Connecting.png)

## Forth step: Moving Files with scp
* By using scp, we can copy files from our computer to server
1. Create a file .java in our local machine
2. then use `scp fileName cs15lsp22zz@ieng6.ucsd.edu:~/` , replace zz with our user name
3. login to server, we can run this file with javac and java

![Image](report1Image\Moving_Files_with_scp.png)

## Fifth step: Setting an SSH Key
* It is unconvenient to login with typing our password everytime; but we can use `ssh-keygen` to login without our password safely.
1. input `ssh-keygen` in terminal, and keep clicking 'enter' on keyboard.
2. if you are windows: `Get-Service ssh-agent | Set-Service -StartupType Manual`
    * `Start-Service ssh-agent`
    * `Get-Service ssh-agent`
    * `ssh-add zz\.ssh\id_ed25519` (find ssh path and replace zz with it)
3. go back to server:input `mkdir .ssh` then logout
4. in your computer: `scp /Users/<user-name>/.ssh/id_rsa.pub cs15lsp22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys` replace username

![Image](report1Image\Setting_an_SSH_Key.png)

## Sixth step: Optimizing Remote Running
* We can use some sort of "shortcut" to make remote running even more pleasant
1. ssh cs15lsp22akt@ieng6.ucsd.edu "ls"

![Image](report1Image\multipleCommands.png)
