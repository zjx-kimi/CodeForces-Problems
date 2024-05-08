## Description

<div><p>Tema decided to improve his ice cream making skills. He has already learned how to make ice cream in a cone <span class="tex-font-style-bf">using exactly two</span> balls.</p><p>Before his ice cream obsession, Tema was interested in mathematics. Therefore, he is curious about the <span class="tex-font-style-bf">minimum</span> number of balls he needs to have in order to make <span class="tex-font-style-bf">exactly</span> $n$ <span class="tex-font-style-bf">different</span> types of ice cream.</p><p>There are plenty possible ice cream flavours: $1, 2, 3, \dots$. Tema can make two-balls ice cream with any flavours (probably the same).</p><p>Two ice creams are considered different if their sets of ball flavours are different. For example, $\{1, 2\} = \{2, 1\}$, but $\{1, 1\} \neq \{1, 2\}$.</p><p>For example, having the following ice cream balls: $\{1, 1, 2\}$, Tema can make only two types of ice cream: $\{1, 1\}$ and $\{1, 2\}$.</p><p><span class="tex-font-style-bf">Note, that Tema do not need to make all the ice cream cones at the same time. This means that he making ice cream cones independently. Also in order to make a following cone $\{x, x\}$ for some $x$, Tema needs at least $2$ balls of type $x$</span>.</p><p>Help Tema answer this question. It can be shown that answer always exist.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line of input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then follows the description of the test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^{18}$)&nbsp;— the number of ice cream types that Tema wants to make.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the minimum number of balls Tema needs to buy.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line of input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then follows the description of the test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^{18}$)&nbsp;— the number of ice cream types that Tema wants to make.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the minimum number of balls Tema needs to buy.</p>





```input1|2,4,6
5
1
3
6
179
1000000000000000000
```




```output1
2
3
4
27
2648956421
```



## Note

<p>In the first sample, it is enough to have following balls types: $\{1, 1\}$. <span class="tex-font-style-bf">Note, that set $\{1\}$ if not enough since we need at least $2$ balls of a type $1$ in order to make such cone $\{1, 1\}$</span>.</p><p>In the second sample, it is not possible to make it with $2$ balls, but it can be done with these balls: $\{1, 2, 3\}$.</p><p>In the third sample, $\{1, 2, 3, 4\}$ is optimal answer, so we can get following ice cream cones: $\{1, 2\}$, $\{1, 3\}$, $\{1, 4\}$, $\{2, 3\}$, $\{2, 4\}$, $\{3, 4\}$.</p>
