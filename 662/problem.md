## Description

<div><p>In Berland, there are two types of coins, having denominations of $2$ and $k$ burles.</p><p>Your task is to determine whether it is possible to represent $n$ burles in coins, i. e. whether there exist non-negative integers $x$ and $y$ such that $2 \cdot x + k \cdot y = n$.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains two integers $n$ and $k$ ($1 \le k \le n \le 10^{18}$; $k \ne 2$).</p></div><div class="output-specification"><p>For each test case, print <span class="tex-font-style-tt">YES</span> if it is possible to represent $n$ burles in coins; otherwise, print <span class="tex-font-style-tt">NO</span>. You may print each letter in any case (<span class="tex-font-style-tt">YES</span>, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span> will all be recognized as positive answer, <span class="tex-font-style-tt">NO</span>, <span class="tex-font-style-tt">no</span> and <span class="tex-font-style-tt">nO</span> will all be recognized as negative answer).</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains two integers $n$ and $k$ ($1 \le k \le n \le 10^{18}$; $k \ne 2$).</p>

## Output

<p>For each test case, print <span class="tex-font-style-tt">YES</span> if it is possible to represent $n$ burles in coins; otherwise, print <span class="tex-font-style-tt">NO</span>. You may print each letter in any case (<span class="tex-font-style-tt">YES</span>, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span> will all be recognized as positive answer, <span class="tex-font-style-tt">NO</span>, <span class="tex-font-style-tt">no</span> and <span class="tex-font-style-tt">nO</span> will all be recognized as negative answer).</p>





```input1|2,4
4
5 3
6 1
7 4
8 8
```




```output1
YES
YES
NO
YES
```



## Note

<p>In the first test case, you can take one coin with denomination $2$ and one coin with denomination $k = 3$.</p><p>In the second test case, you can take three coins with denomination $2$. Alternatively, you can take six coins with denomination $k = 1$.</p><p>In the third test case, there is no way to represent $7$ burles.</p><p>In the fourth test case, you can take one coin with denomination $k = 8$.</p>
