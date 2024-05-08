## Description

<div><div class="epigraph"><div class="epigraph-text"><span class="tex-font-style-it"><a href="https://soundcloud.com/shiki-8/pure-rubyversoundcloud">Shiki - Pure Ruby</a></span></div><div class="epigraph-source">⠀</div></div><p>You have $n$ intervals $[l_1, r_1], [l_2, r_2], \dots, [l_n, r_n]$, such that $l_i &lt; r_i$ for each $i$, and all the endpoints of the intervals are distinct.</p><p>The $i$-th interval has weight $c_i$ per unit length. Therefore, the <span class="tex-font-style-it">weight</span> of the $i$-th interval is $c_i \cdot (r_i - l_i)$.</p><p>You don't like large weights, so you want to make the sum of weights of the intervals as small as possible. It turns out you can perform all the following three operations:</p><ul> <li> rearrange the elements in the array $l$ in any order; </li><li> rearrange the elements in the array $r$ in any order; </li><li> rearrange the elements in the array $c$ in any order. </li></ul><p>However, after performing all of the operations, the intervals must still be valid (i.e., for each $i$, $l_i &lt; r_i$ must hold).</p><p>What's the minimum possible sum of weights of the intervals after performing the operations?</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$)&nbsp;— the number of intervals.</p><p>The second line of each test case contains $n$ integers $l_1, l_2, \ldots, l_n$ ($1 \le l_i \le 2 \cdot 10^5$)&nbsp;— the left endpoints of the initial intervals.</p><p>The third line of each test case contains $n$ integers $r_1, r_2, \ldots, r_n$ ($l_i &lt; r_i \le 2 \cdot 10^5$)&nbsp;— the right endpoints of the initial intervals.</p><p>It is guaranteed that $\{l_1, l_2, \dots, l_n, r_1, r_2, \dots, r_n\}$ are all distinct.</p><p>The fourth line of each test case contains $n$ integers $c_1, c_2, \ldots, c_n$ ($1 \le c_i \le 10^7$)&nbsp;— the initial weights of the intervals per unit length.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer: the minimum possible sum of weights of the intervals after your operations.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$)&nbsp;— the number of intervals.</p><p>The second line of each test case contains $n$ integers $l_1, l_2, \ldots, l_n$ ($1 \le l_i \le 2 \cdot 10^5$)&nbsp;— the left endpoints of the initial intervals.</p><p>The third line of each test case contains $n$ integers $r_1, r_2, \ldots, r_n$ ($l_i &lt; r_i \le 2 \cdot 10^5$)&nbsp;— the right endpoints of the initial intervals.</p><p>It is guaranteed that $\{l_1, l_2, \dots, l_n, r_1, r_2, \dots, r_n\}$ are all distinct.</p><p>The fourth line of each test case contains $n$ integers $c_1, c_2, \ldots, c_n$ ($1 \le c_i \le 10^7$)&nbsp;— the initial weights of the intervals per unit length.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output a single integer: the minimum possible sum of weights of the intervals after your operations.</p>





```input1|2,3,4,5
2
2
8 3
12 23
100 100
4
20 1 2 5
30 4 3 10
2 3 2 3
```




```output1
2400
42
```



## Note

<p>In the first test case, you can make </p><ul> <li> $l = [8, 3]$; </li><li> $r = [23, 12]$; </li><li> $c = [100, 100]$. </li></ul><p>In that case, there are two intervals: </p><ul> <li> interval $[8, 23]$ with weight $100$ per unit length, and $100 \cdot (23-8) = 1500$ in total; </li><li> interval $[3, 12]$ with weight $100$ per unit length, and $100 \cdot (12-3) = 900$ in total. </li></ul><p>The sum of the weights is $2400$. It can be shown that there is no configuration of final intervals whose sum of weights is less than $2400$.</p><p>In the second test case, you can make </p><ul> <li> $l = [1, 2, 5, 20]$; </li><li> $r = [3, 4, 10, 30]$; </li><li> $c = [3, 3, 2, 2]$. </li></ul><p>In that case, there are four intervals: </p><ul> <li> interval $[1, 3]$ with weight $3$ per unit length, and $3 \cdot (3-1) = 6$ in total; </li><li> interval $[2, 4]$ with weight $3$ per unit length, and $3 \cdot (4-2) = 6$ in total; </li><li> interval $[5, 10]$ with weight $2$ per unit length, and $2 \cdot (10-5) = 10$ in total; </li><li> interval $[20, 30]$ with weight $2$ per unit length, and $2 \cdot (30-20) = 20$ in total. </li></ul><p>The sum of the weights is $42$. It can be shown that there is no configuration of final intervals whose sum of weights is less than $42$.</p>
