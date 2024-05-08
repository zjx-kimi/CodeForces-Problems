## Description

<div><p>You are given $n$ points with integer coordinates $x_1,\dots x_n$, which lie on a number line.</p><p>For some integer $s$, we construct segments [$s,x_1$], [$s,x_2$], $\dots$, [$s,x_n$]. Note that if $x_i&lt;s$, then the segment will look like [$x_i,s$]. The segment [$a, b$] covers all integer points $a, a+1, a+2, \dots, b$.</p><p>We define the <span class="tex-font-style-it">power</span> of a point $p$ as the number of segments that intersect the point with coordinate $p$, denoted as $f_p$.</p><p>Your task is to compute $\sum\limits_{p=1}^{10^9}f_p$ for each $s \in \{x_1,\dots,x_n\}$, i.e., the sum of $f_p$ for all integer points from $1$ to $10^9$.</p><p>For example, if the initial coordinates are $[1,2,5,7,1]$ and we choose $s=5$, then the segments will be: $[1,5]$,$[2,5]$,$[5,5]$,$[5,7]$,$[1,5]$. And the powers of the points will be: $f_1=2, f_2=3, f_3=3, f_4=3, f_5=5, f_6=1, f_7=1, f_8=0, \dots, f_{10^9}=0$. Their sum is $2+3+3+3+5+1+1=18$.</p></div><div class="input-specification"><p>The first line contains an integer $t$ ($1\le t\le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains an integer $n$ ($1 \le n \le 2\cdot 10^5$)&nbsp;— the number of points.</p><p>The second line contains $n$ integers $x_1,x_2 \dots x_n$ ($1 \le x_i \le 10^9$)&nbsp;— the coordinates of the points.</p><p>It is guaranteed that the sum of the values of $n$ over all test cases does not exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output $n$ integers, where the $i$-th integer is equal to the sum of the powers of all points for $s=x_i$.</p></div>

## Input

<p>The first line contains an integer $t$ ($1\le t\le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains an integer $n$ ($1 \le n \le 2\cdot 10^5$)&nbsp;— the number of points.</p><p>The second line contains $n$ integers $x_1,x_2 \dots x_n$ ($1 \le x_i \le 10^9$)&nbsp;— the coordinates of the points.</p><p>It is guaranteed that the sum of the values of $n$ over all test cases does not exceed $2\cdot 10^5$.</p>

## Output

<p>For each test case, output $n$ integers, where the $i$-th integer is equal to the sum of the powers of all points for $s=x_i$.</p>





```input1|2,3,6,7
3
3
1 4 3
5
1 2 5 7 1
4
1 10 100 1000
```




```output1
8 7 6
16 15 18 24 16
1111 1093 1093 2893
```



## Note

<p>In the first test case we first choose $s=x_1=1$, then the following segments are formed: $[1,1]$,$[1,4]$,$[1,3]$. </p><p>The powers of the points will be as follows: $f_1=3, f_2=2, f_3=2, f_4=1, f_5=0 \dots$ The sum of powers of the points: $3+2+2+1+0+\dots+0=8$. </p><p>After that we choose $s=x_2=4$. Then there will be such segments: $[1,4]$,$[4,4]$,$[3,4]$, and powers of the points are $f_1=1, f_2=1, f_3=2, f_4=3$. </p><p>At the end we take $s=x_3=3$ and the segments look like this: $[1,3]$,$[3,4]$,$[3,3]$, the powers of the points are $f_1=1, f_2=1, f_3=3, f_4=1$.</p>
