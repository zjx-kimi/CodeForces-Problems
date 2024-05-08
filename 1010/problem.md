## Description

<div><p><span class="tex-font-style-it">This is an interactive problem.</span></p><p>There is a secret permutation $p$ of $[0,1,2,\ldots,n-1]$. Your task is to find $2$ indices $x$ and $y$ ($1 \leq x, y \leq n$, possibly $x=y$) such that $p_x=0$ or $p_y=0$. In order to find it, you are allowed to ask <span class="tex-font-style-bf">at most</span> $2n$ queries.</p><p>In one query, you give two integers $i$ and $j$ ($1 \leq i, j \leq n$, $i \neq j$) and receive the value of $\gcd(p_i,p_j)^\dagger$.</p><p>Note that the permutation $p$ is fixed <span class="tex-font-style-bf">before</span> any queries are made and does not depend on the queries.</p><p>$^\dagger$ $\gcd(x, y)$ denotes the <a href="https://en.wikipedia.org/wiki/Greatest_common_divisor">greatest&nbsp;common divisor (GCD)</a> of integers $x$ and $y$. Note that $\gcd(x,0)=\gcd(0,x)=x$ for all positive integers $x$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \leq n \leq 2 \cdot 10^4$).</p><p>After reading the integer $n$ for each test case, you should begin the interaction.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^4$.</p></div><div><h2>Interaction</h2><p>The interaction for each test case begins by reading the integer $n$.</p><p>To make a query, output "<span class="tex-font-style-tt">?</span> $i$ $j$" ($1 \leq i, j \leq n$, $i \neq j$) without quotes. Afterwards, you should read a single integer — the answer to your query $\gcd(p_i,p_j)$. You can make at most $2n$ such queries in each test case.</p><p>If you want to print the answer, output "<span class="tex-font-style-tt">!</span> $x$ $y$" ($1 \leq x, y \leq n$) without quotes. <span class="tex-font-style-bf">After doing that, read $1$ or $-1$</span>. If $p_x=0$ or $p_y=0$, you'll receive $1$, otherwise you'll receive $-1$. If you receive $-1$, your program must terminate immediately to receive a <span class="tex-font-style-tt">Wrong Answer</span> verdict. Otherwise, you can get an arbitrary verdict because your solution will continue to read from a closed stream.</p><p>If you receive the integer $-1$ instead of an answer or a valid value of $n$, it means your program has made an invalid query, has exceeded the limit of queries, or has given an incorrect answer on the previous test case. Your program must terminate immediately to receive a <span class="tex-font-style-tt">Wrong Answer</span> verdict. Otherwise, you can get an arbitrary verdict because your solution will continue to read from a closed stream.</p><p>After printing a query or the answer, do not forget to output the end of line and flush the output. Otherwise, you will get <span class="tex-font-style-tt">Idleness limit exceeded</span>. To do this, use: </p><ul> <li> <span class="tex-font-style-tt">fflush(stdout)</span> or <span class="tex-font-style-tt">cout.flush()</span> in C++; </li><li> <span class="tex-font-style-tt">System.out.flush(</span>) in Java; </li><li> <span class="tex-font-style-tt">flush(output)</span> in Pascal; </li><li> <span class="tex-font-style-tt">stdout.flush()</span> in Python; </li><li> see documentation for other languages. </li></ul><p><span class="tex-font-style-bf">Hacks</span></p><p>To hack, use the following format.</p><p>The first line should contain a single integer $t$ ($1 \leq t \leq 10^4$).</p><p>The first line of each test case should contain a single integer $n$ ($2 \leq n \leq 2 \cdot 10^4$).</p><p>The second line of each test case should contain $n$ space separated integers $p_1,p_2,\ldots,p_n$. $p$ should be a permutation of $[0,1,2,\ldots,n-1]$.</p><p>The sum of $n$ should not exceed $2 \cdot 10^4$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \leq n \leq 2 \cdot 10^4$).</p><p>After reading the integer $n$ for each test case, you should begin the interaction.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^4$.</p>





```input1
2
2

1

1
5

2

4

1
```




```output1
? 1 2

! 1 2


? 1 2

? 2 3

! 3 3
```



## Note

<p>In the first test, the interaction proceeds as follows.</p><center> <table class="tex-tabular"><tbody><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">Solution</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">Jury</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">Explanation</td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"></td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$\texttt{2}$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">There are 2 test cases.</td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"></td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$\texttt{2}$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">In the first test case, the hidden permutation is $[1,0]$, with length $2$.</td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$\texttt{? 1 2}$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$\texttt{1}$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">The solution requests $\gcd(p_1,p_2)$, and the jury responds with $1$.</td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$\texttt{! 1 2}$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$\texttt{1}$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">The solution knows that either $p_1=0$ or $p_2=0$, and prints the answer. Since the output is correct, the jury responds with $1$ and continues to the next test case.</td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"></td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$\texttt{5}$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">In the second test case, the hidden permutation is $[2,4,0,1,3]$, with length $5$.</td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$\texttt{? 1 2}$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$\texttt{2}$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">The solution requests $\gcd(p_1,p_2)$, and the jury responds with $2$.</td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$\texttt{? 2 3}$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$\texttt{4}$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">The solution requests $\gcd(p_2,p_3)$, and the jury responds with $4$.</td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$\texttt{! 3 3}$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$\texttt{1}$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">The solution has somehow determined that $p_3=0$, and prints the answer. Since the output is correct, the jury responds with $1$.</td></tr></tbody></table> </center><p>Note that the empty lines in the example input and output are for the sake of clarity, and do not occur in the real interaction.</p><p><span class="tex-font-style-bf">After each test case, make sure to read $1$ or $-1$</span>.</p>
