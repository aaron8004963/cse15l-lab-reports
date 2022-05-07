# Lab Report 3
> implement all group choice options from lab 5

## Streamlining ssh Configuration

### Screenshot of the .ssh/config file
![Image](report3Image\ConfigEditing.png)

### Screenshot of ssh command logging 
![Image](report3Image\loginWithIeng6.png)

### Screenshot of scp with alias
![Image](report3Image\scpWithAlie.png)

### Describing
This option "Streamlining ssh Configuration" help us to login our account much faster than
before. We first need to create an condig fiel in "C:\Users\[username]}\.ssh". Inside the config file, we can set the aliasto login whatever we want. Then, we are able to login to our account by simply typing "ssh [alias]".

## Setup Github Access from ieng6

### Screenshot of the code diff
![Image](report2Image\code-diff2.png)

### link to the test file for a failure-inducing input
[failure-inducing_input_file2](https://github.com/aaron8004963/markdown-parser/blob/main/myTest-file2.md)

### the Symptom of that input
![Image](report2Image\image_as_link.png)

### Describing
In this case, the symptom I found is that this program incorrectly take the image address as the link address.
The bug is that this program only detect the brackets and simply identify all contents between brackets is the link. Therefore, this program ignores the "!" before bracket.

## Copy whole directories with scp -r
### Screenshot of the code diff
![Image](report2Image\coded-diff3.png)

### link to the test file for a failure-inducing input
[failure-inducing_input_file3](https://github.com/aaron8004963/markdown-parser/blob/main/myTest-file3.md)

### the Sypmtom of that input
![Image](report2Image\indexNegative.png)

### Describing
In this case, the symptom I found is that the program outputs a "IndexOutOfBoundException". I think the bug is caused due to the previous change. This program would still check the chat at previous index of the closebracket when the closebracket is at the index 0. 