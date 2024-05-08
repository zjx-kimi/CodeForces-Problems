## Description

<div><p>An array $a$ of length $m$ is considered good if there exists an integer array $b$ of length $m$ such that the following conditions hold: </p><ol>  <li> $\sum\limits_{i=1}^{m} a_i = \sum\limits_{i=1}^{m} b_i$;  </li><li> $a_i \neq b_i$ for every index $i$ from $1$ to $m$;  </li><li> $b_i &gt; 0$ for every index $i$ from $1$ to $m$. </li></ol><p>You are given an array $c$ of length $n$. Each element of this array is greater than $0$.</p><p>You have to answer $q$ queries. During the $i$-th query, you have to determine whether the subarray $c_{l_{i}}, c_{l_{i}+1}, \dots, c_{r_{i}}$ is good.</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>The first line of each test case contains two integers $n$ and $q$ ($1 \le n, q \le 3 \cdot 10^5$) — the length of the array $c$ and the number of queries.</p><p>The second line of each test case contains $n$ integers $c_1, c_2, \dots, c_n$ ($1 \le c_i \le 10^9$).</p><p>Then $q$ lines follow. The $i$-th of them contains two integers $l_i$ and $r_i$ ($1 \le l_i \le r_i \le n$) — the borders of the $i$-th subarray.</p><p>Additional constraints on the input: the sum of $n$ over all test cases does not exceed $3 \cdot 10^5$; the sum of $q$ over all test cases does not exceed $3 \cdot 10^5$.</p></div><div class="output-specification"><p>For each query, print <span class="tex-font-style-tt">YES</span> if the subarray is good. Otherwise, print <span class="tex-font-style-tt">NO</span>.</p><p>You can output each letter of the answer in any case (upper or lower). For example, the strings <span class="tex-font-style-tt">yEs</span>, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span>, and <span class="tex-font-style-tt">YES</span> will all be recognized as positive responses.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>The first line of each test case contains two integers $n$ and $q$ ($1 \le n, q \le 3 \cdot 10^5$) — the length of the array $c$ and the number of queries.</p><p>The second line of each test case contains $n$ integers $c_1, c_2, \dots, c_n$ ($1 \le c_i \le 10^9$).</p><p>Then $q$ lines follow. The $i$-th of them contains two integers $l_i$ and $r_i$ ($1 \le l_i \le r_i \le n$) — the borders of the $i$-th subarray.</p><p>Additional constraints on the input: the sum of $n$ over all test cases does not exceed $3 \cdot 10^5$; the sum of $q$ over all test cases does not exceed $3 \cdot 10^5$.</p>

## Output

<p>For each query, print <span class="tex-font-style-tt">YES</span> if the subarray is good. Otherwise, print <span class="tex-font-style-tt">NO</span>.</p><p>You can output each letter of the answer in any case (upper or lower). For example, the strings <span class="tex-font-style-tt">yEs</span>, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span>, and <span class="tex-font-style-tt">YES</span> will all be recognized as positive responses.</p>





```input1|2,3,4,5,6,7
1
5 4
1 2 1 4 5
1 5
4 4
3 4
1 3
```




```output1
YES
NO
YES
NO
```


