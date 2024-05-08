## Description

<div><p>Given an array $a_1, a_2, \ldots, a_n$, determine whether it is possible to <span class="tex-font-style-bf">rearrange its elements</span> into $b_1, b_2, \ldots, b_n$, such that $b_1 \bmod b_2 \bmod \ldots \bmod b_n \neq 0$.</p><p>Here $x \bmod y$ denotes the remainder from dividing $x$ by $y$. Also, the modulo operations are calculated from left to right. That is, $x \bmod y \bmod z = (x \bmod y) \bmod z$. For example, $2024 \bmod 1000 \bmod 8 = (2024 \bmod 1000) \bmod 8 = 24 \bmod 8 = 0$.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 10^5$).</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$).</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if it is possible, "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 10^5$).</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$).</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if it is possible, "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p>





```input1|2,3,6,7,10,11,14,15
8
6
1 2 3 4 5 6
5
3 3 3 3 3
3
2 2 3
5
1 1 2 3 7
3
1 2 2
3
1 1 2
6
5 2 10 10 10 2
4
3 6 9 3
```




```output1
YES
NO
YES
NO
YES
NO
YES
NO
```



## Note

<p>In the first test case, rearranging the array into $b = [1, 2, 3, 4, 5, 6]$ (doing nothing) would result in $1 \bmod 2 \bmod 3 \bmod 4 \bmod 5 \bmod 6 = 1$. Hence it is possible to achieve the goal.</p><p>In the second test case, the array $b$ must be equal to $[3, 3, 3, 3, 3]$, which would result in $3 \bmod 3 \bmod 3 \bmod 3 \bmod 3 = 0$. Hence it is impossible to achieve the goal.</p><p>In the third test case, rearranging the array into $b = [3, 2, 2]$ would result in $3 \bmod 2 \bmod 2 = 1$. Hence it is possible to achieve the goal.</p>
