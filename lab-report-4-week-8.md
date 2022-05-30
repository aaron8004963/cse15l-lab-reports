# Lab Report 4
> markdownParse Tests

## links
my repository: https://github.com/aaron8004963/markdown-parser
reviewd repository: https://github.com/alixintong/markdown-parser

## Tests for My implementation:

## First test from snippet_1
1. It should produce [`google.com, google.com, ucsd.edu]
2. The code I turn it to a test:
![Image](report4Image\Test1.png)
3. result for my implementation: Passed

## Second test to snippet_2
1. It should produce [a.com, a.com(()), example.com]
2. The code I turn it to a test:
![Image](report4Image\Test2.png)
3. result for my implementation: failures
![Image](report4Image\mresult1.png)

## Third test to snippet_3
1. It should produce [https://www.twitter.com, https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule, https://cse.ucsd.edu/]
2. The code I turn it to a test:
![Image](report4Image\Test3.png)
3. result for my implementation: failures
![Image](report4Image\mresult2.png)

## Tests for Reviewed implementation:

## First test from snippet_1
1. It should produce [`google.com, google.com, ucsd.edu]
2. The code I turn it to a test:
![Image](report4Image\rTest1.png)
3. result for their implementation: failures
![Image](report4Image\rresult1.png)

## Second test to snippet_2
1. It should produce [a.com, a.com(()), example.com]
2. The code I turn it to a test:
![Image](report4Image\rTest2.png)
3. result for their implementation: failures
![Image](report4Image\rresult2.png)

## Third test to snippet_3
1. It should produce [https://www.twitter.com, https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule, https://cse.ucsd.edu/]
2. The code I turn it to a test:
![Image](report4Image\rTest3.png)
3. result for their implementation: failures
![Image](report4Image\rresult3.png)

## Answering questios:
1. Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change.

There is a small code change that will make my program work for snippet 1. The backtick will not affect the original functionality to find the correct link unless it is occured before the openBracket. Therefore, I can simply add a if statement to check is the closeBracket has a backtick one before its index.

2. Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be a more involved change.

I don't think there is a small code change that will make my program work for snippet 2. In order to pair up all nest parentheses, brackets, and escaped brackets, we need some kind of stack method to count the number of openParens and closeParens. Thus we can determine which pair are the outmost parentheses, then we can get the correct link.

3. Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would be a more involved change

I think there is a small code change that will make my program work for snippet 1. All I need to do is to count the number of blanks occurred between the open paren and the first character, and between the last character of link and the close pare. Thus, I can reading the substring from (openParen + numBlanks) to (closeParen - numBlanks) to get the correct link
