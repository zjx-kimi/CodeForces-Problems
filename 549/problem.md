## Description

<div><p>You are given a string $s$ of length $n$, where each character is either <span class="tex-font-style-tt">&lt;</span> or <span class="tex-font-style-tt">&gt;</span>.</p><p>An array $a$ consisting of $n+1$ elements is compatible with the string $s$ if, for every $i$ from $1$ to $n$, the character $s_i$ represents the result of comparing $a_i$ and $a_{i+1}$, i. e.:</p><ul> <li> $s_i$ is <span class="tex-font-style-tt">&lt;</span> if and only if $a_i &lt; a_{i+1}$; </li><li> $s_i$ is <span class="tex-font-style-tt">&gt;</span> if and only if $a_i &gt; a_{i+1}$. </li></ul><p>For example, the array $[1, 2, 5, 4, 2]$ is compatible with the string <span class="tex-font-style-tt">&lt;&lt;&gt;&gt;</span>. There are other arrays with are compatible with that string, for example, $[13, 37, 42, 37, 13]$.</p><p>The <span class="tex-font-style-bf">cost</span> of the array is the number of different elements in it. For example, the cost of $[1, 2, 5, 4, 2]$ is $4$; the cost of $[13, 37, 42, 37, 13]$ is $3$.</p><p>You have to calculate the minimum cost among all arrays which are compatible with the given string $s$.</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 500$) — the number of test cases.</p><p>Each test case consists of two lines: </p><ul> <li> the first line contains one integer $n$ ($1 \le n \le 100$); </li><li> the second line contains the string $s$, consisting of $n$ characters. Each character of $s$ is either <span class="tex-font-style-tt">&lt;</span> or <span class="tex-font-style-tt">&gt;</span>. </li></ul></div><div class="output-specification"><p>For each test case, print one integer — the minimum cost among all arrays which are compatible with the given string $s$.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 500$) — the number of test cases.</p><p>Each test case consists of two lines: </p><ul> <li> the first line contains one integer $n$ ($1 \le n \le 100$); </li><li> the second line contains the string $s$, consisting of $n$ characters. Each character of $s$ is either <span class="tex-font-style-tt">&lt;</span> or <span class="tex-font-style-tt">&gt;</span>. </li></ul>

## Output

<p>For each test case, print one integer — the minimum cost among all arrays which are compatible with the given string $s$.</p>





```input1|2,3,6,7
4
4
&lt;&lt;&gt;&gt;
4
&gt;&gt;&lt;&lt;
5
&gt;&gt;&gt;&gt;&gt;
7
&lt;&gt;&lt;&gt;&lt;&gt;&lt;
```




```output1
3
3
6
2
```



## Note

<p>In the first test case of the example, the array can be $[13, 37, 42, 37, 13]$.</p><p>In the second test case of the example, the array can be $[42, 37, 13, 37, 42]$.</p>
