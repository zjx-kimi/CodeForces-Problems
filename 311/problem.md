## Description

<div><p>You are given a string $s$ of length $n$, containing lowercase Latin letters. </p><p>Next you will be given a positive integer $k$ and two arrays, $l$ and $r$ of length $k$.</p><p>It is guaranteed that the following conditions hold for these 2 arrays: </p><ul> <li> $l_1 = 1$; </li><li> $r_k = n$; </li><li> $l_i \le r_i$, for each positive integer $i$ such that $1 \le i \le k$; </li><li> $l_i = r_{i-1}+1$, for each positive integer $i$ such that $2 \le i \le k$; </li></ul><p>Now you will be given a positive integer $q$ which represents the number of modifications you need to do on $s$.</p><p>Each modification is defined with one positive integer $x$: </p><ul> <li> Find an index $i$ such that $l_i \le x \le r_i$ (notice that such $i$ is unique). </li><li> Let $a=\min(x, r_i+l_i-x)$ and let $b=\max(x, r_i+l_i-x)$. </li><li> Reverse the substring of $s$ from index $a$ to index $b$. </li></ul><p>Reversing the substring $[a, b]$ of a string $s$ means to make $s$ equal to $s_1, s_2, \dots, s_{a-1},\ s_b, s_{b-1}, \dots, s_{a+1}, s_a,\ s_{b+1}, s_{b+2}, \dots, s_{n-1}, s_n$.</p><p>Print $s$ after the last modification is finished.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le k \le n \le 2\cdot 10^5$)&nbsp;— the length of the string $s$, and the length of arrays $l$ and $r$.</p><p>The second line of each test case contains the string $s$ ($ |s| = n$) containing lowercase Latin letters&nbsp;— the initial string.</p><p>The third line of each test case contains $k$ positive integers $l_1, l_2, \dots, l_k$ ($1 \le l_i \le n$)&nbsp;— the array $l$.</p><p>The fourth line of each test case contains $k$ positive integers $r_1, r_2, \dots, r_k$ ($1 \le r_i \le n$)&nbsp;— the array $r$.</p><p>The fifth line of each test case contains a positive integer $q$ ($1 \le q \le 2 \cdot 10^5 $)&nbsp;— the number of modifications you need to do to $s$.</p><p>The sixth line of each test case contains $q$ positive integers $x_1, x_2, \dots, x_q$ ($1\le x_i \le n$)&nbsp;— the description of the modifications.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot10^5$. </p><p>It is guaranteed that the sum of $q$ over all test cases does not exceed $2\cdot10^5$.</p><p>It is guaranteed that the conditions in the statement hold for the arrays $l$ and $r$.</p></div><div class="output-specification"><p>For each test case, in a new line, output the string $s$ after the last modification is done.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le k \le n \le 2\cdot 10^5$)&nbsp;— the length of the string $s$, and the length of arrays $l$ and $r$.</p><p>The second line of each test case contains the string $s$ ($ |s| = n$) containing lowercase Latin letters&nbsp;— the initial string.</p><p>The third line of each test case contains $k$ positive integers $l_1, l_2, \dots, l_k$ ($1 \le l_i \le n$)&nbsp;— the array $l$.</p><p>The fourth line of each test case contains $k$ positive integers $r_1, r_2, \dots, r_k$ ($1 \le r_i \le n$)&nbsp;— the array $r$.</p><p>The fifth line of each test case contains a positive integer $q$ ($1 \le q \le 2 \cdot 10^5 $)&nbsp;— the number of modifications you need to do to $s$.</p><p>The sixth line of each test case contains $q$ positive integers $x_1, x_2, \dots, x_q$ ($1\le x_i \le n$)&nbsp;— the description of the modifications.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot10^5$. </p><p>It is guaranteed that the sum of $q$ over all test cases does not exceed $2\cdot10^5$.</p><p>It is guaranteed that the conditions in the statement hold for the arrays $l$ and $r$.</p>

## Output

<p>For each test case, in a new line, output the string $s$ after the last modification is done.</p>





```input1|2,3,4,5,6,7,14,15,16,17,18,19,26,27,28,29,30,31
5
4 2
abcd
1 3
2 4
2
1 3
5 3
abcde
1 2 3
1 2 5
3
1 2 3
3 1
gaf
1
3
2
2 2
10 1
aghcdegdij
1
10
5
1 2 3 4 2
1 1
a
1
1
1
1
```




```output1
badc
abedc
gaf
jihgedcdga
a
```



## Note

<p>In the first test case:</p><p>The initial string is "<span class="tex-font-style-tt">abcd</span>". In the <span class="tex-font-style-bf">first modification</span>, we have $x=1$. Since $l_1=1\leq x \leq r_1=2$, we find the index $i = 1$. We reverse the substring from index $x=1$ to $l_1+r_1-x=1+2-1=2$. After this modification, our string is "<span class="tex-font-style-tt">bacd</span>". </p><p>In the <span class="tex-font-style-bf">second modification</span> (and the last modification), we have $x=3$. Since $l_2=3\leq x \leq r_2=4$, we find the index $i = 2$. We reverse the substring from index $x=3$ to $l_2+r_2-x=3+4-3=4$. After this modification, our string is "<span class="tex-font-style-tt">badc</span>".</p><p>In the second test case:</p><p>The initial string is "<span class="tex-font-style-tt">abcde</span>". In the <span class="tex-font-style-bf">first modification</span>, we have $x=1$. Since $l_1=1\leq x \leq r_1=1$, we find the index $i = 1$. We reverse the substring from index $x=1$ to $l_1+r_1-x=1+1-1=1$. After this modification, our string hasn't changed ("<span class="tex-font-style-tt">abcde</span>"). </p><p>In the <span class="tex-font-style-bf">second modification</span>, we have $x=2$. Since $l_2=2\leq x \leq r_2=2$, we find the index $i = 2$. We reverse the substring from index $x=2$ to $l_2+r_2-x=2+2-2=2$. After this modification, our string hasn't changed ("<span class="tex-font-style-tt">abcde</span>"). </p><p>In the <span class="tex-font-style-bf">third modification</span> (and the last modification), we have $x=3$. Since $l_3=3\leq x \leq r_3=5$, we find the index $i = 3$. We reverse the substring from index $x=3$ to $l_3+r_3-x=3+5-3=5$. After this modification, our string is "<span class="tex-font-style-tt">abedc</span>".</p>
