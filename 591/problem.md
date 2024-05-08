## Description

<div><p>You are given a binary array $a$ of $n$ elements, a binary array is an array consisting only of $0$s and $1$s. </p><p>A blank space is a segment of <span class="tex-font-style-bf">consecutive</span> elements consisting of only $0$s. </p><p>Your task is to find the length of the longest blank space.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 100$)&nbsp;— the length of the array.</p><p>The second line of each test case contains $n$ space-separated integers $a_i$ ($0 \leq a_i \leq 1$)&nbsp;— the elements of the array.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the length of the longest blank space.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 100$)&nbsp;— the length of the array.</p><p>The second line of each test case contains $n$ space-separated integers $a_i$ ($0 \leq a_i \leq 1$)&nbsp;— the elements of the array.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the length of the longest blank space.</p>





```input1|2,3,6,7,10,11
5
5
1 0 0 1 0
4
0 1 1 1
1
0
3
1 1 1
9
1 0 0 0 1 0 0 0 1
```




```output1
2
1
1
0
3
```


