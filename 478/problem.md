## Description

<div><p>While tracking Diavolo's origins, Giorno receives a secret code from Polnareff. The code can be represented as an infinite sequence of positive integers: $a_1, a_2, \dots $. Giorno immediately sees the pattern behind the code. The first $n$ numbers $a_1, a_2, \dots, a_n$ are <span class="tex-font-style-bf">given</span>. For $i &gt; n$ the value of $a_i$ is $(a_{i-n}\ |\ a_{i-n+1})$, where $|$ denotes the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#OR">bitwise OR operator</a>.</p><p>Pieces of information about Diavolo are hidden in $q$ questions. Each question has a positive integer $v$ associated with it and its answer is the smallest index $i$ such that $a_i &gt; v$. If no such $i$ exists, the answer is $-1$. Help Giorno in answering the questions!</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10\,000$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $q$ ($2 \leq n \leq 2 \cdot 10^5$ , $1 \leq q \leq 2 \cdot 10^5$).</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($0 \leq a_i \leq 10^9$)&nbsp;— the parts of the code which define the pattern.</p><p>The $i$-th line of the next $q$ lines contain a single integer $v_i$ ($0 \leq v_i \leq 10^9$)&nbsp;— the question Giorno asks you.</p><p>The sum of $n$ and $q$ over all test cases does not exceed $2 \cdot 10^5$. </p></div><div class="output-specification"><p>Print $q$ numbers. The $i$-th number is the answer to the $i$-th question asked by Giorno.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10\,000$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $q$ ($2 \leq n \leq 2 \cdot 10^5$ , $1 \leq q \leq 2 \cdot 10^5$).</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($0 \leq a_i \leq 10^9$)&nbsp;— the parts of the code which define the pattern.</p><p>The $i$-th line of the next $q$ lines contain a single integer $v_i$ ($0 \leq v_i \leq 10^9$)&nbsp;— the question Giorno asks you.</p><p>The sum of $n$ and $q$ over all test cases does not exceed $2 \cdot 10^5$. </p>

## Output

<p>Print $q$ numbers. The $i$-th number is the answer to the $i$-th question asked by Giorno.</p>





```input1|2,3,4,5,6,14,15,16,17,18,19,20
3
2 3
2 1
1
2
3
4 5
0 2 1 3
0
1
2
3
4
5 5
1 2 3 4 5
7
2
6
0
4
```




```output1
1
3
-1
2
2
4
-1
-1
-1
3
8
1
5
```



## Note

<p>In the first test case, $a = [2,1,3,3,\ldots]$. </p><ul> <li> For the first question, $a_1=2$ is the element with the smallest index greater than $1$. </li><li> For the second question, $a_3=3$ is the element with the smallest index greater than $2$. </li><li> For the third question, there is no index $i$ such that $a_i &gt; 3$. </li></ul>
