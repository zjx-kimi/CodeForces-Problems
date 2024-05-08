## Description

<div><p>Yarik's birthday is coming soon, and Mark decided to give him an array $a$ of length $n$.</p><p>Mark knows that Yarik loves bitwise operations very much, and he also has a favorite number $x$, so Mark wants to find the maximum number $k$ such that it is possible to select pairs of numbers [$l_1, r_1$], [$l_2, r_2$], $\ldots$ [$l_k, r_k$], such that: </p><ul> <li> $l_1 = 1$. </li><li> $r_k = n$. </li><li> $l_i \le r_i$ for all $i$ from $1$ to $k$. </li><li> $r_i + 1 = l_{i + 1}$ for all $i$ from $1$ to $k - 1$. </li><li> $(a_{l_1} \oplus a_{l_1 + 1} \oplus \ldots \oplus a_{r_1}) | (a_{l_2} \oplus a_{l_2 + 1} \oplus \ldots \oplus a_{r_2}) | \ldots | (a_{l_k} \oplus a_{l_k + 1} \oplus \ldots \oplus a_{r_k}) \le x$, where $\oplus$ denotes the operation of <a href="https://en.wikipedia.org/wiki/Exclusive_or">bitwise XOR</a>, and $|$ denotes the operation of <a href="https://en.wikipedia.org/wiki/Logical_disjunction">bitwise OR</a>. </li></ul><p>If such $k$ does not exist, then output $-1$.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The following lines contain the descriptions of the test cases.</p><p>The first line of each test case contains two integers $n$ and $x$ ($1 \le n \le 10^5, 0 \le x &lt; 2^{30}$)&nbsp;— the length of the array $a$ and the number $x$ respectively.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i &lt; 2^{30}$)&nbsp;— the array $a$ itself.</p><p>It is guaranteed that the sum of the values of $n$ across all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer on a separate line&nbsp;— the maximum suitable number $k$, and $-1$ if such $k$ does not exist.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The following lines contain the descriptions of the test cases.</p><p>The first line of each test case contains two integers $n$ and $x$ ($1 \le n \le 10^5, 0 \le x &lt; 2^{30}$)&nbsp;— the length of the array $a$ and the number $x$ respectively.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i &lt; 2^{30}$)&nbsp;— the array $a$ itself.</p><p>It is guaranteed that the sum of the values of $n$ across all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output a single integer on a separate line&nbsp;— the maximum suitable number $k$, and $-1$ if such $k$ does not exist.</p>





```input1|2,3,6,7,10,11,14,15
8
3 1
1 2 3
2 2
1 1
2 2
1 3
2 3
0 0
3 2
0 0 1
4 2
1 3 3 7
2 2
2 3
5 0
0 1 2 2 1
```




```output1
2
2
1
2
3
-1
1
2
```



## Note

<p>In the first test case, you can take $k$ equal to $2$ and choose two segments [$1, 1$] and [$2, 3$], $(1) | (2 \oplus 3) = 1$. It can be shown that $2$ is the maximum possible answer.</p><p>In the second test case, the segments [$1, 1$] and [$2, 2$] are suitable, $(1) | (1) = 1$. It is not possible to make more segments.</p><p>In the third test case, it is not possible to choose $2$ segments, as $(1) | (3) = 3 &gt; 2$, so the optimal answer is $1$.</p>
