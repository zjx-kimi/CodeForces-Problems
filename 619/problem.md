## Description

<div><p>Let's define a <span class="tex-font-style-it">permutation</span> of length $n$ as an array $p$ of length $n$, which contains every number from $1$ to $n$ exactly once.</p><p>You are given a permutation $p_1, p_2, \dots, p_n$ and a number $k$. You need to sort this permutation in the ascending order. In order to do it, you can repeat the following operation any number of times (possibly, zero): </p><ul> <li> pick two elements of the permutation $p_i$ and $p_j$ such that $|i - j| = k$, and swap them. </li></ul><p>Unfortunately, some permutations can't be sorted with some fixed numbers $k$. For example, it's impossible to sort $[2, 4, 3, 1]$ with $k = 2$.</p><p>That's why, before starting the sorting, you can make at most one <span class="tex-font-style-it">preliminary exchange</span>: </p><ul> <li> choose any pair $p_i$ and $p_j$ and swap them. </li></ul><p>Your task is to: </p><ol> <li> check whether is it possible to sort the permutation <span class="tex-font-style-bf">without</span> any preliminary exchanges, </li><li> if it's not, check, whether is it possible to sort the permutation using exactly <span class="tex-font-style-bf">one</span> preliminary exchange. </li></ol><p>For example, if $k = 2$ and permutation is $[2, 4, 3, 1]$, then you can make a preliminary exchange of $p_1$ and $p_4$, which will produce permutation $[1, 4, 3, 2]$, which is possible to sort with given $k$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($2 \le n \le 2 \cdot 10^5$; $1 \le k \le n - 1$)&nbsp;— length of the permutation, and a distance between elements that can be swapped.</p><p>The second line of each test case contains $n$ integers $p_1, p_2, \dots, p_n$ ($1 \le p_i \le n$)&nbsp;— elements of the permutation $p$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10 ^ 5$.</p></div><div class="output-specification"><p>For each test case print </p><ul> <li> <span class="tex-font-style-tt">0</span>, if it is possible to sort the permutation without preliminary exchange; </li><li> <span class="tex-font-style-tt">1</span>, if it is possible to sort the permutation with one preliminary exchange, but not possible without preliminary exchange; </li><li> <span class="tex-font-style-tt">-1</span>, if it is not possible to sort the permutation with at most one preliminary exchange. </li></ul></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($2 \le n \le 2 \cdot 10^5$; $1 \le k \le n - 1$)&nbsp;— length of the permutation, and a distance between elements that can be swapped.</p><p>The second line of each test case contains $n$ integers $p_1, p_2, \dots, p_n$ ($1 \le p_i \le n$)&nbsp;— elements of the permutation $p$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10 ^ 5$.</p>

## Output

<p>For each test case print </p><ul> <li> <span class="tex-font-style-tt">0</span>, if it is possible to sort the permutation without preliminary exchange; </li><li> <span class="tex-font-style-tt">1</span>, if it is possible to sort the permutation with one preliminary exchange, but not possible without preliminary exchange; </li><li> <span class="tex-font-style-tt">-1</span>, if it is not possible to sort the permutation with at most one preliminary exchange. </li></ul>





```input1|2,3,6,7,10,11
6
4 1
3 1 2 4
4 2
3 4 1 2
4 2
3 1 4 2
10 3
4 5 9 1 8 6 10 2 3 7
10 3
4 6 9 1 8 5 10 2 3 7
10 3
4 6 9 1 8 5 10 3 2 7
```




```output1
0
0
1
0
1
-1
```



## Note

<p>In the first test case, there is no need in <span class="tex-font-style-it">preliminary exchange</span>, as it is possible to swap $(p_1, p_2)$ and then $(p_2, p_3)$.</p><p>In the second test case, there is no need in <span class="tex-font-style-it">preliminary exchange</span>, as it is possible to swap $(p_1, p_3)$ and then $(p_2, p_4)$.</p><p>In the third test case, you need to apply <span class="tex-font-style-it">preliminary exchange</span> to $(p_2, p_3)$. After that the permutation becomes $[3, 4, 1, 2]$ and can be sorted with $k = 2$.</p>
