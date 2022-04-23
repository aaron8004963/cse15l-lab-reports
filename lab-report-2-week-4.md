# Lab Report 2
> reviewing lab 3 group work

## First change

### Screenshot of the code diff
![Image](report2Image\code-diff1.png)

### link to the test file for a failure-inducing input
[failure-inducing_input_file1](https://github.com/aaron8004963/markdown-parser/blob/main/myTest-file1.md)

### the Symptom of that input
![Image](report2Image\out_of_memory.png)

### Describing
In this case, the symptom I found is that the terminal shows "OutofMemoryError" instead of showing corret link output. I think the bug which causes this error is when the program cannot find next openBracket, the currenindex
will never be updated.This failure-inducing input contains a "blank" after the closeBracket,therefore the currenindex will fowever smaller than the size of this file contents. Thus it will cause a inifinite loop and results a OutofMemoryError.

## Second change

### Screenshot of the code diff
![Image](report2Image\code-diff2.png)

### link to the test file for a failure-inducing input
[failure-inducing_input_file2](https://github.com/aaron8004963/markdown-parser/blob/main/myTest-file2.md)

### the Symptom of that input
![Image](report2Image\image_as_link.png)

### Describing
In this case, the symptom I found is that this program incorrectly take the image address as the link address.
The bug is that this program only detect the brackets and simply identify all contents between brackets is the link. Therefore, this program ignores the "!" before bracket.

## Third change
### Screenshot of the code diff
![Image](report2Image\coded-diff3.png)

### link to the test file for a failure-inducing input
[failure-inducing_input_file3](https://github.com/aaron8004963/markdown-parser/blob/main/myTest-file3.md)

### the Sypmtom of that input
![Image](report2Image\indexNegative.png)

### Describing
In this case, the symptom I found is that the program outputs a "IndexOutOfBoundException". I think the bug is caused due to the previous change. This program would still check the chat at previous index of the closebracket when the closebracket is at the index 0. 