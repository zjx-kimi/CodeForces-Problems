## Description

<div><p><span class="tex-font-style-it">Iva and Pav are a famous Serbian competitive programming couple. In Serbia, they call Pav "papuca" and that's why he will make all of Iva's wishes come true.</span></p><p>Iva gave Pav an array $a$ of $n$ elements.</p><p>Let's define $f(l, r) = a_l \ \&amp; \ a_{l+1} \ \&amp; \dots \&amp; \ a_r$ (here $\&amp;$ denotes the <a href="http://tiny.cc/bitwise_and">bitwise AND operation</a>). </p><p><span class="tex-font-style-bf">Note that</span> $f(l, r)$ <span class="tex-font-style-bf">is not defined when</span> $l&gt;r$.</p><p>Iva also gave Pav $q$ queries.</p><p>Each query consists of 2 numbers, $k$ and $l$, and she wants Pav to find the largest index $r$ ($l \le r \le n$), such that $f(l, r) \ge k$. </p><p>Pav wants to solve this problem fast because he doesn't want to upset Iva. He needs your help.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the elements of array $a$.</p><p>The third line of each test case contains a single integer $q$ ($1 \le q \le 10^5$) — the number of queries Iva gave Pav.</p><p>The next $q$ lines of each test case contains two numbers, $l$ and $k$ ($1 \le l \le n$, $1 \le k \le 10^9$)&nbsp;— the left bound for the subsegment, and the integer $k$ described in statement.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$. Also, it is guaranteed that the sum of $q$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each query output maximal index $r$ ($l \le r \le n$) such that $a_l \ \&amp; \ a_{l+1} \ \&amp; \dots \&amp; \ a_r \ \ge \ k$.</p><p>If such $r$ doesn't exist, output $-1$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the elements of array $a$.</p><p>The third line of each test case contains a single integer $q$ ($1 \le q \le 10^5$) — the number of queries Iva gave Pav.</p><p>The next $q$ lines of each test case contains two numbers, $l$ and $k$ ($1 \le l \le n$, $1 \le k \le 10^9$)&nbsp;— the left bound for the subsegment, and the integer $k$ described in statement.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$. Also, it is guaranteed that the sum of $q$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each query output maximal index $r$ ($l \le r \le n$) such that $a_l \ \&amp; \ a_{l+1} \ \&amp; \dots \&amp; \ a_r \ \ge \ k$.</p><p>If such $r$ doesn't exist, output $-1$.</p>





```input1|2,3,4,5,6,7,15,16,17,18,19,20,21
3
5
15 14 17 42 34
3
1 7
2 15
4 5
5
7 5 3 1 7
4
1 7
5 7
2 3
2 2
7
19 20 15 12 21 7 11
4
1 15
4 4
7 12
5 7
```




```output1
2 -1 5 
1 5 2 2 
2 6 -1 5
```



## Note

<p>In the <span class="tex-font-style-bf">first test case</span> $n=5$, and the array $a = [15, 14, 17, 42, 34]$</p><p>The first query asks for the biggest index $r$ such that the $f(1, r) \ge 7$.</p><p>$f(1,1) = 15, \ f(1, 2) = 14, \ f(1,3)=0 \ f(1, 4)=0 \ f(1, 5)=0$, so $r=2$ is the answer.</p><p>The second query asks for $f(2, r) \ge 15$. Since such $r$ doesn't exist, the answer is $-1$.</p><p>The third query asks for $f(4, r) \ge 5$. $f(4, 4) = 42, \ f(4, 5) = 34$, so $r=5$ is the answer.</p><p>In the <span class="tex-font-style-bf">second test case</span> $n=5$, and the array $a= [7, 5, 3, 1, 7]$.</p><p>For the first query, $f(1, r) \ge 7$.</p><p>$f(1, 1)=7, \ f(1, 2)=5, \ f(1, 3) = 1, \ f(1,4) = 1, \ f(1, 5)=1$, so the answer to this query is $1$.</p><p>For the second query, $f(5, r) \ge 7$.</p><p>$f(5, 5) = 7$, so the answer is $5$.</p><p>For the third query, $f(2, r) \ge 3$.</p><p>$f(2, 2) = 5, \ f(2, 3) = 1, \ f(2, 4) = 1, \ f(2, 5) = 1$, so the answer is $2$.</p>
