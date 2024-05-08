## Description

<div><p>You are given a string $s$ with length $n-1$ whose characters are either $\texttt{&lt;}$ or $\texttt{&gt;}$.</p><p>Count the permutations $p_1, \, p_2, \, \dots, \, p_n$ of $1, \, 2, \, \dots, \, n$ such that, for all $i = 1, \, 2, \, \dots, \, n - 1$, if $s_i$ is $\texttt{&lt;}$ then $p_i &lt; p_{i+1}$ and if $s_i$ is $\texttt{&gt;}$ then $p_i &gt; p_{i+1}$.</p><p>Since this number can be very large, compute its logarithm in base $2$.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($2 \le n \le 100\,000$).</p><p>The second line contains a string $s$ of length $n-1$; each character of $s$ is either $\texttt{&lt;}$ or $\texttt{&gt;}$.</p></div><div class="output-specification"><p>Print the logarithm in base $2$ of the number of permutations satisfying the constraints described in the statement.</p><p>Your answer is considered correct if its absolute or relative error does not exceed $10^{-6}$. Formally, let your answer be $x$ and let the correct answer be $y$. Your answer is accepted if and only if $\frac{|x - y|}{\max{(1, |y|)}} \le 10^{-6}$.</p></div>

## Input

<p>The first line contains a single integer $n$ ($2 \le n \le 100\,000$).</p><p>The second line contains a string $s$ of length $n-1$; each character of $s$ is either $\texttt{&lt;}$ or $\texttt{&gt;}$.</p>

## Output

<p>Print the logarithm in base $2$ of the number of permutations satisfying the constraints described in the statement.</p><p>Your answer is considered correct if its absolute or relative error does not exceed $10^{-6}$. Formally, let your answer be $x$ and let the correct answer be $y$. Your answer is accepted if and only if $\frac{|x - y|}{\max{(1, |y|)}} \le 10^{-6}$.</p>





```input1
2
&lt;
```




```input2
3
&lt;&gt;
```




```input3
5
&gt;&lt;&lt;&lt;
```




```input4
10
&lt;&gt;&lt;&lt;&lt;&lt;&lt;&gt;&gt;
```




```output1
0.0000000000
```




```output2
1.0000000000
```




```output3
2.0000000000
```




```output4
9.8281364842
```



## Note

<p>In the <span class="tex-font-style-bf">first sample</span>, there is only one valid permutation, that is $[2, 1]$. Since $\log_2(1)=0$, the correct output is $0$.</p><p>In the <span class="tex-font-style-bf">second sample</span>, there are $2$ valid permutations, that are $[3, 1, 2]$ and $[2, 1, 3]$. Since $\log_2(2)=1$, the correct output is $1$.</p><p>In the <span class="tex-font-style-bf">third sample</span>, there are $4$ valid permutations, that are $[1, 5, 4, 3, 2]$, $[2, 5, 4, 3, 1]$, $[3, 5, 4, 2, 1]$, $[4, 5, 3, 2, 1]$. Since $\log_2(4)=2$, the correct output is $2$.</p><p>In the <span class="tex-font-style-bf">fourth sample</span>, there are $909$ valid permutations. Notice that $\log_2(909)=9.828136484194\ldots$</p>
