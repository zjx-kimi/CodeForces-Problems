## Description

<div><p>Suppose you have an integer array $a_1, a_2, \dots, a_n$.</p><p>Let $\operatorname{lsl}(i)$ be the number of indices $j$ ($1 \le j &lt; i$) such that $a_j &lt; a_i$.</p><p>Analogically, let $\operatorname{grr}(i)$ be the number of indices $j$ ($i &lt; j \le n$) such that $a_j &gt; a_i$.</p><p>Let's name position $i$ <span class="tex-font-style-it">good</span> in the array $a$ if $\operatorname{lsl}(i) &lt; \operatorname{grr}(i)$.</p><p>Finally, let's define a function $f$ on array $a$ $f(a)$ as the <span class="tex-font-style-bf">sum</span> of all $a_i$ such that $i$ is <span class="tex-font-style-it">good</span> in $a$.</p><p>Given two integers $n$ and $k$, find the sum of $f(a)$ over all arrays $a$ of size $n$ such that $1 \leq a_i \leq k$ for all $1 \leq i \leq n$ modulo $998\,244\,353$.</p></div><div class="input-specification"><p>The first and only line contains two integers $n$ and $k$ ($1 \leq n \leq 50$; $2 \leq k &lt; 998\,244\,353$).</p></div><div class="output-specification"><p>Output a single integer&nbsp;— the sum of $f$ over all arrays $a$ of size $n$ modulo $998\,244\,353$.</p></div>

## Input

<p>The first and only line contains two integers $n$ and $k$ ($1 \leq n \leq 50$; $2 \leq k &lt; 998\,244\,353$).</p>

## Output

<p>Output a single integer&nbsp;— the sum of $f$ over all arrays $a$ of size $n$ modulo $998\,244\,353$.</p>





```input1
3 3
```




```input2
5 6
```




```input3
12 30
```




```output1
28
```




```output2
34475
```




```output3
920711694
```



## Note

<p>In the first test case: </p><center> <table class="tex-tabular"><tbody><tr><td class="tex-tabular-text-align-center tex-tabular-border-right">$f([1,1,1]) = 0$</td><td class="tex-tabular-border-left tex-tabular-text-align-center">$f([2,2,3]) = 2 + 2 = 4$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right">$f([1,1,2]) = 1 + 1 = 2$</td><td class="tex-tabular-border-left tex-tabular-text-align-center">$f([2,3,1]) = 2$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right">$f([1,1,3]) = 1 + 1 = 2$</td><td class="tex-tabular-border-left tex-tabular-text-align-center">$f([2,3,2]) = 2$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right">$f([1,2,1]) = 1$</td><td class="tex-tabular-border-left tex-tabular-text-align-center">$f([2,3,3]) = 2$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right">$f([1,2,2]) = 1$</td><td class="tex-tabular-border-left tex-tabular-text-align-center">$f([3,1,1]) = 0$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right">$f([1,2,3]) = 1$</td><td class="tex-tabular-border-left tex-tabular-text-align-center">$f([3,1,2]) = 1$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right">$f([1,3,1]) = 1$</td><td class="tex-tabular-border-left tex-tabular-text-align-center">$f([3,1,3]) = 1$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right">$f([1,3,2]) = 1$</td><td class="tex-tabular-border-left tex-tabular-text-align-center">$f([3,2,1]) = 0$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right">$f([1,3,3]) = 1$</td><td class="tex-tabular-border-left tex-tabular-text-align-center">$f([3,2,2]) = 0$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right">$f([2,1,1]) = 0$</td><td class="tex-tabular-border-left tex-tabular-text-align-center">$f([3,2,3]) = 2$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right">$f([2,1,2]) = 1$</td><td class="tex-tabular-border-left tex-tabular-text-align-center">$f([3,3,1]) = 0$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right">$f([2,1,3]) = 2 + 1 = 3$</td><td class="tex-tabular-border-left tex-tabular-text-align-center">$f([3,3,2]) = 0$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right">$f([2,2,1]) = 0$</td><td class="tex-tabular-border-left tex-tabular-text-align-center">$f([3,3,3]) = 0$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right">$f([2,2,2]) = 0$</td><td class="tex-tabular-border-left tex-tabular-text-align-center"></td></tr></tbody></table> </center><p>Adding up all of these values, we get $28$ as the answer.</p>
