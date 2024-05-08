## Description

<div><p>As soon as everyone in the camp fell asleep, Kirill sneaked out of the tent and went to the Wise Oak to gather mushrooms.</p><p>It is known that there are $n$ mushrooms growing under the Oak, each of which has magic power $v_i$. Kirill really wants to make a magical elixir of maximum strength from the mushrooms.</p><p>The strength of the elixir is equal to the product of the <span class="tex-font-style-bf">number</span> of mushrooms in it and the <span class="tex-font-style-bf">minimum</span> magic power among these mushrooms. To prepare the elixir, Kirill will sequentially pick one mushroom growing under the Oak. Kirill can gather mushrooms in any order.</p><p>However, it's not that simple. The Wise Oak informed Kirill of a permutation of numbers $p$ from $1$ to $n$. If Kirill picks only $k$ mushrooms, then the magic power of all mushrooms with indices $p_1, p_2, \dots, p_{k - 1}$ will become $0$. Kirill will not use mushrooms with zero magic power to prepare the elixir.</p><p>Your task is to help Kirill gather mushrooms in such a way that he can brew the elixir of maximum possible strength. However, Kirill is a little scared to stay near the oak for too long, so out of all the suitable options for gathering mushrooms, he asks you to find the one with the minimum number of mushrooms.</p><p>A permutation of length $n$ is an array consisting of $n$ different integers from $1$ to $n$ in any order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation ($2$ appears in the array twice) and $[1,3,4]$ is also not a permutation ($n=3$, but $4$ appears in the array).</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 200\,000$)&nbsp;— the number of mushrooms.</p><p>The second line contains an array $v$ of size $n$ ($1\le v_i \le 10^9$)&nbsp;— the magic powers of the mushrooms.</p><p>The third line contains a permutation $p$ of numbers from $1$ to $n$.</p><p>It is guaranteed that the sum of the values of $n$ over all test cases does not exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output two integers separated by a space&nbsp;— the maximum strength of the elixir that can be brewed and the minimum number of mushrooms that Kirill needs to use for this.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 200\,000$)&nbsp;— the number of mushrooms.</p><p>The second line contains an array $v$ of size $n$ ($1\le v_i \le 10^9$)&nbsp;— the magic powers of the mushrooms.</p><p>The third line contains a permutation $p$ of numbers from $1$ to $n$.</p><p>It is guaranteed that the sum of the values of $n$ over all test cases does not exceed $2\cdot 10^5$.</p>

## Output

<p>For each test case, output two integers separated by a space&nbsp;— the maximum strength of the elixir that can be brewed and the minimum number of mushrooms that Kirill needs to use for this.</p>





```input1|2,3,4,8,9,10,14,15,16
6
3
9 8 14
3 2 1
5
1 2 3 4 5
1 2 3 4 5
6
1 2 3 4 5 6
6 5 4 3 2 1
5
1 4 6 10 10
2 1 4 5 3
4
2 2 5 5
4 2 3 1
5
1 2 9 10 10
1 4 2 3 5
```




```output1
16 2
9 3
8 2
20 2
5 1
20 2
```



## Note

<p>In the first example, you need to take the mushrooms with indices $1$ and $2$, so the strength of the elixir is equal to $2 \cdot \min(a_1, a_2) = 2 \cdot \min(9, 8) = 2 \cdot 8 = 16$. Note that the magic power of the mushroom with index $3$ after picking two mushrooms will become $0$.</p>
