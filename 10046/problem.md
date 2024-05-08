## Description

<div><p><span class="tex-font-style-bf">This is an interactive problem.</span></p><p>There is a secret sequence $p_0, p_1, \ldots, p_{n-1}$, which is a permutation of $\{0,1,\ldots,n-1\}$.</p><p>You need to find any two indices $i$ and $j$ such that $p_i \oplus p_j$ is maximized, where $\oplus$ denotes the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#XOR">bitwise XOR operation</a>.</p><p>To do this, you can ask queries. Each query has the following form: you pick arbitrary indices $a$, $b$, $c$, and $d$ ($0 \le a,b,c,d &lt; n$). Next, the jury calculates $x = (p_a \mid p_b)$ and $y = (p_c \mid p_d)$, where $|$ denotes the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#OR">bitwise OR operation</a>. Finally, you receive the result of comparison between $x$ and $y$. In other words, you are told if $x &lt; y$, $x &gt; y$, or $x = y$.</p><p>Please find any two indices $i$ and $j$ ($0 \le i,j &lt; n$) such that $p_i \oplus p_j$ is maximum among all such pairs, using at most $3n$ queries. If there are multiple pairs of indices satisfying the condition, you may output any one of them.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^3$). The description of the test cases follows.</p></div><div><h2>Interaction</h2><p>The first line of each test case contains one integer $n$ ($2 \le n \le 10^4$). At this moment, the permutation $p_0, p_1, \ldots, p_{n-1}$ is chosen. The interactor in this task is <span class="tex-font-style-bf">not adaptive</span>. In other words, the sequence $p$ is fixed in every test case and does not change during the interaction.</p><p>To ask a query, you need to pick four indices $a$, $b$, $c$, and $d$ ($0 \le a,b,c,d &lt; n$) and print the line of the following form:</p><ul> <li> "<span class="tex-font-style-tt">? a b c d</span>" </li></ul><p>After that, you receive:</p><ul> <li> "<span class="tex-font-style-tt">&lt;</span>" if $(p_a \mid p_b) &lt; (p_c \mid p_d)$; </li><li> "<span class="tex-font-style-tt">=</span>" if $(p_a \mid p_b) = (p_c \mid p_d)$; </li><li> "<span class="tex-font-style-tt">&gt;</span>" if $(p_a \mid p_b) &gt; (p_c \mid p_d)$. </li></ul><p>You can make at most $3n$ queries of this form.</p><p>Next, if your program has found a pair of indices $i$ and $j$ ($0 \le i, j &lt; n$) such that $p_i \oplus p_j$ is maximized, print the line of the following form:</p><ul> <li> "<span class="tex-font-style-tt">! i j</span>" </li></ul><p>Note that this line is <span class="tex-font-style-bf">not</span> considered a query and is <span class="tex-font-style-bf">not</span> taken into account when counting the number of queries asked.</p><p>After this, proceed to the next test case.</p><p>If you make more than $3n$ queries during an interaction, your program must terminate immediately, and you will receive the <span class="tex-font-style-tt">Wrong Answer</span> verdict. Otherwise, you can get an arbitrary verdict because your solution will continue to read from a closed stream.</p><p>After printing a query or the answer for a test case, do not forget to output the end of line and flush the output. Otherwise, you will get the verdict <span class="tex-font-style-tt">Idleness Limit Exceeded</span>. To do this, use:</p><ul> <li> <span class="tex-font-style-tt">fflush(stdout)</span> or <span class="tex-font-style-tt">cout.flush()</span> in C++; </li><li> <span class="tex-font-style-tt">System.out.flush()</span> in Java; </li><li> <span class="tex-font-style-tt">flush(output)</span> in Pascal; </li><li> <span class="tex-font-style-tt">stdout.flush()</span> in Python; </li><li> see the documentation for other languages. </li></ul><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^4$.</p><p><span class="tex-font-style-bf">Hacks</span></p><p>To hack, follow the test format below.</p><p>The first line contains the number of test cases $t$ ($1 \le t \le 10^3$). The description of the test cases follows.</p><p>The first line of each test case contains one integer $n$ ($2 \le n \le 10^4$).</p><p>The second line of each test case contains $n$ integers $p_0,p_1,\ldots,p_{n-1}$, which represent a permutation of integers from $0$ to $n - 1$.</p><p>The sum of $n$ over all test cases should not exceed $10^4$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^3$). The description of the test cases follows.</p>





```input1
2
4

&lt;

=

&gt;

2
```




```output1
? 0 2 3 1

? 1 1 2 3

? 1 2 0 3

! 3 2

! 0 1
```



## Note

<p>In the first test case, the hidden permutation is $p=[0,3,1,2]$.</p><p>For the query "<span class="tex-font-style-tt">? 0 2 3 1</span>", the jury return "<span class="tex-font-style-tt">&lt;</span>" because $(p_0 \mid p_2) = (0 \mid 1) =1 &lt; (p_3 \mid p_1) = (2 \mid 3) = 3$.</p><p>For the query "<span class="tex-font-style-tt">? 1 1 2 3</span>", the jury return "<span class="tex-font-style-tt">=</span>" because $(p_1 \mid p_1) = (3\mid 3)= 3 = (p_2 \mid p_3) = (1 \mid 2)=3$.</p><p>For the query "<span class="tex-font-style-tt">? 1 2 0 3</span>", the jury return "<span class="tex-font-style-tt">&gt;</span>" because $(p_1 \mid p_2) = (3 \mid 1) = 3 &gt; (p_0 \mid p_3) = (0\mid 2)=2$.</p><p>The answer $i = 3$ and $j = 2$ is valid: $(p_3 \oplus p_2) = (2 \oplus 1) = 3$ is indeed equal to the maximum possible value of $p_i \oplus p_j$. Another valid answer would be $i=0$ and $j=1$. As the number of queries does not exceed $3n=12$, the answer is considered correct.</p><p>In the second test case, $n = 2$, so $p$ is either $[0, 1]$ or $[1, 0]$. In any case, $p_0 \oplus p_1 = 1$ is maximum possible.</p>
