## Description

<div><p>Alice gave Bob two integers $a$ and $b$ ($a &gt; 0$ and $b \ge 0$). Being a curious boy, Bob wrote down an array of <span class="tex-font-style-bf">non-negative</span> integers with $\operatorname{MEX}$ value of all elements equal to $a$ and $\operatorname{XOR}$ value of all elements equal to $b$.</p><p>What is the <span class="tex-font-style-it">shortest</span> possible length of the array Bob wrote?</p><p>Recall that the $\operatorname{MEX}$ (<a href="https://en.wikipedia.org/wiki/Mex_(mathematics)">Minimum EXcluded</a>) of an array is the minimum non-negative integer that does <span class="tex-font-style-bf">not</span> belong to the array and the $\operatorname{XOR}$ of an array is the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#XOR">bitwise XOR</a> of all the elements of the array.</p></div><div class="input-specification"><p>The input consists of multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 5 \cdot 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The only line of each test case contains two integers $a$ and $b$ ($1 \leq a \leq 3 \cdot 10^5$; $0 \leq b \leq 3 \cdot 10^5$)&nbsp;— the $\operatorname{MEX}$ and $\operatorname{XOR}$ of the array, respectively.</p></div><div class="output-specification"><p>For each test case, output one (positive) integer&nbsp;— the length of the shortest array with $\operatorname{MEX}$ $a$ and $\operatorname{XOR}$ $b$. We can show that such an array always exists.</p></div>

## Input

<p>The input consists of multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 5 \cdot 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The only line of each test case contains two integers $a$ and $b$ ($1 \leq a \leq 3 \cdot 10^5$; $0 \leq b \leq 3 \cdot 10^5$)&nbsp;— the $\operatorname{MEX}$ and $\operatorname{XOR}$ of the array, respectively.</p>

## Output

<p>For each test case, output one (positive) integer&nbsp;— the length of the shortest array with $\operatorname{MEX}$ $a$ and $\operatorname{XOR}$ $b$. We can show that such an array always exists.</p>





```input1
5
1 1
2 1
2 0
1 10000
2 10000
```




```output1
3
2
3
2
3
```



## Note

<p>In the first test case, one of the shortest arrays with $\operatorname{MEX}$ $1$ and $\operatorname{XOR}$ $1$ is $[0, 2020, 2021]$.</p><p>In the second test case, one of the shortest arrays with $\operatorname{MEX}$ $2$ and $\operatorname{XOR}$ $1$ is $[0, 1]$.</p><p>It can be shown that these arrays are the shortest arrays possible.</p>
