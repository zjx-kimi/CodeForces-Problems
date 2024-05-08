## Description

<div><p><span class="tex-font-style-it">This is an interactive problem.</span></p><p>There are $n^2$ pepes labeled $1, 2, \ldots, n^2$ with <span class="tex-font-style-bf">pairwise distinct</span> speeds. You would like to set up some races to find out the relative speed of these pepes.</p><p>In one race, you can choose exactly $n$ distinct pepes and make them race against each other. After each race, you will only know the <span class="tex-font-style-bf">fastest</span> pepe of these $n$ pepes.</p><p>Can you order the $n^2-n+1$ fastest pepes in <span class="tex-font-style-bf">at most</span> $2n^2 - 2n + 1$ races? Note that the slowest $n - 1$ pepes are indistinguishable from each other.</p><p>Note that the interactor is <span class="tex-font-style-bf">adaptive</span>. That is, the relative speeds of the pepes are not fixed in the beginning and may depend on your queries. But it is guaranteed that at any moment there is at least one initial configuration of pepes such that all the answers to the queries are consistent.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The only line of each test case contains a single integer $n$ ($2 \le n \le 20$)&nbsp;— the number of pepes in one race.</p><p>After reading the integer $n$ for each test case, you should begin the interaction.</p><p>It is guaranteed that the sum of $n^3$ over all test cases does not exceed $3 \cdot 10^5$.</p></div><div><h2>Interaction</h2><p>To set up a race, print a line with the following format: </p><ul> <li> $\mathtt{?}\,x_1\,x_2 \ldots x_n$ ($1 \le x_i \le n^2$, $x_i$ are pairwise distinct)&nbsp;— the labels of the pepes in the race. </li></ul><p>After each race, you should read a line containing a single integer $p$ ($1\le p\le n^2$) — the label of the fastest pepe in the race.</p><p>When you know the $n^2-n+1$ fastest pepes, print one line in the following format: </p><ul> <li> $\mathtt{!}\,p_1\,p_2 \ldots p_{n^2 - n + 1}$ ($1 \le p_i \le n^2$, $p_i$ are pairwise distinct) </li></ul> where $p$ is the sequence of these pepe's labels in descending order of speed.<p>After that, move on to the next test case, or terminate the program if no more test cases are remaining.</p><p>If your program performs more than $2n^2 - 2n + 1$ races for one test case or makes an invalid race, you may receive a Wrong Answer verdict.</p><p>After printing a query do not forget to output the end of the line and flush the output. Otherwise, you will get <span class="tex-font-style-tt">Idleness limit exceeded</span>. To do this, use: </p><ul> <li> <span class="tex-font-style-tt">fflush(stdout)</span> or <span class="tex-font-style-tt">cout.flush()</span> in C++; </li><li> <span class="tex-font-style-tt">System.out.flush()</span> in Java; </li><li> <span class="tex-font-style-tt">flush(output)</span> in Pascal; </li><li> <span class="tex-font-style-tt">stdout.flush()</span> in Python; </li><li> see the documentation for other languages. </li></ul><p><span class="tex-font-style-bf">Hack format</span></p><p>For hacks, use the following format.</p><p>The first line should contain $t$&nbsp;— the number of test cases.</p><p>The first line of each test case should contain an integer $n$ followed by the string <span class="tex-font-style-tt">manual</span>.</p><p>The second line of each test case should contain a permutation $a_1,a_2,\ldots,a_{n^2}$ of the integers from $1$ to $n^2$. $a_i &gt; a_j$ if and only if pepe $i$ has a faster speed than pepe $j$.</p><p>As an example, the hack format for the example input is: $\mathtt{1}\\\mathtt{2}~\mathtt{manual}\\\mathtt{1}~\mathtt{2}~\mathtt{3}~\mathtt{4}$</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The only line of each test case contains a single integer $n$ ($2 \le n \le 20$)&nbsp;— the number of pepes in one race.</p><p>After reading the integer $n$ for each test case, you should begin the interaction.</p><p>It is guaranteed that the sum of $n^3$ over all test cases does not exceed $3 \cdot 10^5$.</p>





```input1
1
2

2

4

4

3

2
```




```output1
? 1 2

? 3 4

? 2 4

? 2 3

? 2 1

! 4 3 2
```


