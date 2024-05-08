## Description

<div><p>Milica has a string $s$ of length $n$, consisting only of characters <span class="tex-font-style-tt">A</span> and <span class="tex-font-style-tt">B</span>. She wants to modify $s$ so it contains <span class="tex-font-style-bf">exactly</span> $k$ instances of <span class="tex-font-style-tt">B</span>. In one operation, she can do the following:</p><ul> <li> Select an integer $i$ ($1 \leq i \leq n$) and a character $c$ ($c$ is equal to either <span class="tex-font-style-tt">A</span> or <span class="tex-font-style-tt">B</span>). </li><li> Then, replace <span class="tex-font-style-bf">each</span> of the first $i$ characters of string $s$ (that is, characters $s_1, s_2, \ldots, s_i$) with $c$. </li></ul><p>Milica does not want to perform too many operations in order not to waste too much time on them.</p><p>She asks you to find the minimum number of operations required to modify $s$ so it contains exactly $k$ instances of <span class="tex-font-style-tt">B</span>. She also wants you to find these operations (that is, integer $i$ and character $c$ selected in each operation).</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 500$). The description of test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($3 \leq n \leq 100$, $0 \leq k \leq n$)&nbsp;— the length of the string $s$ and the number of characters <span class="tex-font-style-tt">B</span> Milica wants to appear in $s$ in the end.</p><p>The second line of each test case contains the string $s$ of length $n$, consisting only of characters <span class="tex-font-style-tt">A</span> and <span class="tex-font-style-tt">B</span>.</p></div><div class="output-specification"><p>For each test case, in the first line output a single integer $m$&nbsp;— the minimum number of operations Milica should perform.</p><p>In the $j$-th of the next $m$ lines output an integer $i$ ($1 \le i \le n$) and a character $c$ ($c$ is '<span class="tex-font-style-tt">A</span>' or '<span class="tex-font-style-tt">B</span>')&nbsp;— the parameters of the $j$-th operation as described in the statement.</p><p>If there are multiple solutions with the minimum possible number of operations, output any of them.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 500$). The description of test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($3 \leq n \leq 100$, $0 \leq k \leq n$)&nbsp;— the length of the string $s$ and the number of characters <span class="tex-font-style-tt">B</span> Milica wants to appear in $s$ in the end.</p><p>The second line of each test case contains the string $s$ of length $n$, consisting only of characters <span class="tex-font-style-tt">A</span> and <span class="tex-font-style-tt">B</span>.</p>

## Output

<p>For each test case, in the first line output a single integer $m$&nbsp;— the minimum number of operations Milica should perform.</p><p>In the $j$-th of the next $m$ lines output an integer $i$ ($1 \le i \le n$) and a character $c$ ($c$ is '<span class="tex-font-style-tt">A</span>' or '<span class="tex-font-style-tt">B</span>')&nbsp;— the parameters of the $j$-th operation as described in the statement.</p><p>If there are multiple solutions with the minimum possible number of operations, output any of them.</p>





```input1
5
5 2
AAABB
5 3
AABAB
5 0
BBBBB
3 0
BAA
10 3
BBBABBBBAB
```




```output1
0
1
1 B
1
5 A
1
2 A
1
6 A
```



## Note

<p>In the first test case, there are already $2$ characters <span class="tex-font-style-tt">B</span> in $s$, so Milica does not have to perform any operations.</p><p>In the second test case, the only way to achieve $3$ characters <span class="tex-font-style-tt">B</span> in $s$ in one operation is to replace the first character of $s$ by <span class="tex-font-style-tt">B</span> on the first operation: <span class="tex-font-style-tt">AABAB</span> $\rightarrow$ <span class="tex-font-style-tt"><span class="tex-font-style-underline">B</span>ABAB</span>.</p><p>In the third test case, the only way to achieve $0$ characters <span class="tex-font-style-tt">B</span> in $s$ in one operation is to replace the first $5$ characters of $s$ by <span class="tex-font-style-tt">A</span> on the first operation: <span class="tex-font-style-tt">BBBBB</span> $\rightarrow$ <span class="tex-font-style-tt"><span class="tex-font-style-underline">AAAAA</span></span>.</p><p>In the fourth test case, one of the ways to achieve $0$ characters <span class="tex-font-style-tt">B</span> in $s$ in one operation is to replace the first $2$ characters of $s$ by <span class="tex-font-style-tt">A</span> on the first operation: <span class="tex-font-style-tt">BAA</span> $\rightarrow$ <span class="tex-font-style-tt"><span class="tex-font-style-underline">AA</span>A</span>. Note that "<span class="tex-font-style-tt">1 A</span>" and "<span class="tex-font-style-tt">3 A</span>" are also correct one-operation solutions.</p>
