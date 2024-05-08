## Description

<div><p>This problem is about candy. Initially, you only have $1$ candy, and you want to have exactly $n$ candies.</p><p>You can use the two following spells in any order at most $40$ times in total.</p><ul> <li> Assume you have $x$ candies now. If you use the first spell, then $x$ candies become $2x-1$ candies. </li><li> Assume you have $x$ candies now. If you use the second spell, then $x$ candies become $2x+1$ candies. </li></ul><p>Construct a sequence of spells, such that after using them in order, you will have <span class="tex-font-style-bf">exactly</span> $n$ candies, or determine it's impossible.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases. Their description follows.</p><p>Each test case contains one line with a single integer $n$ ($2 \le n \le 10^9$) — the required final number of candies.</p></div><div class="output-specification"><p>For each test case, output the following.</p><p>If it's possible to eventually have $n$ candies within $40$ spells, in the first line print an integer $m$ ($1 \le m \le 40$), representing the total number of spells you use.</p><p>In the second print $m$ integers $a_{1}, a_{2}, \ldots, a_{m}$ ($a_{i}$ is $1$ or $2$) separated by spaces, where $a_{i} = 1$ means that you use the first spell in the $i$-th step, while $a_{i} = 2$ means that you use the second spell in the $i$-th step.</p><p>Note that you <span class="tex-font-style-bf">do not</span> have to minimize $m$, and if there are multiple solutions, you may output any one of them.</p><p>If it's impossible, output $-1$ in one line.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases. Their description follows.</p><p>Each test case contains one line with a single integer $n$ ($2 \le n \le 10^9$) — the required final number of candies.</p>

## Output

<p>For each test case, output the following.</p><p>If it's possible to eventually have $n$ candies within $40$ spells, in the first line print an integer $m$ ($1 \le m \le 40$), representing the total number of spells you use.</p><p>In the second print $m$ integers $a_{1}, a_{2}, \ldots, a_{m}$ ($a_{i}$ is $1$ or $2$) separated by spaces, where $a_{i} = 1$ means that you use the first spell in the $i$-th step, while $a_{i} = 2$ means that you use the second spell in the $i$-th step.</p><p>Note that you <span class="tex-font-style-bf">do not</span> have to minimize $m$, and if there are multiple solutions, you may output any one of them.</p><p>If it's impossible, output $-1$ in one line.</p>





```input1|2,4
4
2
3
7
17
```




```output1
-1
1
2 
2
2 2 
4
2 1 1 1
```



## Note

<p>For $n=3$, you can just use the second spell once, and then have $2 \cdot 1 + 1 = 3$ candies.</p><p>For $n=7$, you can use the second spell twice. After the first step, you will have $3$ candies. And after the second step, you will have $2 \cdot 3 + 1 = 7$ candies.</p>
