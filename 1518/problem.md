## Description

<div><p>You are given a sequence of $n$ integers $a_1, a_2, \dots, a_n$. You are also given $x$ integers $1, 2, \dots, x$.</p><p>You are asked to insert each of the extra integers into the sequence $a$. Each integer can be inserted at the beginning of the sequence, at the end of the sequence, or between any elements of the sequence.</p><p>The score of the resulting sequence $a'$ is the sum of absolute differences of adjacent elements in it $\left(\sum \limits_{i=1}^{n+x-1} |a'_i - a'_{i+1}|\right)$.</p><p>What is the smallest possible score of the resulting sequence $a'$?</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains two integers $n$ and $x$ ($1 \le n, x \le 2 \cdot 10^5$)&nbsp;— the length of the sequence and the number of extra integers.</p><p>The second line of each testcase contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 2 \cdot 10^5$).</p><p>The sum of $n$ over all testcases doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each testcase, print a single integer&nbsp;— the smallest sum of absolute differences of adjacent elements of the sequence after you insert the extra integers into it.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains two integers $n$ and $x$ ($1 \le n, x \le 2 \cdot 10^5$)&nbsp;— the length of the sequence and the number of extra integers.</p><p>The second line of each testcase contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 2 \cdot 10^5$).</p><p>The sum of $n$ over all testcases doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>For each testcase, print a single integer&nbsp;— the smallest sum of absolute differences of adjacent elements of the sequence after you insert the extra integers into it.</p>





```input1
4
1 5
10
3 8
7 2 10
10 2
6 1 5 7 3 3 9 10 10 1
4 10
1 3 1 2
```




```output1
9
15
31
13
```



## Note

<p>Here are the sequences with the smallest scores for the example. The underlined elements are the extra integers. Note that there exist other sequences with this smallest score. </p><ul> <li> $\underline{1}, \underline{2}, \underline{3}, \underline{4}, \underline{5}, 10$ </li><li> $\underline{7}, 7, \underline{6}, \underline{4}, 2, \underline{2}, \underline{1}, \underline{3}, \underline{5}, \underline{8}, 10$ </li><li> $6, \underline{1}, 1, \underline{2}, 5, 7, 3, 3, 9, 10, 10, 1$ </li><li> $1, 3, \underline{1}, 1, 2, \underline{2}, \underline{3}, \underline{4}, \underline{5}, \underline{6}, \underline{7}, \underline{8}, \underline{9}, \underline{10}$ </li></ul>
