## Description

<div><p>Monocarp has $n$ numbers $1, 2, \dots, n$ and a set (initially empty). He adds his numbers to this set $n$ times in some order. During each step, he adds a new number (which has not been present in the set before). In other words, the sequence of added numbers is a permutation of length $n$.</p><p>Every time Monocarp adds an element into the set <span class="tex-font-style-bf">except for the first time</span>, he writes out a character:</p><ul> <li> if the element Monocarp is trying to insert becomes the maximum element in the set, Monocarp writes out the character <span class="tex-font-style-tt">&gt;</span>; </li><li> if the element Monocarp is trying to insert becomes the minimum element in the set, Monocarp writes out the character <span class="tex-font-style-tt">&lt;</span>; </li><li> if none of the above, Monocarp writes out the character <span class="tex-font-style-tt">?</span>. </li></ul><p>You are given a string $s$ of $n-1$ characters, which represents the characters written out by Monocarp (in the order he wrote them out). You have to process $m$ queries to the string. Each query has the following format:</p><ul> <li> $i$ $c$ — replace $s_i$ with the character $c$. </li></ul><p>Both before processing the queries and after each query, you have to calculate the number of different ways to order the integers $1, 2, 3, \dots, n$ such that, if Monocarp inserts the integers into the set in that order, he gets the string $s$. Since the answers might be large, print them modulo $998244353$.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $m$ ($2 \le n \le 3 \cdot 10^5$; $1 \le m \le 3 \cdot 10^5$).</p><p>The second line contains the string $s$, consisting of exactly $n-1$ characters <span class="tex-font-style-tt">&lt;</span>, <span class="tex-font-style-tt">&gt;</span> and/or <span class="tex-font-style-tt">?</span>.</p><p>Then $m$ lines follow. Each of them represents a query. Each line contains an integer $i$ and a character $c$ ($1 \le i \le n-1$; $c$ is either <span class="tex-font-style-tt">&lt;</span>, <span class="tex-font-style-tt">&gt;</span>, or <span class="tex-font-style-tt">?</span>).</p></div><div class="output-specification"><p>Both before processing the queries and after each query, print one integer — the number of ways to order the integers $1, 2, 3, \dots, n$ such that, if Monocarp inserts the integers into the set in that order, he gets the string $s$. Since the answers might be large, print them modulo $998244353$.</p></div>

## Input

<p>The first line contains two integers $n$ and $m$ ($2 \le n \le 3 \cdot 10^5$; $1 \le m \le 3 \cdot 10^5$).</p><p>The second line contains the string $s$, consisting of exactly $n-1$ characters <span class="tex-font-style-tt">&lt;</span>, <span class="tex-font-style-tt">&gt;</span> and/or <span class="tex-font-style-tt">?</span>.</p><p>Then $m$ lines follow. Each of them represents a query. Each line contains an integer $i$ and a character $c$ ($1 \le i \le n-1$; $c$ is either <span class="tex-font-style-tt">&lt;</span>, <span class="tex-font-style-tt">&gt;</span>, or <span class="tex-font-style-tt">?</span>).</p>

## Output

<p>Both before processing the queries and after each query, print one integer — the number of ways to order the integers $1, 2, 3, \dots, n$ such that, if Monocarp inserts the integers into the set in that order, he gets the string $s$. Since the answers might be large, print them modulo $998244353$.</p>





```input1
6 4
&lt;?&gt;?&gt;
1 ?
4 &lt;
5 &lt;
1 &gt;
```




```input2
2 2
&gt;
1 ?
1 &lt;
```




```output1
3
0
0
0
1
```




```output2
1
0
1
```



## Note

<p>In the first example, there are three possible orderings before all queries: </p><ul> <li> $3, 1, 2, 5, 4, 6$; </li><li> $4, 1, 2, 5, 3, 6$; </li><li> $4, 1, 3, 5, 2, 6$. </li></ul><p>After the last query, there is only one possible ordering: </p><ul> <li> $3, 5, 4, 6, 2, 1$. </li></ul>
