## Description

<div><p>You are given a string consisting of characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span>. You have to paint every character of this string into one of two colors, red or blue.</p><p>If you paint the $i$-th character red, you get $r_i$ coins. If you paint it blue, you get $b_i$ coins.</p><p>After coloring the string, you remove every <span class="tex-font-style-bf">blue</span> character from it, and count the number of inversions in the resulting string (i. e. the number of pairs of characters such that the left character in the pair is <span class="tex-font-style-tt">1</span>, and the right character in the pair is <span class="tex-font-style-tt">0</span>). For each inversion, you have to pay $1$ coin.</p><p>What is the maximum number of coins you can earn?</p></div><div class="input-specification"><p>The first line of the input contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of four lines:</p><ul> <li> the first line contains one integer $n$ ($1 \le n \le 4 \cdot 10^5$) — the length of the string; </li><li> the second line contains $s$ — a string of $n$ characters, where each character is either <span class="tex-font-style-tt">0</span> or <span class="tex-font-style-tt">1</span>; </li><li> the third line contains $n$ integers $r_1, r_2, \dots, r_n$ ($1 \le r_i \le 10^{12}$); </li><li> the fourth line contains $n$ integers $b_1, b_2, \dots, b_n$ ($1 \le b_i \le 10^{12}$). </li></ul><p>Additional constraint on the input: the sum of values of $n$ over all test cases does not exceed $4 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print one integer — the maximum number of coins you can earn.</p></div>

## Input

<p>The first line of the input contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of four lines:</p><ul> <li> the first line contains one integer $n$ ($1 \le n \le 4 \cdot 10^5$) — the length of the string; </li><li> the second line contains $s$ — a string of $n$ characters, where each character is either <span class="tex-font-style-tt">0</span> or <span class="tex-font-style-tt">1</span>; </li><li> the third line contains $n$ integers $r_1, r_2, \dots, r_n$ ($1 \le r_i \le 10^{12}$); </li><li> the fourth line contains $n$ integers $b_1, b_2, \dots, b_n$ ($1 \le b_i \le 10^{12}$). </li></ul><p>Additional constraint on the input: the sum of values of $n$ over all test cases does not exceed $4 \cdot 10^5$.</p>

## Output

<p>For each test case, print one integer — the maximum number of coins you can earn.</p>





```input1|2,3,4,5,10,11,12,13
4
7
0100010
6 6 6 7 7 6 6
3 3 5 4 7 6 7
5
10111
9 8 5 7 5
4 4 7 8 4
10
0100000000
7 7 6 5 2 2 5 3 8 3
8 6 9 6 6 8 9 7 7 9
8
01010000
8 7 7 7 8 7 7 8
4 4 4 2 1 4 4 4
```




```output1
43
36
76
52
```



## Note

<p>Explanations for the test cases for the example (blue characters are underlined, red ones are not):</p><ol> <li> $0100\underline{0}1\underline{0}$; </li><li> $10\underline{11}1$; </li><li> $\underline{0}1\underline{00000000}$; </li><li> $0\underline{1}010000$. </li></ol>
