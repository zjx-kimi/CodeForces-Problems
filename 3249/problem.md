## Description

<div><p>Once again, Boris needs the help of Anton in creating a task. This time Anton needs to solve the following problem:</p><p>There are two arrays of integers $a$ and $b$ of length $n$. It turned out that array $a$ contains only elements from the set $\{-1, 0, 1\}$.</p><p>Anton can perform the following sequence of operations any number of times:</p><ol>  <li> Choose any pair of indexes $(i, j)$ such that $1 \le i &lt; j \le n$. It is possible to choose the same pair $(i, j)$ more than once.  </li><li> Add $a_i$ to $a_j$. In other words, $j$-th element of the array becomes equal to $a_i + a_j$. </li></ol><p>For example, if you are given array $[1, -1, 0]$, you can transform it only to $[1, -1, -1]$, $[1, 0, 0]$ and $[1, -1, 1]$ by one operation.</p><p>Anton wants to predict if it is possible to apply some number (zero or more) of these operations to the array $a$ so that it becomes equal to array $b$. Can you help him?</p></div><div class="input-specification"><p>Each test contains multiple test cases. </p><p>The first line contains the number of test cases $t$ ($1 \le t \le 10000$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$) &nbsp;— the length of arrays.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($-1 \le a_i \le 1$) &nbsp;— elements of array $a$. There can be duplicates among elements.</p><p>The third line of each test case contains $n$ integers $b_1, b_2, \dots, b_n$ ($-10^9 \le b_i \le 10^9$) &nbsp;— elements of array $b$. There can be duplicates among elements.</p><p>It is guaranteed that the sum of $n$ over all test cases doesn't exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output one line containing "<span class="tex-font-style-tt">YES</span>" if it's possible to make arrays $a$ and $b$ equal by performing the described operations, or "<span class="tex-font-style-tt">NO</span>" if it's impossible.</p><p>You can print each letter in any case (upper or lower).</p></div>

## Input

<p>Each test contains multiple test cases. </p><p>The first line contains the number of test cases $t$ ($1 \le t \le 10000$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$) &nbsp;— the length of arrays.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($-1 \le a_i \le 1$) &nbsp;— elements of array $a$. There can be duplicates among elements.</p><p>The third line of each test case contains $n$ integers $b_1, b_2, \dots, b_n$ ($-10^9 \le b_i \le 10^9$) &nbsp;— elements of array $b$. There can be duplicates among elements.</p><p>It is guaranteed that the sum of $n$ over all test cases doesn't exceed $10^5$.</p>

## Output

<p>For each test case, output one line containing "<span class="tex-font-style-tt">YES</span>" if it's possible to make arrays $a$ and $b$ equal by performing the described operations, or "<span class="tex-font-style-tt">NO</span>" if it's impossible.</p><p>You can print each letter in any case (upper or lower).</p>





```input1
5
3
1 -1 0
1 1 -2
3
0 1 1
0 2 2
2
1 0
1 41
2
-1 0
-1 -41
5
0 1 -1 1 -1
1 1 -1 1 -1
```




```output1
YES
NO
YES
YES
NO
```



## Note

<p>In the first test-case we can choose $(i, j)=(2, 3)$ twice and after that choose $(i, j)=(1, 2)$ twice too. These operations will transform $[1, -1, 0] \to [1, -1, -2] \to [1, 1, -2]$</p><p>In the second test case we can't make equal numbers on the second position.</p><p>In the third test case we can choose $(i, j)=(1, 2)$ $41$ times. The same about the fourth test case.</p><p>In the last lest case, it is impossible to make array $a$ equal to the array $b$.</p>
