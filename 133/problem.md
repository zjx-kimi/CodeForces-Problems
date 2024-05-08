## Description

<div><div class="epigraph"><div class="epigraph-text"><span class="tex-font-style-it"><a href="https://soundcloud.com/yugenero/xi-solar-storm">xi - Solar Storm</a></span></div><div class="epigraph-source">⠀</div></div><p>You are given an array $a_1, a_2, \dots, a_n$ of distinct positive integers. You have to do the following operation <span class="tex-font-style-bf">exactly once</span>:</p><ul> <li> choose a positive integer $k$; </li><li> for each $i$ from $1$ to $n$, replace $a_i$ with $a_i \text{ mod } k^\dagger$. </li></ul><p>Find a value of $k$ such that $1 \leq k \leq 10^{18}$ and the array $a_1, a_2, \dots, a_n$ contains <span class="tex-font-style-bf">exactly</span> $2$ distinct values at the end of the operation. It can be shown that, under the constraints of the problem, at least one such $k$ always exists. If there are multiple solutions, you can print any of them.</p><p>$^\dagger$ $a \text{ mod } b$ denotes the remainder after dividing $a$ by $b$. For example: </p><ul> <li> $7 \text{ mod } 3=1$ since $7 = 3 \cdot 2 + 1$ </li><li> $15 \text{ mod } 4=3$ since $15 = 4 \cdot 3 + 3$ </li><li> $21 \text{ mod } 1=0$ since $21 = 21 \cdot 1 + 0$ </li></ul></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 500$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 100$)&nbsp;— the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^{17}$)&nbsp;— the initial state of the array. It is guaranteed that all the $a_i$ are distinct.</p><p>Note that there are no constraints on the sum of $n$ over all test cases.</p></div><div class="output-specification"><p>For each test case, output a single integer: a value of $k$ ($1 \leq k \leq 10^{18}$) such that the array $a_1, a_2, \dots, a_n$ contains exactly $2$ distinct values at the end of the operation.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 500$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 100$)&nbsp;— the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^{17}$)&nbsp;— the initial state of the array. It is guaranteed that all the $a_i$ are distinct.</p><p>Note that there are no constraints on the sum of $n$ over all test cases.</p>

## Output

<p>For each test case, output a single integer: a value of $k$ ($1 \leq k \leq 10^{18}$) such that the array $a_1, a_2, \dots, a_n$ contains exactly $2$ distinct values at the end of the operation.</p>





```input1|2,3,6,7,10,11
5
4
8 15 22 30
5
60 90 98 120 308
6
328 769 541 986 215 734
5
1000 2000 7000 11000 16000
2
2 1
```




```output1
7
30
3
5000
1000000000000000000
```



## Note

<p>In the first test case, you can choose $k = 7$. The array becomes $[8 \text{ mod } 7, 15 \text{ mod } 7, 22 \text{ mod } 7, 30 \text{ mod } 7] = [1, 1, 1, 2]$, which contains exactly $2$ distinct values ($\{1, 2\}$).</p><p>In the second test case, you can choose $k = 30$. The array becomes $[0, 0, 8, 0, 8]$, which contains exactly $2$ distinct values ($\{0, 8\}$). Note that choosing $k = 10$ would also be a valid solution.</p><p>In the last test case, you can choose $k = 10^{18}$. The array becomes $[2, 1]$, which contains exactly $2$ distinct values ($\{1, 2\}$). Note that choosing $k = 10^{18} + 1$ would not be valid, because $1 \leq k \leq 10^{18}$ must be true.</p>
