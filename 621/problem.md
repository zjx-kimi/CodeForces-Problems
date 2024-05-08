## Description

<div><p><span class="tex-font-style-bf">This is the hard version of the problem. The only difference is that in this version, $a_i \le 10^9$.</span></p><p>For a given sequence of $n$ integers $a$, a triple $(i, j, k)$ is called <span class="tex-font-style-it">magic</span> if: </p><ul> <li> $1 \le i, j, k \le n$. </li><li> $i$, $j$, $k$ are pairwise distinct. </li><li> there exists a positive integer $b$ such that $a_i \cdot b = a_j$ and $a_j \cdot b = a_k$. </li></ul><p>Kolya received a sequence of integers $a$ as a gift and now wants to count the number of <span class="tex-font-style-it">magic</span> triples for it. Help him with this task!</p><p>Note that there are no constraints on the order of integers $i$, $j$ and $k$.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of the test case contains a single integer $n$ ($3 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the sequence.</p><p>The second line of the test contains $n$ integers $a_1, a_2, a_3, \dots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the elements of the sequence $a$.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the number of <span class="tex-font-style-it">magic</span> triples for the sequence $a$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of the test case contains a single integer $n$ ($3 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the sequence.</p><p>The second line of the test contains $n$ integers $a_1, a_2, a_3, \dots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the elements of the sequence $a$.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the number of <span class="tex-font-style-it">magic</span> triples for the sequence $a$.</p>





```input1|2,3,6,7,10,11,14,15
7
5
1 7 7 2 7
3
6 2 18
9
1 2 3 4 5 6 7 8 9
4
1000 993 986 179
7
1 10 100 1000 10000 100000 1000000
8
1 1 2 2 4 4 8 8
9
1 1 1 2 2 2 4 4 4
```




```output1
6
1
3
0
9
16
45
```



## Note

<p>In the first example, there are $6$ <span class="tex-font-style-it">magic</span> triples for the sequence $a$&nbsp;— $(2, 3, 5)$, $(2, 5, 3)$, $(3, 2, 5)$, $(3, 5, 2)$, $(5, 2, 3)$, $(5, 3, 2)$.</p><p>In the second example, there is a single <span class="tex-font-style-it">magic</span> triple for the sequence $a$&nbsp;— $(2, 1, 3)$.</p>
