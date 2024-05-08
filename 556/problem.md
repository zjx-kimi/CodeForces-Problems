## Description

<div><p>Famous worldwide astrophysicist Mleil waGrasse Tysok recently read about the existence of <span class="tex-font-style-it">twin galaxy clusters</span>. Before he shares this knowledge with the broader audience in his podcast called <span class="tex-font-style-it">S.tarT-ok</span>, he wants to prove their presence on his own. Mleil is aware that the vastness of the universe is astounding (almost as astounding as his observation skills) and decides to try his luck and find some new pair of twin clusters.</p><p>To do so, he used his TLEscope to observe a part of the night sky that was not yet examined by humanity in which there are exactly $2^{k + 1}$ galaxies in a row. $i$-th of them consist of exactly $0 \le g_i &lt; 4^k$ stars.</p><p>A galaxy cluster is any non-empty contiguous segment of galaxies. Moreover, its' <span class="tex-font-style-it">trait</span> is said to be equal to the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#XOR">bitwise XOR</a> of all values $g_i$ within this range.</p><p>Two galaxy clusters are considered twins if and only if they have the same traits and their corresponding segments are <span class="tex-font-style-bf">disjoint</span>.</p><p>Write a program that, for many scenarios, will read a description of a night sky part observed by Mleil and outputs a location of two intervals belonging to some twin clusters pair, or a single value $-1$ if no such pair exists.</p></div><div class="input-specification"><p>The first line contains a single integer $t$, denoting the number of test cases that the program has to handle. The following lines contain test case descriptions, each containing exactly two lines.</p><p>The first of them contains a single integer $k$ ($0 \le k \le 17$).</p><p>The second line contains $2^{k + 1}$ integers $g_1, g_2, \ldots, g_{2^{k+1}}$ ($0 \le g_i &lt; 4^k$).</p><p>We guarantee that the sum of values $2^{k + 1}$ over all test cases does not exceed $2^{18}$.</p></div><div class="output-specification"><p>Answers for all test cases should be present in separate lines. If there exist a pair of twin galaxies, then output four integers $a$, $b$, $c$, and $d$ denoting their inclusive ranges $[a, b]$ and $[c, d]$ (the first interval does not need to start before the second one, but they have to be disjoint). If no pair of such galaxies exist, output a single value $-1$ instead.</p></div>

## Input

<p>The first line contains a single integer $t$, denoting the number of test cases that the program has to handle. The following lines contain test case descriptions, each containing exactly two lines.</p><p>The first of them contains a single integer $k$ ($0 \le k \le 17$).</p><p>The second line contains $2^{k + 1}$ integers $g_1, g_2, \ldots, g_{2^{k+1}}$ ($0 \le g_i &lt; 4^k$).</p><p>We guarantee that the sum of values $2^{k + 1}$ over all test cases does not exceed $2^{18}$.</p>

## Output

<p>Answers for all test cases should be present in separate lines. If there exist a pair of twin galaxies, then output four integers $a$, $b$, $c$, and $d$ denoting their inclusive ranges $[a, b]$ and $[c, d]$ (the first interval does not need to start before the second one, but they have to be disjoint). If no pair of such galaxies exist, output a single value $-1$ instead.</p>





```input1|2,3,6,7
4
2
4 15 0 7 11 8 3 2
1
0 1 2 3
0
0 0
3
15 63 57 39 61 25 42 61 50 41 27 41 56 23 17 27
```




```output1
2 4 6 6
2 2 3 4
1 1 2 2
1 1 4 10
```



## Note

<p>In the first test case we pick intervals $[2, 4]$ and $[6, 6]$ as our twin clusters. The trait of the first interval equals $15 \oplus 0 \oplus 7 = 8$, and the trait of the second interval equals $8$, so these galaxy clusters are indeed twins.</p>
