## Description

<div><p>Monocarp had an array $a$ consisting of $n$ integers. He has decided to choose two integers $l$ and $r$ such that $1 \le l \le r \le n$, and then sort the subarray $a[l..r]$ (the subarray $a[l..r]$ is the part of the array $a$ containing the elements $a_l, a_{l+1}, a_{l+2}, \dots, a_{r-1}, a_r$) in <span class="tex-font-style-bf">non-descending order</span>. After sorting the subarray, Monocarp has obtained a new array, which we denote as $a'$.</p><p>For example, if $a = [6, 7, 3, 4, 4, 6, 5]$, and Monocarp has chosen $l = 2, r = 5$, then $a' = [6, 3, 4, 4, 7, 6, 5]$.</p><p>You are given the arrays $a$ and $a'$. Find the integers $l$ and $r$ that Monocarp could have chosen. If there are multiple pairs of values $(l, r)$, find the one which <span class="tex-font-style-bf">corresponds to the longest subarray</span>.</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of three lines:</p><ul> <li> the first line contains one integer $n$ ($2 \le n \le 2 \cdot 10^5$); </li><li> the second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le n$); </li><li> the third line contains $n$ integers $a'_1, a'_2, \dots, a'_n$ ($1 \le a'_i \le n$). </li></ul><p>Additional constraints on the input:</p><ul> <li> the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$; </li><li> it is possible to obtain the array $a'$ by sorting one subarray of $a$; </li><li> $a' \ne a$ (there exists at least one position in which these two arrays are different). </li></ul></div><div class="output-specification"><p>For each test case, print two integers — the values of $l$ and $r$ ($1 \le l \le r \le n$). If there are multiple answers, print the values that correspond to the <span class="tex-font-style-bf">longest subarray</span>. If there are still multiple answers, print any of them.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of three lines:</p><ul> <li> the first line contains one integer $n$ ($2 \le n \le 2 \cdot 10^5$); </li><li> the second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le n$); </li><li> the third line contains $n$ integers $a'_1, a'_2, \dots, a'_n$ ($1 \le a'_i \le n$). </li></ul><p>Additional constraints on the input:</p><ul> <li> the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$; </li><li> it is possible to obtain the array $a'$ by sorting one subarray of $a$; </li><li> $a' \ne a$ (there exists at least one position in which these two arrays are different). </li></ul>

## Output

<p>For each test case, print two integers — the values of $l$ and $r$ ($1 \le l \le r \le n$). If there are multiple answers, print the values that correspond to the <span class="tex-font-style-bf">longest subarray</span>. If there are still multiple answers, print any of them.</p>





```input1|2,3,4,8,9,10
3
7
6 7 3 4 4 6 5
6 3 4 4 7 6 5
3
1 2 1
1 1 2
3
2 2 1
2 1 2
```




```output1
2 5
1 3
2 3
```


