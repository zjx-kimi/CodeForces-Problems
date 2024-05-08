## Description

<div><p>You are given $2n$ tuples of values $(a, b, c)$, where $a$ and $b$ are positive integers and $c$ is a bracket '<span class="tex-font-style-tt">(</span>' or '<span class="tex-font-style-tt">)</span>'. Exactly $n$ tuples have $c = $'<span class="tex-font-style-tt">(</span>' and the other $n$ tuples have $c =$ '<span class="tex-font-style-tt">)</span>'.</p><p>You are asked to choose two positive values $x$ and $y$ ($x &gt; 0$ and $y &gt; 0$; <span class="tex-font-style-bf">not necessarily integers</span>) and sort the tuples in the increasing value of $a \cdot x + b \cdot y$. If several tuples have the same value, you can place them in any order among themselves.</p><p>Is it possible to choose such $x$ and $y$ that taking brackets $c$ from the tuples in the resulting order produces a regular bracket sequence?</p><p><span class="tex-font-style-it">A regular bracket sequence is a bracket sequence that can be transformed into a correct arithmetic expression by inserting characters "<span class="tex-font-style-tt">1</span>" and "<span class="tex-font-style-tt">+</span>" between the original characters of the sequence.</span></p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 1500$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a single integer $n$ ($1 \le n \le 1500$).</p><p>The $i$-th of the next $2n$ lines contains two integers $a_i$ and $b_i$ ($1 \le a_i, b_i \le 10^6$) and a character $c_i$ ($c_i = $'<span class="tex-font-style-tt">(</span>' or $c_i = $'<span class="tex-font-style-tt">)</span>'). Exactly $n$ tuples have $c_i = $'<span class="tex-font-style-tt">(</span>' and the other $n$ tuples have $c_i =$ '<span class="tex-font-style-tt">)</span>'.</p><p>The sum of $n$ over all testcases doesn't exceed $1500$.</p></div><div class="output-specification"><p>For each testcase, print "<span class="tex-font-style-tt">YES</span>" if it's possible to choose such $x$ and $y$ that taking brackets $c$ from the tuples in the resulting order produces a regular bracket sequence. Otherwise, print "<span class="tex-font-style-tt">NO</span>".</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 1500$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a single integer $n$ ($1 \le n \le 1500$).</p><p>The $i$-th of the next $2n$ lines contains two integers $a_i$ and $b_i$ ($1 \le a_i, b_i \le 10^6$) and a character $c_i$ ($c_i = $'<span class="tex-font-style-tt">(</span>' or $c_i = $'<span class="tex-font-style-tt">)</span>'). Exactly $n$ tuples have $c_i = $'<span class="tex-font-style-tt">(</span>' and the other $n$ tuples have $c_i =$ '<span class="tex-font-style-tt">)</span>'.</p><p>The sum of $n$ over all testcases doesn't exceed $1500$.</p>

## Output

<p>For each testcase, print "<span class="tex-font-style-tt">YES</span>" if it's possible to choose such $x$ and $y$ that taking brackets $c$ from the tuples in the resulting order produces a regular bracket sequence. Otherwise, print "<span class="tex-font-style-tt">NO</span>".</p>





```input1|2,3,4,8,9,10,11,12,13,14,15,16
4
1
1 4 (
2 3 )
1
1 2 )
3 4 (
4
16 5 (
12 3 (
19 6 )
4 10 )
3 10 )
19 11 (
19 7 )
7 14 (
4
16 8 (
11 9 )
20 10 )
20 19 )
2 13 (
18 7 (
15 19 )
5 6 (
```




```output1
YES
NO
NO
YES
```



## Note

<p>In the first testcase, you can choose $x = 10, y = 0.1$. The values for tuples will be $10 \cdot 1 + 0.1 \cdot 4 = 10.4$ and $10 \cdot 2 + 0.1 \cdot 3 = 20.3$. Thus, the first tuple will go first, then the second one, making the bracket sequence "<span class="tex-font-style-tt">()</span>", which is regular.</p><p>In the second testcase, you can't choose positive $x$ and $y$ such that the opening brackets gets assigned a value less or equal to the value of the closing bracket.</p><p>In the fourth testcase, you can choose $x = 0.6, y = 0.55$. The bracket sequence is "<span class="tex-font-style-tt">(()(()))</span>".</p>
