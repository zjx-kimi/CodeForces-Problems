## Description

<div><p>You are given an array $[p_1, p_2, \dots, p_n]$, where all elements are distinct.</p><p>You can perform several (possibly zero) operations with it. In one operation, you can choose a <span class="tex-font-style-bf">contiguous subsegment</span> of $p$ and remove <span class="tex-font-style-bf">all</span> elements from that subsegment, <span class="tex-font-style-bf">except for</span> the minimum element on that subsegment. For example, if $p = [3, 1, 4, 7, 5, 2, 6]$ and you choose the subsegment from the $3$-rd element to the $6$-th element, the resulting array is $[3, 1, 2, 6]$.</p><p>An array $a$ is called <span class="tex-font-style-it">reachable</span> if it can be obtained from $p$ using several (maybe zero) aforementioned operations. Calculate the number of <span class="tex-font-style-it">reachable</span> arrays, and print it modulo $998244353$.</p></div><div class="input-specification"><p>The first line of the input contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of two lines. The first line contains one integer $n$ ($1 \le n \le 3 \cdot 10^5$). The second line contains $n$ <span class="tex-font-style-bf">distinct</span> integers $p_1, p_2, \dots, p_n$ ($1 \le p_i \le 10^9$).</p><p>Additional constraint on the input: the sum of $n$ over all test cases does not exceed $3 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print one integer — the number of <span class="tex-font-style-it">reachable</span> arrays, taken modulo $998244353$.</p></div>

## Input

<p>The first line of the input contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of two lines. The first line contains one integer $n$ ($1 \le n \le 3 \cdot 10^5$). The second line contains $n$ <span class="tex-font-style-bf">distinct</span> integers $p_1, p_2, \dots, p_n$ ($1 \le p_i \le 10^9$).</p><p>Additional constraint on the input: the sum of $n$ over all test cases does not exceed $3 \cdot 10^5$.</p>

## Output

<p>For each test case, print one integer — the number of <span class="tex-font-style-it">reachable</span> arrays, taken modulo $998244353$.</p>





```input1|2,3,6,7
3
2
2 1
4
2 4 1 3
5
10 2 6 3 4
```




```output1
2
6
12
```


