## Description

<div><p><span class="tex-font-style-tt">This is an interactive problem!</span></p><p>In the new round, there were $n$ tasks with difficulties from $1$ to $n$. The coordinator, who decided to have the first round with tasks in unsorted order of difficulty, rearranged the tasks, resulting in a permutation of difficulties from $1$ to $n$. After that, the coordinator challenged ace5 to guess the permutation in the following way.</p><p>Initially, the coordinator chooses a number $x$ from $1$ to $n$.</p><p>ace5 can make queries of the form: $?\ i$. The answer will be: </p><ul> <li> $&gt;$, if $a_i &gt; x$, after which $x$ increases by $1$. </li><li> $&lt;$, if $a_i &lt; x$, after which $x$ decreases by $1$. </li><li> $=$, if $a_i = x$, after which $x$ remains unchanged. </li></ul><p>The task for ace5 is to guess the permutation in no more than $40n$ queries. Since ace5 is too busy writing the announcement, he has entrusted this task to you.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$) — the number of test cases.</p></div><div><h2>Interaction</h2><p>The interaction between your program and the jury's program begins with reading a positive integer $n$ ($1 \leq n \leq 2000$) — the length of the hidden permutation.</p><p>To make a query, output a line in the format "<span class="tex-font-style-tt">? i</span>", where $1 \leq i \leq n$.</p><p>As an answer, you will receive: </p><ul> <li> "<span class="tex-font-style-tt">&gt;</span>", if $a_i$ &gt; $x$, after which $x$ will increase by $1$. </li><li> "<span class="tex-font-style-tt">&lt;</span>", if $a_i$ &lt; $x$, after which $x$ will decrease by $1$. </li><li> "<span class="tex-font-style-tt">=</span>", if $a_i$ = $x$, after which $x$ will remain unchanged. </li></ul><p>You can make no more than $40n$ queries. To output the answer, you need to print "<span class="tex-font-style-tt">! a_1 a_2 ... a_n</span>", where $1 \leq a_i \leq n$, and all of them are distinct. Outputting the answer <span class="tex-font-style-bf">does not count</span> as a query.</p><p>If your program makes more than $40n$ queries for one test case, or makes an invalid query, then the <span class="tex-font-style-bf">response to the query will be</span> <span class="tex-font-style-tt">-1</span>. After receiving such a response, your program should immediately terminate to receive the verdict <span class="tex-font-style-tt">Wrong Answer</span>. Otherwise, it may receive any other verdict.</p><p>After outputting a query, do not forget to print a newline and flush the output buffer. Otherwise, you will receive the verdict <span class="tex-font-style-tt">Presentation Error</span>. To flush the buffer, use:</p><ul><li> <span class="tex-font-style-tt">fflush(stdout)</span> or <span class="tex-font-style-tt">cout.flush()</span> in C++;</li><li> <span class="tex-font-style-tt">System.out.flush()</span> in Java;</li><li> <span class="tex-font-style-tt">flush(output)</span> in Pascal;</li><li> <span class="tex-font-style-tt">stdout.flush()</span> in Python;</li><li> see the documentation for other languages.</li></ul><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2000$. </p><p>The interactor in this problem is <span class="tex-font-style-bf">not adaptive</span>.</p><p><span class="tex-font-style-bf">Hacks:</span></p><p>To make a hack, use the following format:</p><p>The first line contains a single integer $t$ — the number of test cases.</p><p>The description of each test case should consist of two lines. The first line contains the numbers $n$ and $x$ ($1 \leq x \leq n \leq 2000$) — the length of the hidden permutation and the initial value of the number $x$. The second line contains $n$ distinct numbers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq n$) — the permutation that the jury should choose in this test case.</p><p>Sum of $n$ over all test cases should not exceed $2000$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$) — the number of test cases.</p>





```input1
2
5

&gt;

=

&lt;

=

&lt;

&lt;

2

&gt;
```




```output1
? 4

? 2

? 1

? 5

? 1

? 3

! 2 4 1 5 3

? 1

! 2 1
```



## Note

<p>In the first test, the hidden permutation is $a$ = [$2,4,1,5,3$], and the initial value of $x$ is $3$.</p><p>In the second test, the hidden permutation is $a$ = [$2,1$], and the initial value of $x$ is $1$.</p>
