## Description

<div><p>You are the author of a Codeforces round and have prepared $n$ problems you are going to set, problem $i$ having difficulty $a_i$. You will do the following process: </p><ul> <li> remove some (possibly zero) problems from the list; </li><li> rearrange the remaining problems in any order you wish. </li></ul><p>A round is considered <span class="tex-font-style-it">balanced</span> if and only if the absolute difference between the difficulty of any two consecutive problems is at most $k$ (less or equal than $k$).</p><p>What is the minimum number of problems you have to remove so that an arrangement of problems is balanced?</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two positive integers $n$ ($1 \leq n \leq 2 \cdot 10^5$) and $k$ ($1 \leq k \leq 10^9$)&nbsp;— the number of problems, and the maximum allowed absolute difference between consecutive problems.</p><p>The second line of each test case contains $n$ space-separated integers $a_i$ ($1 \leq a_i \leq 10^9$)&nbsp;— the difficulty of each problem.</p><p>Note that the sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the minimum number of problems you have to remove so that an arrangement of problems is balanced.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two positive integers $n$ ($1 \leq n \leq 2 \cdot 10^5$) and $k$ ($1 \leq k \leq 10^9$)&nbsp;— the number of problems, and the maximum allowed absolute difference between consecutive problems.</p><p>The second line of each test case contains $n$ space-separated integers $a_i$ ($1 \leq a_i \leq 10^9$)&nbsp;— the difficulty of each problem.</p><p>Note that the sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the minimum number of problems you have to remove so that an arrangement of problems is balanced.</p>





```input1|2,3,6,7,10,11,14,15
7
5 1
1 2 4 5 6
1 2
10
8 3
17 3 1 20 12 5 17 12
4 2
2 4 6 8
5 3
2 3 19 10 8
3 4
1 10 5
8 1
8 3 1 4 5 10 7 3
```




```output1
2
0
5
0
3
1
4
```



## Note

<p>For the first test case, we can remove the first $2$ problems and construct a set using problems with the difficulties $[4, 5, 6]$, with difficulties between adjacent problems equal to $|5 - 4| = 1 \leq 1$ and $|6 - 5| = 1 \leq 1$.</p><p>For the second test case, we can take the single problem and compose a round using the problem with difficulty $10$.</p>
