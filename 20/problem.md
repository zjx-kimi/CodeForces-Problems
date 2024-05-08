## Description

<div><p>You are given an array $a_1, a_2, \dots, a_n$, where each element is an integer from $1$ to $x$.</p><p>You can perform the following operation with it any number of times:</p><ul> <li> choose three integers $l$, $r$ and $k$ such that $1 \le l \le r \le n$, $1 \le k \le x$ and <span class="tex-font-style-bf">each</span> element $a_i$ such that $l \le i \le r$ is different from $k$. Then, for each $i \in [l, r]$, replace $a_i$ with $k$. </li></ul><p>In other words, you choose a subsegment of the array and an integer from $1$ to $x$ which does not appear in that subsegment, and replace every element in the subsegment with that chosen integer.</p><p>Your goal is to make all elements in the array equal. What is the minimum number of operations that you have to perform?</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 100$) — the number of test cases.</p><p>Each test case consists of two lines:</p><ul> <li> the first line contains two integers $n$ and $x$ ($1 \le x \le n \le 100$); </li><li> the second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le x$). </li></ul><p>Additional constraint on the input: the sum of $n$ over all test cases does not exceed $500$.</p></div><div class="output-specification"><p>For each test case, print one integer — the minimum number of operations you have to perform.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 100$) — the number of test cases.</p><p>Each test case consists of two lines:</p><ul> <li> the first line contains two integers $n$ and $x$ ($1 \le x \le n \le 100$); </li><li> the second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le x$). </li></ul><p>Additional constraint on the input: the sum of $n$ over all test cases does not exceed $500$.</p>

## Output

<p>For each test case, print one integer — the minimum number of operations you have to perform.</p>





```input1|2,3,6,7
3
3 2
1 2 1
6 3
1 2 3 1 2 3
12 3
3 1 3 1 2 1 1 2 3 1 1 3
```




```output1
1
2
2
```


