## Description

<div><p>You are given three integers $a$, $b$, and $c$ such that <span class="tex-font-style-bf">exactly one</span> of these two equations is true: </p><ul> <li> $a+b=c$ </li><li> $a-b=c$ </li></ul> Output <span class="tex-font-style-tt">+</span> if the first equation is true, and <span class="tex-font-style-tt">-</span> otherwise.</div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 162$)&nbsp;— the number of test cases.</p><p>The description of each test case consists of three integers $a$, $b$, $c$ ($1 \leq a, b \leq 9$, $-8 \leq c \leq 18$). The additional constraint on the input: it will be generated so that <span class="tex-font-style-bf">exactly</span> one of the two equations will be true.</p></div><div class="output-specification"><p>For each test case, output either <span class="tex-font-style-tt">+</span> or <span class="tex-font-style-tt">-</span> on a new line, representing the correct equation.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 162$)&nbsp;— the number of test cases.</p><p>The description of each test case consists of three integers $a$, $b$, $c$ ($1 \leq a, b \leq 9$, $-8 \leq c \leq 18$). The additional constraint on the input: it will be generated so that <span class="tex-font-style-bf">exactly</span> one of the two equations will be true.</p>

## Output

<p>For each test case, output either <span class="tex-font-style-tt">+</span> or <span class="tex-font-style-tt">-</span> on a new line, representing the correct equation.</p>





```input1|2,4,6,8,10,12
11
1 2 3
3 2 1
2 9 -7
3 4 7
1 1 2
1 1 0
3 3 6
9 9 18
9 9 0
1 9 -8
1 9 10
```




```output1
+
-
-
+
+
-
+
+
-
-
+
```



## Note

<p>In the first test case, $1+2=3$.</p><p>In the second test case, $3-2=1$.</p><p>In the third test case, $2-9=-7$. Note that $c$ can be negative.</p>
