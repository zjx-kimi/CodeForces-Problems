## Description

<div><div class="epigraph"><div class="epigraph-text"><span class="tex-font-style-it">Enjoy erasing Tenzing, identified as Accepted!</span></div></div><p>Tenzing has $n$ balls arranged in a line. The color of the $i$-th ball from the left is $a_i$.</p><p>Tenzing can do the following operation any number of times:</p><ul> <li> select $i$ and $j$ such that $1\leq i &lt; j \leq |a|$ and $a_i=a_j$, </li><li> remove $a_i,a_{i+1},\ldots,a_j$ from the array (and decrease the indices of all elements to the right of $a_j$ by $j-i+1$). </li></ul><p>Tenzing wants to know the maximum number of balls he can remove.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1\leq t\leq 10^3$) — the number of test cases. The description of test cases follows.</p><p>The first line contains a single integer $n$ ($1\leq n\leq 2\cdot 10^5$)&nbsp;— the number of balls.</p><p>The second line contains $n$ integers $a_1,a_2,\ldots,a_n$ ($1\leq a_i \leq n$)&nbsp;— the color of the balls.</p><p>It is guaranteed that sum of $n$ of all test cases will not exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output the maximum number of balls Tenzing can remove.</p></div>

## Input

<p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1\leq t\leq 10^3$) — the number of test cases. The description of test cases follows.</p><p>The first line contains a single integer $n$ ($1\leq n\leq 2\cdot 10^5$)&nbsp;— the number of balls.</p><p>The second line contains $n$ integers $a_1,a_2,\ldots,a_n$ ($1\leq a_i \leq n$)&nbsp;— the color of the balls.</p><p>It is guaranteed that sum of $n$ of all test cases will not exceed $2\cdot 10^5$.</p>

## Output

<p>For each test case, output the maximum number of balls Tenzing can remove.</p>





```input1|2,3
2
5
1 2 2 3 3
4
1 2 1 2
```




```output1
4
3
```



## Note

<p>In the first example, Tenzing will choose $i=2$ and $j=3$ in the first operation so that $a=[1,3,3]$. Then Tenzing will choose $i=2$ and $j=3$ again in the second operation so that $a=[1]$. So Tenzing can remove $4$ balls in total.</p><p>In the second example, Tenzing will choose $i=1$ and $j=3$ in the first and only operation so that $a=[2]$. So Tenzing can remove $3$ balls in total.</p>
