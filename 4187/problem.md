## Description

<div><p>Carl has $n$ coins of various colors, and he would like to sort them into piles. The coins are labeled $1,2,\ldots,n$, and each coin is exactly one of red, green, or blue. He would like to sort the coins into three different piles so one pile contains all red coins, one pile contains all green coins, and one pile contains all blue coins.</p><p>Unfortunately, Carl is colorblind, so this task is impossible for him. Luckily, he has a friend who can take a pair of coins and tell Carl if they are the same color or not. Using his friend, Carl believes he can now sort the coins. The order of the piles doesn't matter, as long as all same colored coins are in the one pile, and no two different colored coins are in the same pile.</p><p>His friend will answer questions about multiple pairs of coins in batches, and will answer about all of those pairs in parallel. Each coin should be in at most one pair in each batch. The same coin can appear in different batches.</p><p>Carl can use only $7$ batches. Help him find the piles of coins after sorting.</p></div><div><h2>Interaction</h2><p>You will be given multiple test cases. The first line contains an integer $t$ $(1 \leq t \leq 5$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains one integer $n$ ($1 \leq n \leq 10^5$)&nbsp;— the number of coins. If you read in a value of $-1$ here, that means that you printed an invalid answer in the previous case and exit immediately to avoid getting other verdicts.</p><p>To ask a question, print "<span class="tex-font-style-tt">Q</span> $k\ x_1\ y_1\ \ldots\ x_k\ y_k$" ($1 \leq k \leq n/2, 1 \leq x_i,y_i \leq n, x_i \neq y_i$). $k$ denotes the number of pairs in the batch, and $x_i, y_i$ denote the $i$-th pair of coins in the batch. A coin can only appear at most once in a batch. All $x_i$ and $y_i$ should be distinct.</p><p>The judge will respond with a bitstring of length $k$, where the $i$-th character is "<span class="tex-font-style-tt">1</span>" if $x_i$ and $y_i$ are the same color, and "<span class="tex-font-style-tt">0</span>" otherwise. The judge will respond with $-1$ if you ever ask an invalid query. Make sure to exit immediately to avoid getting other verdicts.</p><p>When you are ready to answer, print four lines.</p><p>The first line contains "<span class="tex-font-style-tt">A</span> $k_1\ k_2\ k_3$" ($0 \leq k_1,k_2,k_3$ and $k_1+k_2+k_3 = n$). These denote the sizes of the three piles.</p><p>The next line has $k_1$ integers, the labels of the coins in the first pile.</p><p>The next line has $k_2$ integers, the labels of the coins in the second pile.</p><p>The next line has $k_3$ integers, the labels coins in the third pile.</p><p>Each coin must appear in exactly one pile.</p><p>You may only ask at most $7$ batches per test case.</p><p>After printing a query and the answer do not forget to output end of line and flush the output. Otherwise, you will get <span class="tex-font-style-tt">Idleness limit exceeded</span>. To do this, use:</p><ul><li> <span class="tex-font-style-tt">fflush(stdout)</span> or <span class="tex-font-style-tt">cout.flush()</span> in C++;</li><li> <span class="tex-font-style-tt">System.out.flush()</span> in Java;</li><li> <span class="tex-font-style-tt">flush(output)</span> in Pascal;</li><li> <span class="tex-font-style-tt">stdout.flush()</span> in Python;</li><li> see documentation for other languages.</li></ul><p><span class="tex-font-style-bf">Hack Format</span></p><p>To hack, use the following format. Note that you can only hack with one test case.</p><p>The first line should contain a single integer $t$ ($t=1$).</p><p>The second line should contain a single string $s$ consisting of only the characters "<span class="tex-font-style-tt">R</span>", "<span class="tex-font-style-tt">G</span>", "<span class="tex-font-style-tt">B</span>" ($1 \leq |s| \leq 10^5$). The $i$-th character in this string represents the color of the $i$-th coin.</p></div>





```input1
3
3
1
1
1
3
1
0
0
6
000
010
100
001
000
```




```output1
Q 1 1 2
Q 1 2 3
Q 1 1 3
A 3 0 0
1 2 3


Q 1 1 3
Q 1 2 3
Q 1 1 2
A 2 0 1
1 3

2
Q 3 1 2 3 4 5 6
Q 3 1 3 2 5 4 6
Q 3 1 4 2 6 3 5
Q 3 1 5 2 4 3 6
Q 3 1 6 2 3 4 5
A 2 2 2
1 4
2 5
3 6
```



## Note

<p>In the example, there are three test cases.</p><p>In the first test case, there are three coins. We ask about the pairs $(1,2)$, $(2,3)$, and $(1,3)$ in different batches and get that they are all the same color. Thus, we know all the coins are the same color, so we can put them all in one pile. Note that some piles can be empty and those are denoted with an empty line.</p><p>In the second test case, there are three coins again. This time, we only get that $(1,3)$ are the same and $(1,2)$ and $(2,3)$ are different. So, one possible scenario is that coins $1$ and $3$ are red and coin $2$ is green.</p><p>In the last case, there are $6$ coins. The case shows how to ask and receive answers for multiple pairs in one batch.</p>
