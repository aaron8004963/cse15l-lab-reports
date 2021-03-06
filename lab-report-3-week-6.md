# Lab Report 3
> implement all group choice options from lab 5

## Option 1: Streamlining ssh Configuration

### Screenshot of the .ssh/config file
![Image](report3Image\ConfigEditing.png)

### Screenshot of ssh command logging 
![Image](report3Image\loginWithIeng6.png)

### Screenshot of scp with alias
![Image](report3Image\scpWithAlie.png)

## Option 2: Setup Github Access from ieng6

### public key I made is stored on Github
![Image](report3Image\pubKeyInGithub.png)

### public and private key I made in user account
![Image](report3Image\successfulPush.png)
![Image](report3Image\privateKey&puclicKeyInUserAcc.png)

### running git commands to commit and push a change to Github while logged in
![Image](report3Image\successfulPush.png)

### Link of that commit
[Iink to resulting commit](https://github.com/aaron8004963/markdown-parser/commit/926a98dd715855f72306302155ebadd0be165e52)

### Describing
This option enable us to use push from the command line in server. What we need to do is copy the public key to github account - setting - add new shh key. Then, while logged in server, after editing some file and committing(before commiting, we need to use "add filename" to add the file which nedded to be commit), then we will be able to use "git push origin main" to push a change"

## Option 3 Copy whole directories with scp -r
### copying my whole markdown-parse directory to your ieng6 
![Image](report3Image\copyingWholeDirectory.png)

### logging into your ieng6 account after doing this and compiling and running the tests for your repository
![Image](report3Image\compilelingAndRunTests.png)

### combining scp, ;, and ssh to copy the whole directory and run the tests in one line
![Image](report3Image\combineAndTest.png)

### Describing
This option allowed us to copy whole directory with "scp -r". And this command is also allowed use combination of ";" and "ssh"