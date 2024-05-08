## Description

<div><p><span class="tex-font-style-bf">This is the simple version of the problem. The only difference between the versions is the limit on the number of queries. In this version, you can make no more than 100 queries. You can make hacks only if both versions of the problem are solved.</span></p><p><span class="tex-font-style-bf">This is an interactive problem!</span></p><p>salyg1n has given you a positive integer $k$ and wants to play a game with you. He has chosen an array of $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$). You must print $a_1 \oplus a_2 \oplus \ldots \oplus a_n$, where $\oplus$ denotes the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#XOR">bitwise XOR</a> operation. You can make queries of the following type:</p><ul> <li> $?$ $i$: in response to this query, you will receive $a_i \oplus a_{i + 1} \oplus \ldots \oplus a_{i + k - 1}$. Also, after this query, the subarray $a_i, a_{i + 1}, \ldots, a_{i + k - 1}$ will be reversed, i.e., the chosen array $a$ will become: $a_1, a_2, \ldots a_{i - 1}, a_{i + k - 1}, a_{i + k - 2}, \ldots, a_{i + 1}, a_i, a_{i + k}, \ldots, a_n$. </li></ul><p>You can make no more than $100$ queries to answer the problem.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$) – the number of test cases.</p></div><div><h2>Interaction</h2><p>The interaction between your program and the jury's program begins with reading two positive <span class="tex-font-style-bf">even</span> integers $n$ and $k$ ($1 \leq k \leq n \leq k^2 \leq 2500$) – the length of the chosen array and the length of the query subarray, respectively.</p><p>To find the value of $a_i \oplus a_{i + 1} \oplus \ldots \oplus a_{i + k - 1}$, print the query in the format $?$ $i$ ($1 \leq i \leq n - k + 1$). Then read a single integer – the answer to your query.</p><p>You can make no more than $100$ queries. When you are ready to print the answer, output it in the format $!$ $x$. After that, proceed to process the next test case or terminate the program if it was the last test case. Printing the answer does not count as one of the $100$ queries.</p><p>If your program makes more than $100$ queries for one set of input data, or makes an invalid query, then the <span class="tex-font-style-bf">response to the query will be</span> <span class="tex-font-style-tt">-1</span>. After receiving such a response, your program should immediately terminate to receive the verdict <span class="tex-font-style-tt">Wrong Answer</span>. Otherwise, it may receive any other verdict.</p><p>After printing a query do not forget to output the end of line and flush the output. Otherwise, you will get <span class="tex-font-style-tt">Idleness limit exceeded</span>. To do this, use:</p><ul><li> <span class="tex-font-style-tt">fflush(stdout)</span> or <span class="tex-font-style-tt">cout.flush()</span> in C++;</li><li> <span class="tex-font-style-tt">System.out.flush()</span> in Java;</li><li> <span class="tex-font-style-tt">flush(output)</span> in Pascal;</li><li> <span class="tex-font-style-tt">stdout.flush()</span> in Python;</li><li> see the documentation for other languages.</li></ul> It is guaranteed that the sum of $n$ over all test cases does not exceed $10000$. The interactor in this problem is not adaptive.<p><span class="tex-font-style-bf">Hacks:</span></p><p>To perform a hack, use the following format:</p><p>The first line contains a single integer $t$ – the number of test cases.</p><p>The description of each test case should consist of two lines. The first line contains the numbers $n$ and $k$ – the length of the chosen array and the length of the query subarray, respectively. The second line contains $n$ numbers $a_1, a_2, \ldots, a_n$ – the array that the jury should choose for this test case.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$) – the number of test cases.</p>





```input1
2
4 2

6

4

6 6

4
```




```output1
? 1

? 3

! 2

? 1

! 4
```



## Note

<p>In the first test case, the jury has chosen the array $a$ $=$ $[4, 2, 5, 1]$</p><p>In the second test case, the jury has chosen the array $a$ $=$ $[5, 7, 1, 3, 3, 7]$</p>
