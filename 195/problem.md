## Description

<div><p>Yarik is a big fan of many kinds of music. But Yarik loves not only listening to music but also writing it. He likes electronic music most of all, so he has created his own system of music notes, which, in his opinion, is best for it.</p><p>Since Yarik also likes informatics, in his system notes are denoted by integers of $2^k$, where $k \ge 1$&nbsp;— a positive integer. But, as you know, you can't use just notes to write music, so Yarik uses combinations of two notes. The combination of two notes $(a, b)$, where $a = 2^k$ and $b = 2^l$, he denotes by the integer $a^b$.</p><p>For example, if $a = 8 = 2^3$, $b = 4 = 2^2$, then the combination $(a, b)$ is denoted by the integer $a^b = 8^4 = 4096$. Note that different combinations can have the same notation, e.g., the combination $(64, 2)$ is also denoted by the integer $4096 = 64^2$.</p><p>Yarik has already chosen $n$ notes that he wants to use in his new melody. However, since their integers can be very large, he has written them down as an array $a$ of length $n$, then the note $i$ is $b_i = 2^{a_i}$. The integers in array $a$ can be repeated.</p><p>The melody will consist of several combinations of two notes. Yarik was wondering how many pairs of notes $b_i, b_j$ $(i &lt; j)$ exist such that the combination $(b_i, b_j)$ is equal to the combination $(b_j, b_i)$. In other words, he wants to count the number of pairs $(i, j)$ $(i &lt; j)$ such that $b_i^{b_j} = b_j^{b_i}$. Help him find the number of such pairs.</p></div><div class="input-specification"><p>The first line of the input contains one integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains one integer $n$ ($1 \leq n \leq 2 \cdot 10^5$)&nbsp;— the length of the arrays.</p><p>The next line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \leq a_i \leq 10^9$)&nbsp;— array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output the number of pairs that satisfy the given condition.</p></div>

## Input

<p>The first line of the input contains one integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains one integer $n$ ($1 \leq n \leq 2 \cdot 10^5$)&nbsp;— the length of the arrays.</p><p>The next line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \leq a_i \leq 10^9$)&nbsp;— array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output the number of pairs that satisfy the given condition.</p>





```input1|2,3,6,7,10,11
5
1
2
4
3 1 3 2
2
1000 1000
3
1 1 1
19
2 4 1 6 2 8 5 4 2 10 5 10 8 7 4 3 2 6 10
```




```output1
0
2
1
3
19
```


