## Description

<div><p>You are given an integer array $a_1, a_2, \dots, a_n$, all its elements are distinct.</p><p>First, you are asked to insert one more integer $a_{n+1}$ into this array. $a_{n+1}$ should not be equal to any of $a_1, a_2, \dots, a_n$.</p><p>Then, you will have to make all elements of the array equal. At the start, you choose a <span class="tex-font-style-bf">positive</span> integer $x$ ($x &gt; 0$). In one operation, you add $x$ to exactly one element of the array. <span class="tex-font-style-bf">Note that $x$ is the same for all operations</span>.</p><p>What's the smallest number of operations it can take you to make all elements equal, after you choose $a_{n+1}$ and $x$?</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$).</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($-10^9 \le a_i \le 10^9$). All $a_i$ are distinct.</p><p>The sum of $n$ over all testcases doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each testcase, print a single integer&nbsp;— the smallest number of operations it can take you to make all elements equal, after you choose integers $a_{n+1}$ and $x$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$).</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($-10^9 \le a_i \le 10^9$). All $a_i$ are distinct.</p><p>The sum of $n$ over all testcases doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>For each testcase, print a single integer&nbsp;— the smallest number of operations it can take you to make all elements equal, after you choose integers $a_{n+1}$ and $x$.</p>





```input1|2,3,6,7
3
3
1 2 3
5
1 -19 17 -3 -15
1
10
```




```output1
6
27
1
```



## Note

<p>In the first testcase, you can choose $a_{n+1} = 4$, the array becomes $[1, 2, 3, 4]$. Then choose $x = 1$ and apply the operation $3$ times to the first element, $2$ times to the second element, $1$ time to the third element and $0$ times to the fourth element.</p><p>In the second testcase, you can choose $a_{n+1} = 13, x = 4$.</p><p>In the third testcase, you can choose $a_{n+1} = 9, x = 1$. Then apply the operation once to $a_{n+1}$.</p>
