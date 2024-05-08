## Description

<div><p>You are given a four-digit pin code consisting of digits from $0$ to $9$ that needs to be entered. Initially, the cursor points to the digit $1$. In one second, you can perform exactly one of the following two actions:</p><ul><li> Press the cursor to display the current digit,</li><li> Move the cursor to any adjacent digit.</li></ul><center> <img class="tex-graphics" src="file://qeZldcSq.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>The image above shows the device you are using to enter the pin code. For example, for the digit $5$, the adjacent digits are $4$ and $6$, and for the digit $0$, there is only one adjacent digit, $9$.</p><p>Determine the minimum number of seconds required to enter the given four-digit pin code.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) - the number of the test cases. This is followed by their description.</p><p>The single line of each test case describes the pin code as a string of length $4$, consisting of digits from $0$ to $9$.</p></div><div class="output-specification"><p>For each test case, output the minimum number of seconds required to enter the given pin code.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) - the number of the test cases. This is followed by their description.</p><p>The single line of each test case describes the pin code as a string of length $4$, consisting of digits from $0$ to $9$.</p>

## Output

<p>For each test case, output the minimum number of seconds required to enter the given pin code.</p>





```input1|2,4,6,8,10
10
1111
1236
1010
1920
9273
0000
7492
8543
0294
8361
```




```output1
4
9
31
27
28
13
25
16
33
24
```



## Note

<p>In the first test case, the cursor needs to be pressed $4$ times.</p><p>In the second test case, it can be done in $9$ seconds as follows:</p><ul><li> Press the cursor.</li><li> Move the cursor to the digit $2$.</li><li> Press the cursor.</li><li> Move the cursor to the digit $3$.</li><li> Press the cursor.</li><li> Move the cursor to the digit $4$.</li><li> Move the cursor to the digit $5$.</li><li> Move the cursor to the digit $6$.</li><li> Press the cursor.</li></ul>
