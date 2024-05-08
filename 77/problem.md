## Description

<div><p>The mathematicians of the 31st lyceum were given the following task:</p><p>You are given an <span class="tex-font-style-bf">odd</span> number $n$, and you need to find $n$ different numbers that are squares of integers. But it's not that simple. Each number should have a length of $n$ (and should not have leading zeros), and the multiset of digits of all the numbers should be the same. For example, for $\mathtt{234}$ and $\mathtt{432}$, and $\mathtt{11223}$ and $\mathtt{32211}$, the multisets of digits are the same, but for $\mathtt{123}$ and $\mathtt{112233}$, they are not.</p><p>The mathematicians couldn't solve this problem. Can you?</p></div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \leq t \leq 100$)&nbsp;— the number of test cases.</p><p>The following $t$ lines contain one <span class="tex-font-style-bf">odd</span> integer $n$ ($1 \leq n \leq 99$)&nbsp;— the number of numbers to be found and their length.</p><p>It is guaranteed that the solution exists within the given constraints.</p><p>It is guaranteed that the sum of $n^2$ does not exceed $10^5$.</p><p>The numbers can be output in any order.</p></div><div class="output-specification"><p>For each test case, you need to output $n$ numbers of length $n$&nbsp;— the answer to the problem.</p><p>If there are several answers, print any of them.</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \leq t \leq 100$)&nbsp;— the number of test cases.</p><p>The following $t$ lines contain one <span class="tex-font-style-bf">odd</span> integer $n$ ($1 \leq n \leq 99$)&nbsp;— the number of numbers to be found and their length.</p><p>It is guaranteed that the solution exists within the given constraints.</p><p>It is guaranteed that the sum of $n^2$ does not exceed $10^5$.</p><p>The numbers can be output in any order.</p>

## Output

<p>For each test case, you need to output $n$ numbers of length $n$&nbsp;— the answer to the problem.</p><p>If there are several answers, print any of them.</p>





```input1|2,4
3
1
3
5
```




```output1
1
169
196
961
16384
31684
36481
38416
43681
```



## Note

<p>Below are the squares of the numbers that are the answers for the second test case:</p><p>$\mathtt{169}$ = $\mathtt{13}^2$</p><p>$\mathtt{196}$ = $\mathtt{14}^2$</p><p>$\mathtt{961}$ = $\mathtt{31}^2$</p><p>Below are the squares of the numbers that are the answers for the third test case:</p><p>$\mathtt{16384}$ = $\mathtt{128}^2$</p><p>$\mathtt{31684}$ = $\mathtt{178}^2$</p><p>$\mathtt{36481}$ = $\mathtt{191}^2$</p><p>$\mathtt{38416}$ = $\mathtt{196}^2$</p><p>$\mathtt{43681}$ = $\mathtt{209}^2$</p>
