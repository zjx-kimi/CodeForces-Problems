## Description

<div><p>You are given an array of $n$ integers $a_1, a_2, \ldots, a_n$.</p><p>In one operation you split the array into two parts: a non-empty prefix and a non-empty suffix. The value of each part is the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#XOR">bitwise XOR</a> of all elements in it. Next, discard the part with the smaller value. If both parts have equal values, you can choose which one to discard. Replace the array with the remaining part.</p><p>The operations are being performed until the length of the array becomes $1$. For each $i$ ($1 \le i \le n$), determine whether it is possible to achieve the state when only the $i$-th element (with respect to the original numbering) remains.</p><p>Formally, you have two numbers $l$ and $r$, initially $l = 1$ and $r = n$. The current state of the array is $[a_l, a_{l+1}, \ldots, a_r]$.</p><p>As long as $l &lt; r$, you apply the following operation: </p><ul> <li> Choose an arbitrary $k$ from the set $\{l, l + 1, \ldots, r - 1\}$. Denote $x = a_l \oplus a_{l + 1} \oplus \ldots \oplus a_k$ and $y = a_{k + 1} \oplus a_{k + 2} \oplus \ldots \oplus a_{r}$, where $\oplus$ denotes the bitwise XOR operation. </li><li> If $x &lt; y$, set $l = k + 1$. </li><li> If $x &gt; y$, set $r = k$. </li><li> If $x = y$, either set $l = k + 1$, or set $r = k$. </li></ul><p>For each $i$ ($1 \le i \le n$), determine whether it is possible to achieve $l = r = i$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10\,000$). The description of the test cases follows.</p><p>The first line of each test case contains one integer $n$ ($1 \le n \le 10\,000$).</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i &lt; 2^{60}$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10\,000$.</p></div><div class="output-specification"><p>For each test case, output a single string of length $n$ where the $i$-th element is equal to <span class="tex-font-style-tt">1</span> if it is possible to achieve $l = r = i$ and is equal to <span class="tex-font-style-tt">0</span> otherwise.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10\,000$). The description of the test cases follows.</p><p>The first line of each test case contains one integer $n$ ($1 \le n \le 10\,000$).</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i &lt; 2^{60}$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10\,000$.</p>

## Output

<p>For each test case, output a single string of length $n$ where the $i$-th element is equal to <span class="tex-font-style-tt">1</span> if it is possible to achieve $l = r = i$ and is equal to <span class="tex-font-style-tt">0</span> otherwise.</p>





```input1|2,3,6,7,10,11
6
6
3 2 1 3 7 4
5
1 1 1 1 1
10
1 2 4 8 4 1 2 3 4 5
5
0 0 0 0 0
5
1 2 3 0 1
1
100500
```




```output1
111111
10101
0001000000
11111
11001
1
```



## Note

<p>In the first test case, it is possible to achieve $l = r = i$ for any $i$ from $1$ to $n$:</p><ul> <li> for $i=1$: $[1; 6] \rightarrow [1; 4] \rightarrow [1; 1]$; </li><li> for $i=2$: $[1; 6] \rightarrow [1; 3] \rightarrow [2; 3] \rightarrow [2; 2]$; </li><li> for $i=3$: $[1; 6] \rightarrow [1; 3] \rightarrow [3; 3]$; </li><li> for $i=4$: $[1; 6] \rightarrow [1; 4] \rightarrow [4; 4]$; </li><li> for $i=5$: $[1; 6] \rightarrow [5; 6] \rightarrow [5; 5]$; </li><li> for $i=6$: $[1; 6] \rightarrow [6; 6]$. </li></ul><p>Let's take a closer look at $i = 2$. Initially $l = 1$, $r = 6$. </p><ol> <li> We can choose $k = 3$ and set $r = k = 3$ since $(3 \oplus 2 \oplus 1) = 0 \ge 0 = (3 \oplus 7 \oplus 4)$; </li><li> Next, we can choose $k = 1$ and set $l = k + 1 = 2$ since $3 \le 3 = (2 \oplus 1)$; </li><li> Finally, we can choose $k = 2$ and set $r = k = 2$ since $2 \ge 1$. </li></ol>
