## Description

<div><p>In the village of Letovo, there are $n$ houses. The villagers decided to build a big road that will divide the village into left and right sides. Each resident wants to live on either the right or the left side of the street, which is described as a sequence $a_1, a_2, \dots, a_n$, where $a_j = 0$ if the resident of the $j$-th house wants to live on the left side of the street; otherwise, $a_j = 1$.</p><p>The road will pass between two houses. The houses to the left of it will be declared the left-side, and the houses to the right will be declared the right-side. More formally, let the road pass between houses $i$ and $i+1$. Then the houses at positions between $1$ and $i$ will be on the <span class="tex-font-style-bf">left</span> side of the street, and at positions between $i+1$ and $n$ will be on the <span class="tex-font-style-bf">right</span> side. The road also <span class="tex-font-style-bf">may</span> pass before the first and after the last house; in this case, the entire village is declared to be either the right or left side, respectively.</p><p>To make the design fair, it was decided to lay the road so that at least half of the residents on each side of the village are satisfied with the choice. That is, among $x$ residents on one side, at least $\lceil\frac{x}{2}\rceil$ should want to live on that side, where $\lceil x \rceil$ denotes rounding up a real number $x$.</p><center> <img class="tex-graphics" src="file://SoZF373O.png" style="max-width: 100.0%;max-height: 100.0%;">   <span class="tex-font-size-small">To the left of the road, there will be $i$ houses, among the corresponding $a_j$ there must be at least $\lceil\frac{i}{2}\rceil$ zeros. To the right of the road, there will be $n-i$ houses, among the corresponding $a_j$ there must be at least $\lceil\frac{n-i}{2}\rceil$ ones.</span> </center><p>Determine after which house $i$ the road should be laid in order to satisfy the described condition and be as close to the middle of the village as possible. Formally, among all suitable positions $i$, minimize $\left|\frac{n}{2} - i\right|$.</p><p>If there are multiple suitable positions $i$ with the minimum $\left|\frac{n}{2} - i\right|$, output the smaller one.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 2\cdot 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($3 \le n \le 3\cdot 10^5$). The next line of each test case contains a string $a$ of length $n$, consisting only of $0$ and $1$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $3\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single number $i$&nbsp;— the position of the house after which the road should be laid (if it should be laid before the first house, output $0$). We can show that the answer always exists.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 2\cdot 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($3 \le n \le 3\cdot 10^5$). The next line of each test case contains a string $a$ of length $n$, consisting only of $0$ and $1$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $3\cdot 10^5$.</p>

## Output

<p>For each test case, output a single number $i$&nbsp;— the position of the house after which the road should be laid (if it should be laid before the first house, output $0$). We can show that the answer always exists.</p>





```input1|2,3,6,7,10,11,14,15
7
3
101
6
010111
6
011001
3
000
3
110
3
001
4
1100
```




```output1
2
3
2
3
0
1
0
```



## Note

<p>Let's consider the first example of input data.</p><p>If we lay the road after the first house, there will be one house $a_1 = 1$ on the left side of the street, the resident of which would like to live on the right side of the street. Then $0$ out of $1$ residents on the even side will be satisfied with the choice, which means that the road cannot be laid after house $1$.</p><p>If we lay the road after the second house, $1$ out of $2$ residents on the left side (with preferences $a_1 = 1$, $a_2 = 0$) and $1$ out of $1$ resident on the right side (with preference $a_3 = 1$) will be satisfied with the choice. More than half of the residents on each side are satisfied with the choice, which means that the road can be laid after house $2$. We can show that this is the optimal answer.</p>
