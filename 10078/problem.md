## Description

<div><p>Rudolf has prepared a set of $n$ problems with complexities $a_1 &lt; a_2 &lt; a_3 &lt; \dots &lt; a_n$. He is not entirely satisfied with the balance, so he wants to add <span class="tex-font-style-bf">at most one</span> problem to fix it.</p><p>For this, Rudolf came up with $m$ models of problems and $k$ functions. The complexity of the $i$-th model is $d_i$, and the complexity of the $j$-th function is $f_j$. To create a problem, he selects values $i$ and $j$ ($1 \le i \le m$, $1 \le j \le k$) and by combining the $i$-th model with the $j$-th function, he obtains a new problem with complexity $d_i + f_j$ (a new element is inserted into the array $a$).</p><p>To determine the <span class="tex-font-style-it">imbalance</span> of the set, Rudolf sorts the complexities of the problems in ascending order and finds the largest value of $a_i - a_{i - 1}$ ($i &gt; 1$).</p><p>What is the minimum value of <span class="tex-font-style-it">imbalance</span> that Rudolf can achieve by adding at most one problem, created according to the described rules?</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The first line of each test case contains three integers $n$, $m$, and $k$ ($2 \le n \le 10^5$, $1 \le m, k \le 2 \cdot 10^5$)&nbsp;— the number of prepared problems, the number of models, and the number of functions, respectively.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, a_3, \dots a_n$ ($1 \le a_i \le 2 \cdot 10^9$, $a_i &lt; a_{i+1}$)&nbsp;— the complexities of the prepared problems.</p><p>The third line of each test case contains $m$ integers $d_1, d_2, d_3, \dots d_m$ ($1 \le d_i \le 10^9$)&nbsp;— the complexities of the models.</p><p>The fourth line of each test case contains $k$ integers $f_1, f_2, f_3, \dots f_k$ ($1 \le f_i \le 10^9$)&nbsp;— the complexities of the functions.</p><p>It is guaranteed that the sum of $n$ over all testcases does not exceed $10^5$.</p><p>It is guaranteed that the sum of $m$ over all testcases does not exceed $2 \cdot 10^5$.</p><p>It is guaranteed that the sum of $k$ over all testcases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each testcase, output a single number&nbsp;— the minimum <span class="tex-font-style-it">imbalance</span> that Rudolf can achieve.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The first line of each test case contains three integers $n$, $m$, and $k$ ($2 \le n \le 10^5$, $1 \le m, k \le 2 \cdot 10^5$)&nbsp;— the number of prepared problems, the number of models, and the number of functions, respectively.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, a_3, \dots a_n$ ($1 \le a_i \le 2 \cdot 10^9$, $a_i &lt; a_{i+1}$)&nbsp;— the complexities of the prepared problems.</p><p>The third line of each test case contains $m$ integers $d_1, d_2, d_3, \dots d_m$ ($1 \le d_i \le 10^9$)&nbsp;— the complexities of the models.</p><p>The fourth line of each test case contains $k$ integers $f_1, f_2, f_3, \dots f_k$ ($1 \le f_i \le 10^9$)&nbsp;— the complexities of the functions.</p><p>It is guaranteed that the sum of $n$ over all testcases does not exceed $10^5$.</p><p>It is guaranteed that the sum of $m$ over all testcases does not exceed $2 \cdot 10^5$.</p><p>It is guaranteed that the sum of $k$ over all testcases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each testcase, output a single number&nbsp;— the minimum <span class="tex-font-style-it">imbalance</span> that Rudolf can achieve.</p>





```input1|2,3,4,5,10,11,12,13,18,19,20,21,26,27,28,29
7
5 5 5
5 10 15 20 26
11 14 16 13 8
16 4 5 3 1
7 6 5
1 4 7 10 18 21 22
2 3 5 7 4 2
6 8 9 3 2
7 6 5
1 4 7 10 18 21 22
2 3 5 7 4 2
6 8 13 3 2
5 6 3
2 10 13 20 25
11 6 10 16 14 5
6 17 15
4 2 2
11 12 14 15
19 14
10 6
8 4 2
3 10 16 18 21 22 29 30
9 13 16 15
4 2
2 4 7
4 21
4 15 14 5
20 1 15 1 12 5 11
```




```output1
5
4
5
8
2
7
11
```


