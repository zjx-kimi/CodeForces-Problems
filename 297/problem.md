## Description

<div><p>Given a sequence of integers $a$ of length $n$.</p><p>A sequence is called <span class="tex-font-style-it">beautiful</span> if it has the form of a series of blocks, each starting with its length, i.e., first comes the length of the block, and then its elements. For example, the sequences [$\color{red}{3},\ \color{red}{3},\ \color{red}{4},\ \color{red}{5},\ \color{green}{2},\ \color{green}{6},\ \color{green}{1}$] and [$\color{red}{1},\ \color{red}{8},\ \color{green}{4},\ \color{green}{5},\ \color{green}{2},\ \color{green}{6},\ \color{green}{1}$] are <span class="tex-font-style-it">beautiful</span> (different blocks are colored differently), while [$1$], [$1,\ 4,\ 3$], [$3,\ 2,\ 1$] are not.</p><p>In one operation, you can remove any element from the sequence. What is the minimum number of operations required to make the given sequence <span class="tex-font-style-it">beautiful</span>?</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then follows the descriptions of the test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the sequence $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^6$)&nbsp;— the elements of the sequence $a$.</p><p>It is guaranteed that the sum of the values of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single number&nbsp;— the minimum number of deletions required to make the sequence $a$ <span class="tex-font-style-it">beautiful</span>.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then follows the descriptions of the test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the sequence $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^6$)&nbsp;— the elements of the sequence $a$.</p><p>It is guaranteed that the sum of the values of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output a single number&nbsp;— the minimum number of deletions required to make the sequence $a$ <span class="tex-font-style-it">beautiful</span>.</p>





```input1|2,3,6,7,10,11,14,15
7
7
3 3 4 5 2 6 1
4
5 6 3 2
6
3 4 1 6 7 7
3
1 4 3
5
1 2 3 4 5
5
1 2 3 1 2
5
4 5 5 1 5
```




```output1
0
4
1
1
2
1
0
```



## Note

<p>In the first test case of the example, the given sequence is already <span class="tex-font-style-it">beautiful</span>, as shown in the statement.</p><p>In the second test case of the example, the sequence can only be made beautiful by removing all elements from it.</p><p>In the fifth test case of the example, the sequence can be made beautiful by removing the first and last elements. Then the sequence will become [$2,\ 3,\ 4$].</p>
