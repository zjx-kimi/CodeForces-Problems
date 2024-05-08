## Description

<div><p>In Cyprus, the weather is pretty hot. Thus, Theofanis saw this as an opportunity to create an ice cream company. </p><p>He keeps the ice cream safe from other ice cream producers by locking it inside big storage rooms. However, he forgot the password. Luckily, the lock has a special feature for forgetful people! </p><p>It gives you a table $M$ with $n$ rows and $n$ columns of non-negative integers, and to open the lock, you need to find an array $a$ of $n$ elements such that:</p><ul> <li> $0 \le a_i &lt; 2^{30}$, and </li><li> $M_{i,j} = a_i | a_j$ for all $i \neq j$, where $|$ denotes the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#OR">bitwise OR operation</a>. </li></ul><p>The lock has a bug, and sometimes it gives tables without any solutions. In that case, the ice cream will remain frozen for the rest of eternity.</p><p>Can you find an array to open the lock? </p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^{3}$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^{3}$)&nbsp;— the size of the hidden array.</p><p>The next $n$ lines describe the rows of $M$, line $i$ contains the table values $M_{i,1}, M_{i,2}, \ldots, M_{i,n}$ ($0 \le M_{i,j} &lt; 2^{30}$).</p><p>It is guaranteed that $M_{i,i} = 0$ and $M_{i,j} = M_{j,i}$ for all $1 \le i,j \le n$.</p><p>It is also guaranteed that the sum of $n$ over all test cases does not exceed $10^{3}$.</p></div><div class="output-specification"><p>For each test case, if there is a solution print <span class="tex-font-style-tt">YES</span> and an array that satisfies the property, otherwise print <span class="tex-font-style-tt">NO</span>.</p><p>If there are multiple solutions, print any of them.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^{3}$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^{3}$)&nbsp;— the size of the hidden array.</p><p>The next $n$ lines describe the rows of $M$, line $i$ contains the table values $M_{i,1}, M_{i,2}, \ldots, M_{i,n}$ ($0 \le M_{i,j} &lt; 2^{30}$).</p><p>It is guaranteed that $M_{i,i} = 0$ and $M_{i,j} = M_{j,i}$ for all $1 \le i,j \le n$.</p><p>It is also guaranteed that the sum of $n$ over all test cases does not exceed $10^{3}$.</p>

## Output

<p>For each test case, if there is a solution print <span class="tex-font-style-tt">YES</span> and an array that satisfies the property, otherwise print <span class="tex-font-style-tt">NO</span>.</p><p>If there are multiple solutions, print any of them.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p>





```input1|2,3,9,10,11,12,13,14
4
1
0
4
0 3 3 5
3 0 3 7
3 3 0 7
5 7 7 0
5
0 7 7 5 5
7 0 3 2 6
7 3 0 3 7
5 2 3 0 4
5 6 7 4 0
3
0 0 1
0 0 0
1 0 0
```




```output1
YES
7
YES
1 3 2 5 
YES
5 2 3 0 4
NO
```


