## Description

<div><p>Serval loves Brain Power and his brain power problem.</p><p>Serval defines that a string $T$ is <span class="tex-font-style-it">powerful</span> iff $T$ can be obtained by concatenating some string $T'$ multiple times. Formally speaking, $T$ is powerful iff there exist a string $T'$ and an integer $k\geq 2$ such that $$T=\underbrace{T'+T'+\dots+T'}_{k\text{ times}}$$</p><p>For example, <span class="tex-font-style-tt">gogogo</span> is powerful because it can be obtained by concatenating <span class="tex-font-style-tt">go</span> three times, but <span class="tex-font-style-tt">power</span> is not powerful.</p><p>Serval has a string $S$ consists of lowercase English letters. He is curious about the longest powerful subsequence of $S$, and he only needs you to find out the length of it. If all the non-empty subsequences of $S$ is not powerful, the answer is considered to be $0$.</p><p>A string $a$ is a subsequence of a string $b$ if $a$ can be obtained from $b$ by the deletion of several (possibly, zero or all) characters.</p></div><div class="input-specification"><p>The first line contains a single string $S$ ($|S|\leq 80$) consisting of lowercase English letters.</p></div><div class="output-specification"><p>Print a single integer — the length of the longest powerful subsequence of $S$. If all the non-empty subsequences of $S$ is not powerful, print $0$.</p></div>

## Input

<p>The first line contains a single string $S$ ($|S|\leq 80$) consisting of lowercase English letters.</p>

## Output

<p>Print a single integer — the length of the longest powerful subsequence of $S$. If all the non-empty subsequences of $S$ is not powerful, print $0$.</p>





```input1
buaa
```




```input2
codeforcesround
```




```input3
oooooooooooaaaaeaaiaujooooooooooooo
```




```input4
zero
```




```output1
2
```




```output2
6
```




```output3
24
```




```output4
0
```



## Note

<p>For the first sample, all of the non-empty subsequences of <span class="tex-font-style-tt">buaa</span> are listed below:</p><ul> <li> <span class="tex-font-style-tt">b</span> </li><li> <span class="tex-font-style-tt">u</span> </li><li> <span class="tex-font-style-tt">a</span> (occurred twice, <span class="tex-font-style-tt">bu<span class="tex-font-style-underline">a</span>a</span> and <span class="tex-font-style-tt">bua<span class="tex-font-style-underline">a</span></span>) </li><li> <span class="tex-font-style-tt">bu</span> </li><li> <span class="tex-font-style-tt">ba</span> (occurred twice, <span class="tex-font-style-tt"><span class="tex-font-style-underline">b</span>u<span class="tex-font-style-underline">a</span>a</span> and <span class="tex-font-style-tt"><span class="tex-font-style-underline">b</span>ua<span class="tex-font-style-underline">a</span></span>) </li><li> <span class="tex-font-style-tt">ua</span> (occurred twice, <span class="tex-font-style-tt">b<span class="tex-font-style-underline">ua</span>a</span> and <span class="tex-font-style-tt">b<span class="tex-font-style-underline">u</span>a<span class="tex-font-style-underline">a</span></span>) </li><li> <span class="tex-font-style-tt">aa</span> </li><li> <span class="tex-font-style-tt">bua</span> (occurred twice, <span class="tex-font-style-tt"><span class="tex-font-style-underline">bua</span>a</span> and <span class="tex-font-style-tt"><span class="tex-font-style-underline">bu</span>a<span class="tex-font-style-underline">a</span></span> ) </li><li> <span class="tex-font-style-tt">baa</span> </li><li> <span class="tex-font-style-tt">uaa</span> </li><li> <span class="tex-font-style-tt">buaa</span> </li></ul><p>Since $\texttt{aa} = \texttt{a} + \texttt{a}$, <span class="tex-font-style-tt">aa</span> is a powerful subsequence. It can be shown that <span class="tex-font-style-tt">aa</span> is the only powerful subsequence among them. So the answer is $2$.</p><p>For the second sample, the longest powerful subsequence is <span class="tex-font-style-tt">codcod</span> from <span class="tex-font-style-tt"><span class="tex-font-style-underline">cod</span>efor<span class="tex-font-style-underline">c</span>esr<span class="tex-font-style-underline">o</span>un<span class="tex-font-style-underline">d</span></span>. So the answer is $6$.</p>
