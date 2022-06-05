# Lab Report 5
> vim diff and bash scripts

## How you found the tests with different results (Did you use vimdiff on the results of running a bash for loop? Did you search through manually? Did you use some other programmatic idea?)

I use vim diff to find the tests with different result.

---

## link to different tests result file
# Test 1
https://github.com/nidhidhamnani/markdown-parser/edit/main/test-files/193.md

expect output: cse15l:[url];mine:[]

actual output: ['the title']

![Image](report5Image\vimdiff1.png)
* screenshot for actual ouput
![Image](report5Image\real1.png)



# Test 2
https://github.com/nidhidhamnani/markdown-parser/edit/main/test-files/200.md

expect output: cse15l:[baz];
mine:[]

actual output: []

![Image](report5Image\vimdiff2.png)
* screenshot fo actual ouput
![Image](report5Image\real2.png)


# For the implementation that’s not correct (or choose one if both are incorrect), describe the bug
I chose my implementation for test 1.I think the reason is my implementation of MarkdownParse only finds the link between open parentheses and close parentheses; If there doesn't exist an open parentheses, then the program stops. The details below:
![Image](report5Image\myCode.png)

