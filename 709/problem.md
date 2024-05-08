## Description

<div><p><span class="tex-font-style-bf">This is the easy version of the problem. The only difference between the two versions is the constraint on $m$. You can make hacks only if both versions of the problem are solved.</span></p><p>You are given an array $a$ of length $n$ and two integers $m$ and $k$. Each element in $a$ satisfies $1\le a_i \le m$.</p><p>In one operation, you choose two indices $i$ and $j$ such that $1 \le i &lt; j \le |a|$, then append $\gcd(a_i,a_j)$ to the back of the array and delete $a_i$ and $a_j$ from the array. Note that the length of the array decreases by one after this operation.</p><p>Find the maximum possible sum of the array after performing <span class="tex-font-style-bf">exactly</span> $k$ operations.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1\le t\le 10^5$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains three integers $n$, $m$ and $k$ ($2 \le n \le 10^6$; $1\le m \le 10^6$; $1 \le k \le n-1$).</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($1 \le a_i \le m$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^6$ and the sum of $m$ over all test cases does not exceed $10^6$.</p></div><div class="output-specification"><p>For each test case, output the maximum possible sum of the array after performing $k$ operations optimally.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1\le t\le 10^5$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains three integers $n$, $m$ and $k$ ($2 \le n \le 10^6$; $1\le m \le 10^6$; $1 \le k \le n-1$).</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($1 \le a_i \le m$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^6$ and the sum of $m$ over all test cases does not exceed $10^6$.</p>

## Output

<p>For each test case, output the maximum possible sum of the array after performing $k$ operations optimally.</p>





```input1|2,3,6,7
3
3 8 1
4 7 8
5 114 2
7 2 4 1 6
3 514 2
2 3 3
```




```output1
11
14
1
```



## Note

<p>In the first test case, the best way is to choose $i=1$, $j=3$ in the first operation. The final sequence is $[7,4]$.</p>
