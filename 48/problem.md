## Description

<div><p>Alex is solving a problem. He has $n$ constraints on what the integer $k$ can be. There are three types of constraints:</p><ol> <li> $k$ must be <span class="tex-font-style-bf">greater than or equal to</span> some integer $x$; </li><li> $k$ must be <span class="tex-font-style-bf">less than or equal to</span> some integer $x$; </li><li> $k$ must be <span class="tex-font-style-bf">not equal to</span> some integer $x$. </li></ol><p>Help Alex find the number of integers $k$ that satisfy all $n$ constraints. It is guaranteed that the <span class="tex-font-style-bf">answer is finite</span> (there exists at least one constraint of type $1$ and at least one constraint of type $2$). Also, it is guaranteed that <span class="tex-font-style-bf">no two constraints are the exact same</span>.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 500$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \leq n \leq 100$) — the number of constraints.</p><p>The following $n$ lines describe the constraints. Each line contains two integers $a$ and $x$ ($a \in \{1,2,3\}, \, 1 \leq x \leq 10^9$). $a$ denotes the type of constraint. If $a=1$, $k$ must be greater than or equal to $x$. If $a=2$, $k$ must be less than or equal to $x$. If $a=3$, $k$ must be not equal to $x$.</p><p>It is guaranteed that there is a finite amount of integers satisfying all $n$ constraints (there exists at least one constraint of type $1$ and at least one constraint of type $2$). It is also guaranteed that no two constraints are the exact same (in other words, all pairs $(a, x)$ are distinct).</p></div><div class="output-specification"><p>For each test case, output a single integer — the number of integers $k$ that satisfy all $n$ constraints.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 500$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \leq n \leq 100$) — the number of constraints.</p><p>The following $n$ lines describe the constraints. Each line contains two integers $a$ and $x$ ($a \in \{1,2,3\}, \, 1 \leq x \leq 10^9$). $a$ denotes the type of constraint. If $a=1$, $k$ must be greater than or equal to $x$. If $a=2$, $k$ must be less than or equal to $x$. If $a=3$, $k$ must be not equal to $x$.</p><p>It is guaranteed that there is a finite amount of integers satisfying all $n$ constraints (there exists at least one constraint of type $1$ and at least one constraint of type $2$). It is also guaranteed that no two constraints are the exact same (in other words, all pairs $(a, x)$ are distinct).</p>

## Output

<p>For each test case, output a single integer — the number of integers $k$ that satisfy all $n$ constraints.</p>





```input1|2,3,4,5,6,10,11,12,13,14,15,16,17,18,19,20,28,29,30,31,32,33
6
4
1 3
2 10
3 1
3 5
2
1 5
2 4
10
3 6
3 7
1 2
1 7
3 100
3 44
2 100
2 98
1 3
3 99
6
1 5
2 10
1 9
2 2
3 2
3 9
5
1 1
2 2
3 1
3 2
3 3
6
1 10000
2 900000000
3 500000000
1 100000000
3 10000
3 900000001
```




```output1
7
0
90
0
0
800000000
```



## Note

<p>In the first test case, $k \geq 3$ and $k \leq 10$. Furthermore, $k \neq 1$ and $k \neq 5$. The possible integers $k$ that satisfy the constraints are $3,4,6,7,8,9,10$. So the answer is $7$.</p><p>In the second test case, $k \ge 5$ and $k \le 4$, which is impossible. So the answer is $0$.</p>
