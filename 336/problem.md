## Description

<div><p>Luca is in front of a row of $n$ trees. The $i$-th tree has $a_i$ fruit and height $h_i$.</p><p>He wants to choose a contiguous subarray of the array $[h_l, h_{l+1}, \dots, h_r]$ such that for each $i$ ($l \leq i &lt; r$), <span class="tex-font-style-bf">$h_i$ is divisible$^{\dagger}$ by $h_{i+1}$</span>. He will collect all the fruit from each of the trees in the subarray (that is, he will collect $a_l + a_{l+1} + \dots + a_r$ fruits). However, if he collects more than $k$ fruits in total, he will get caught. </p><p>What is the maximum length of a subarray Luca can choose so he doesn't get caught?</p><p>$^{\dagger}$ $x$ is <span class="tex-font-style-it">divisible</span> by $y$ if the ratio $\frac{x}{y}$ is an integer.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases.</p><p>The first of each test case line contains two space-separated integers $n$ and $k$ ($1 \leq n \leq 2 \cdot 10^5$; $1 \leq k \leq 10^9$)&nbsp;— the number of trees and the maximum amount of fruits Luca can collect without getting caught.</p><p>The second line of each test case contains $n$ space-separated integers $a_i$ ($1 \leq a_i \leq 10^4$)&nbsp;— the number of fruits in the $i$-th tree.</p><p>The third line of each test case contains $n$ space-separated integers $h_i$ ($1 \leq h_i \leq 10^9$)&nbsp;— the height of the $i$-th tree.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$. </p></div><div class="output-specification"><p>For each test case output a single integer, the length of the maximum length contiguous subarray satisfying the conditions, or $0$ if there is no such subarray.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases.</p><p>The first of each test case line contains two space-separated integers $n$ and $k$ ($1 \leq n \leq 2 \cdot 10^5$; $1 \leq k \leq 10^9$)&nbsp;— the number of trees and the maximum amount of fruits Luca can collect without getting caught.</p><p>The second line of each test case contains $n$ space-separated integers $a_i$ ($1 \leq a_i \leq 10^4$)&nbsp;— the number of fruits in the $i$-th tree.</p><p>The third line of each test case contains $n$ space-separated integers $h_i$ ($1 \leq h_i \leq 10^9$)&nbsp;— the height of the $i$-th tree.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$. </p>

## Output

<p>For each test case output a single integer, the length of the maximum length contiguous subarray satisfying the conditions, or $0$ if there is no such subarray.</p>





```input1|2,3,4,8,9,10,14,15,16
5
5 12
3 2 4 1 8
4 4 2 4 1
4 8
5 4 1 2
6 2 3 1
3 12
7 9 10
2 2 4
1 10
11
1
7 10
2 6 3 1 5 10 6
72 24 24 12 4 4 2
```




```output1
3
2
1
0
3
```



## Note

<p>In the first test case, Luca can select the subarray with $l=1$ and $r=3$.</p><p>In the second test case, Luca can select the subarray with $l=3$ and $r=4$.</p><p>In the third test case, Luca can select the subarray with $l=2$ and $r=2$.</p>
