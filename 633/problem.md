## Description

<div><p>An <span class="tex-font-style-it">integer template</span> is a string consisting of digits and/or question marks.</p><p>A positive (strictly greater than $0$) integer matches the integer template if it is possible to replace every question mark in the template with a digit in such a way that we get the decimal representation of that integer <span class="tex-font-style-bf">without any leading zeroes</span>.</p><p>For example:</p><ul> <li> $42$ matches <span class="tex-font-style-tt">4?</span>; </li><li> $1337$ matches <span class="tex-font-style-tt">????</span>; </li><li> $1337$ matches <span class="tex-font-style-tt">1?3?</span>; </li><li> $1337$ matches <span class="tex-font-style-tt">1337</span>; </li><li> $3$ does not match <span class="tex-font-style-tt">??</span>; </li><li> $8$ does not match <span class="tex-font-style-tt">???8</span>; </li><li> $1337$ does not match <span class="tex-font-style-tt">1?7</span>. </li></ul><p>You are given an integer template consisting of <span class="tex-font-style-bf">at most $5$ characters</span>. Calculate the number of positive (strictly greater than $0$) integers that match it.</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 2 \cdot 10^4$) — the number of test cases.</p><p>Each test case consists of one line containing the string $s$ ($1 \le |s| \le 5$) consisting of digits and/or question marks — the integer template for the corresponding test case.</p></div><div class="output-specification"><p>For each test case, print one integer — the number of positive (strictly greater than $0$) integers that match the template.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 2 \cdot 10^4$) — the number of test cases.</p><p>Each test case consists of one line containing the string $s$ ($1 \le |s| \le 5$) consisting of digits and/or question marks — the integer template for the corresponding test case.</p>

## Output

<p>For each test case, print one integer — the number of positive (strictly greater than $0$) integers that match the template.</p>





```input1|2,4,6,8
8
??
?
0
9
03
1??7
?5?
9??99
```




```output1
90
9
0
1
0
100
90
100
```


