## Description

<div><p><span class="tex-font-style-it">This is an interactive problem.</span></p><p>There is a hidden permutation $p_1, p_2, \dots, p_n$. </p><p>Consider an undirected graph with $n$ nodes only with no edges. You can make two types of queries:</p><ol> <li> Specify an integer $x$ satisfying $2 \le x \le 2n$. For all integers $i$ ($1 \le i \le n$) such that $1 \le x-i \le n$, an edge between node $i$ and node $x-i$ will be added. </li><li> Query the number of <span class="tex-font-style-bf">edges</span> in the shortest path between node $p_i$ and node $p_j$. As the answer to this question you will get the number of edges in the shortest path if such a path exists, or $-1$ if there is no such path. </li></ol><p>Note that you can make both types of queries in <span class="tex-font-style-bf">any</span> order.</p><p>Within $2n$ queries (including type $1$ and type $2$), guess two possible permutations, at least one of which is $p_1, p_2, \dots, p_n$. You get accepted if at least one of the permutations is correct. You are allowed to guess the same permutation twice.</p><p>A permutation of length $n$ is an array consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation ($2$ appears twice in the array), and $[1,3,4]$ is also not a permutation ($n=3$ but there is $4$ in the array).</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 100$) — the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 10^3$) — the length of the permutation.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^3$.</p></div><div><h2>Interaction</h2><p>The interaction for each test case begins by reading the integer $n$.</p><p>Then, make at most $2n$ queries: </p><ul> <li> If you want to make a type $1$ query, output "<span class="tex-font-style-tt">+ x</span>". $x$ must be an integer between $2$ and $2n$ inclusive. <span class="tex-font-style-bf">After doing that read $1$ or $-2$</span>. If you read $1$ your query was valid, otherwise it was invalid or you exceed the limit of queries, and your program must terminate immediately to receive a <span class="tex-font-style-tt">Wrong Answer</span> verdict. </li><li> If you want to make a type $2$ query, output "<span class="tex-font-style-tt">? i j</span>". $i$ and $j$ must be integers between $1$ and $n$ inclusive. After that, read in a single integer $r$ ($-1 \le r \le n$) — the answer to your query. If you receive the integer $−2$ instead of an answer, it means your program has made an invalid query, or has exceeded the limit of queries. Your program must terminate immediately to receive a <span class="tex-font-style-tt">Wrong Answer</span> verdict. </li></ul><p>At any point of the interaction, if you want to guess two permutations, output "<span class="tex-font-style-tt">!</span> $p_{1,1}$ $p_{1,2}$ $\dots$ $p_{1,n}$ $p_{2,1}$ $p_{2,2}$ $\dots$ $p_{2,n}$". Note that you should output the two permutations <span class="tex-font-style-bf">on the same line</span>, and <span class="tex-font-style-bf">no exclamation mark</span> is needed to separate the two permutations. <span class="tex-font-style-bf">After doing that read $1$ or $-2$</span>. If you read $1$ your answer was correct, otherwise it was incorrect and your program must terminate immediately to receive a <span class="tex-font-style-tt">Wrong Answer</span> verdict. After that, move on to the next test case, or terminate the program if there are none. Note that reporting the answer <span class="tex-font-style-bf">does not count</span> as a query.</p><p>Note that even if you output a correct permutation, the second permutation should be a permutation and <span class="tex-font-style-bf">not an arbitrary array</span>.</p><p>At any point, if you continue interaction after reading in the integer $-2$, you can get an arbitrary verdict because your solution will continue to read from a closed stream.</p><p>After printing a query or the answer do not forget to output the end of line and flush the output. Otherwise, you will get <span class="tex-font-style-tt">Idleness limit exceeded</span>. To do this, use:</p><ul><li> <span class="tex-font-style-tt">fflush(stdout)</span> or <span class="tex-font-style-tt">cout.flush()</span> in C++;</li><li> <span class="tex-font-style-tt">System.out.flush()</span> in Java;</li><li> <span class="tex-font-style-tt">flush(output)</span> in Pascal;</li><li> <span class="tex-font-style-tt">stdout.flush()</span> in Python;</li><li> see the documentation for other languages.</li></ul><p>Interactor is <span class="tex-font-style-bf">non-adaptive</span>. This means that all permutations are fixed before the interaction starts.</p><p><span class="tex-font-style-bf">Hacks</span></p><p>To make a hack, use the following format.</p><p>The first line should contain a single integer $t$ ($1 \le t \le 100$) — the number of test cases.</p><p>The first line of each test case should contain a single integer $n$ ($2 \le n \le 10^3$) — the length of the permutation.</p><p>The second line of each test case should contain $n$ distinct integers $p_1, p_2, \ldots, p_n$ ($1 \le p_i \le n$) — the hidden permutation.</p><p>The sum of $n$ over all test cases should not exceed $10^3$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 100$) — the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 10^3$) — the length of the permutation.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^3$.</p>





```input1
2
6

1

1

1

1

1

2

-1

1
2

1
```




```output1
+ 12

+ 2

+ 3

? 1 3

+ 5

? 1 5

? 4 5

! 1 4 2 5 3 6 1 2 3 4 5 6


! 1 2 2 1
```



## Note

<p>In the first test case, $n=6$ and the hidden permutation $p = [1,4,2,5,3,6]$.</p><p>Firstly, make a type $1$ query on $x=12, 2, 3$ respectively. This adds four edges to the graph in total: </p><ul> <li> An edge that connects node $6$ and node $6$. </li><li> An edge that connects node $1$ and node $1$. </li><li> An edge that connects node $1$ and node $2$. </li><li> An edge that connects node $2$ and node $1$. </li></ul><p>Since all of these queries are valid, the interactor returns $1$ after each of them.</p><p>Then, query the number of edges in the shortest path between node $p_1 = 1$ and $p_3 = 2$, which is equal to $1$.</p><p>Then, make a type $1$ query on $x=5$. This adds four edges to the graph in total: </p><ul> <li> An edge that connects node $1$ and node $4$. </li><li> An edge that connects node $2$ and node $3$. </li><li> An edge that connects node $3$ and node $2$. </li><li> An edge that connects node $4$ and node $1$. </li></ul><p>Since this query is valid, the interactor returns $1$.</p><p>Then, query the number of edges in the shortest path between node $p_1 = 1$ and $p_5 = 3$, which is equal to $2$.</p><p>Then, query the number of edges in the shortest path between node $p_4 = 5$ and $p_5 = 3$. Such a path doesn't exist, therefore the interactor returns $-1$.</p><p>Afterwards, due to some magic, two possible permutations that can be $p$ are determined: the first permutation is $[1,4,2,5,3,6]$ and the second permutation is $[1,2,3,4,5,6]$. Since the first permutation is equal to the hidden permutation, this test case is solved correctly. In total, $7$ queries are used, which is within the limit of $2 \cdot 6 = 12$ queries.</p><p>Since the answer is correct, the interactor returns $1$.</p><p>In the second test case, $n=2$ and the hidden permutation is $p = [2,1]$.</p><p>Since there are only $2! = 2$ possible permutations, no queries are needed. It is sufficient to just output the two permutations, $[1,2]$ and $[2,1]$. In total, $0$ queries are used, which is within the limit of $2 \cdot 2 = 4$ queries.</p><p>Since the answer is correct, the interactor returns $1$.</p>
