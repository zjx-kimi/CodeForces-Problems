## Description

<div><p><span class="tex-font-style-bf">In the easy version, $m = n-1$ and there exists a path between $u$ and $v$ for all $u, v$ ($1 \leq u, v \leq n$).</span></p><p>After a worker's strike organized by the Dementors asking for equal rights, the prison of Azkaban has suffered some damage. After settling the spirits, the Ministry of Magic is looking to renovate the prison to ensure that the Dementors are kept in check. The prison consists of $n$ prison cells and $m$ bi-directional corridors. The $i^{th}$ corridor is from cells $u_i$ to $v_i$. A subset of these cells $S$ is called a complex if any cell in $S$ is reachable from any other cell in $S$. Formally, a subset of cells $S$ is a complex if $x$ and $y$ are reachable from each other for all $x, y \in S$, using only cells from $S$ on the way. The funding required for a complex $S$ consisting of $k$ cells is defined as $k^2$.</p><p>As part of your <span class="tex-font-style-it">Intro to Magical Interior Design</span> course at Hogwarts, you have been tasked with designing the prison. The Ministry of Magic has asked that you divide the prison into $2$ complexes with $\textbf{exactly one corridor}$ connecting them, so that the Dementors can't organize union meetings. For this purpose, you are allowed to build bi-directional corridors. The funding required to build a corridor between any $2$ cells is $c$. </p><p>Due to budget cuts and the ongoing fight against the Death Eaters, you must find the $\textbf{minimum total funding}$ required to divide the prison as per the Ministry's requirements or $-1$ if no division is possible.</p><p>Note: The total funding is the sum of the funding required for the $2$ complexes and the corridors built. If after the division, the two complexes have $x$ and $y$ cells respectively and you have built a total of $a$ corridors, the total funding will be $x^2 + y^2 + c \times a$. Note that $x+y=n$.</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \leq t \leq 10^5$) — the number of test cases. Then $t$ test cases follow.</p><p>The first line of each test case consists of three integers $n, m$ and $c$ ($2 \leq n \leq 10^5$, $m = n - 1$, $1 \leq c \leq 10^9$)</p><p>$m$ lines follow, each consisting of 2 integers — $u_i, v_i$ indicating a corridor is present between cells $u_i$ and $v_i$ ($1 \leq u_i, v_i \leq n$, $u_i \neq v_i$)</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p><p>It is guaranteed that the sum of $m$ over all test cases does not exceed $5 \times 10^5$.</p><p>It is guaranteed that there exists at most one corridor between any two cells.</p></div><div class="output-specification"><p>Print the $\textbf{minimum funding}$ required to divide the prison as per the Ministry's requirements or $-1$ if no division is possible.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \leq t \leq 10^5$) — the number of test cases. Then $t$ test cases follow.</p><p>The first line of each test case consists of three integers $n, m$ and $c$ ($2 \leq n \leq 10^5$, $m = n - 1$, $1 \leq c \leq 10^9$)</p><p>$m$ lines follow, each consisting of 2 integers — $u_i, v_i$ indicating a corridor is present between cells $u_i$ and $v_i$ ($1 \leq u_i, v_i \leq n$, $u_i \neq v_i$)</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p><p>It is guaranteed that the sum of $m$ over all test cases does not exceed $5 \times 10^5$.</p><p>It is guaranteed that there exists at most one corridor between any two cells.</p>

## Output

<p>Print the $\textbf{minimum funding}$ required to divide the prison as per the Ministry's requirements or $-1$ if no division is possible.</p>





```input1
2
2 1 3
1 2
8 7 76
3 1
3 2
2 4
2 5
4 6
4 7
7 8
```




```output1
2
32
```


