## Description

<div><p>You are given a string $s$ of length $n$ consisting of characters "<span class="tex-font-style-tt">+</span>" and "<span class="tex-font-style-tt">-</span>". $s$ represents an array $a$ of length $n$ defined by $a_i=1$ if $s_i=$ "<span class="tex-font-style-tt">+</span>" and $a_i=-1$ if $s_i=$ "<span class="tex-font-style-tt">-</span>".</p><p>You will do the following process to calculate your penalty: </p><ol> <li> Split $a$ into non-empty arrays $b_1,b_2,\ldots,b_k$ such that $b_1+b_2+\ldots+b_k=a^\dagger$, where $+$ denotes array concatenation. </li><li> The <span class="tex-font-style-it">penalty</span> of a single array is the absolute value of its sum multiplied by its length. In other words, for some array $c$ of length $m$, its penalty is calculated as $p(c)=|c_1+c_2+\ldots+c_m| \cdot m$. </li><li> The total penalty that you will receive is $p(b_1)+p(b_2)+\ldots+p(b_k)$. </li></ol><p>If you perform the above process optimally, find the minimum possible penalty you will receive.</p><p>$^\dagger$ Some valid ways to split $a=[3,1,4,1,5]$ into $(b_1,b_2,\ldots,b_k)$ are $([3],[1],[4],[1],[5])$, $([3,1],[4,1,5])$ and $([3,1,4,1,5])$ while some invalid ways to split $a$ are $([3,1],[1,5])$, $([3],[\,],[1,4],[1,5])$ and $([3,4],[5,1,1])$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 5000$)&nbsp;— the length of string $s$.</p><p>The second line of each test case contains string $s$ ($s_i \in \{ \mathtt{+}, \mathtt{-} \}$, $|s| = n$).</p><p>Note that there are <span class="tex-font-style-bf">no</span> constraints on the sum of $n$ over all test cases.</p></div><div class="output-specification"><p>For each test case, output a single integer representing the minimum possible penalty you will receive.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 5000$)&nbsp;— the length of string $s$.</p><p>The second line of each test case contains string $s$ ($s_i \in \{ \mathtt{+}, \mathtt{-} \}$, $|s| = n$).</p><p>Note that there are <span class="tex-font-style-bf">no</span> constraints on the sum of $n$ over all test cases.</p>

## Output

<p>For each test case, output a single integer representing the minimum possible penalty you will receive.</p>





```input1|2,3,6,7,10,11
5
1
+
5
-----
6
+-+-+-
10
--+++++++-
20
+---++++-+++++---++-
```




```output1
1
5
0
4
4
```



## Note

<p>In the first test case, we have $a=[1]$. We can split array $a$ into $([1])$. Then, the sum of penalties of the subarrays is $p([1]) = 1$.</p><p>In the second test case, we have $a=[-1,-1,-1,-1,-1]$. We can split array $a$ into $([-1],[-1],[-1],[-1],[-1])$. Then, the sum of penalties of the subarrays is $p([-1]) + p([-1]) + p([-1]) + p([-1]) + p([-1]) = 1 + 1 + 1 + 1 + 1 = 5$.</p><p>In the third test case, we have $a=[1,-1,1,-1,1,-1]$. We can split array $a$ into $([1,-1,1,-1],[1,-1])$. Then, the sum of penalties of the subarrays is $p([1,-1,1,-1]) + p([1,-1]) = 0 + 0 = 0$.</p>
