## Description

<div><p>Alice's potion making professor gave the following assignment to his students: brew a potion using $n$ ingredients, such that the proportion of ingredient $i$ in the final potion is $r_i &gt; 0$ (and $r_1 + r_2 + \cdots + r_n = 1$).</p><p>He forgot the recipe, and now all he remembers is a set of $n-1$ facts of the form, "ingredients $i$ and $j$ should have a ratio of $x$ to $y$" (i.e., if $a_i$ and $a_j$ are the amounts of ingredient $i$ and $j$ in the potion respectively, then it must hold $a_i/a_j = x/y$), where $x$ and $y$ are positive integers. However, it is guaranteed that the set of facts he remembers is sufficient to uniquely determine the original values $r_i$.</p><p>He decided that he will allow the students to pass the class as long as they submit a potion which satisfies all of the $n-1$ requirements (there may be many such satisfactory potions), and contains a positive integer amount of each ingredient.</p><p>Find the minimum total amount of ingredients needed to make a potion which passes the class. As the result can be very large, you should print the answer modulo $998\,244\,353$.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 2 \cdot 10^5$).</p><p>Each of the next $n-1$ lines contains four integers $i, j, x, y$ ($1 \le i, j \le n$, $i\not=j$, $1\le x, y \le n$) — ingredients $i$ and $j$ should have a ratio of $x$ to $y$. It is guaranteed that the set of facts is sufficient to uniquely determine the original values $r_i$.</p><p>It is also guaranteed that the sum of $n$ for all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print the minimum total amount of ingredients needed to make a potion which passes the class, modulo $998\,244\,353$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 2 \cdot 10^5$).</p><p>Each of the next $n-1$ lines contains four integers $i, j, x, y$ ($1 \le i, j \le n$, $i\not=j$, $1\le x, y \le n$) — ingredients $i$ and $j$ should have a ratio of $x$ to $y$. It is guaranteed that the set of facts is sufficient to uniquely determine the original values $r_i$.</p><p>It is also guaranteed that the sum of $n$ for all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, print the minimum total amount of ingredients needed to make a potion which passes the class, modulo $998\,244\,353$.</p>





```input1|2,3,4,5,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30
3
4
3 2 3 4
1 2 4 3
1 4 2 4
8
5 4 2 3
6 4 5 4
1 3 5 2
6 8 2 1
3 5 3 4
3 2 2 5
6 7 4 3
17
8 7 4 16
9 17 4 5
5 14 13 12
11 1 17 14
6 13 8 9
2 11 3 11
4 17 7 2
17 16 8 6
15 5 1 14
16 7 1 10
12 17 13 10
11 16 7 2
10 11 6 4
13 17 14 6
3 11 15 8
15 6 12 8
```




```output1
69
359
573672453
```



## Note

<p>In the first test case, the minimum total amount of ingredients is $69$. In fact, the amounts of ingredients $1, 2, 3, 4$ of a valid potion are $16, 12, 9, 32$, respectively. The potion is valid because </p><ul> <li> Ingredients $3$ and $2$ have a ratio of $9 : 12 = 3 : 4$; </li><li> Ingredients $1$ and $2$ have a ratio of $16 : 12 = 4 : 3$; </li><li> Ingredients $1$ and $4$ have a ratio of $16 : 32 = 2 : 4$. </li></ul><p>In the second test case, the amounts of ingredients $1, 2, 3, 4, 5, 6, 7, 8$ in the potion that minimizes the total amount of ingredients are $60, 60, 24, 48, 32, 60, 45, 30$.</p>
