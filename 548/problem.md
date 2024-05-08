## Description

<div><p>You are given a string $s$ consisting of the characters <span class="tex-font-style-tt">0</span>, <span class="tex-font-style-tt">1</span> and/or <span class="tex-font-style-tt">?</span>. Let's call it a <span class="tex-font-style-it">pattern</span>.</p><p>Let's say that the binary string (a string where each character is either <span class="tex-font-style-tt">0</span> or <span class="tex-font-style-tt">1</span>) <span class="tex-font-style-it">matches</span> the <span class="tex-font-style-it">pattern</span> if you can replace each character <span class="tex-font-style-tt">?</span> with <span class="tex-font-style-tt">0</span> or <span class="tex-font-style-tt">1</span> (for each character, the choice is independent) so that the strings become equal. For example, <span class="tex-font-style-tt">0010</span> matches <span class="tex-font-style-tt">?01?</span>, but <span class="tex-font-style-tt">010</span> doesn't match <span class="tex-font-style-tt">1??</span>, <span class="tex-font-style-tt">??</span>, or <span class="tex-font-style-tt">????</span>.</p><p>Let's define the <span class="tex-font-style-it">cost</span> of the binary string as the minimum number of operations of the form "reverse an arbitrary contiguous substring of the string" required to sort the string in non-descending order.</p><p>You have to find a binary string with the minimum possible cost among those that match the given pattern. If there are multiple answers, print any of them.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 3 \cdot 10^4$)&nbsp;— the number of test cases.</p><p>The first and only line of each test case contains the string $s$ ($1 \le |s| \le 3 \cdot 10^5$) consisting of characters <span class="tex-font-style-tt">0</span>, <span class="tex-font-style-tt">1</span>, and/or <span class="tex-font-style-tt">?</span>.</p><p>The sum of the string lengths over all test cases does not exceed $3 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print a binary string with the minimum possible cost among those that match the given pattern. If there are multiple answers, print any of them.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 3 \cdot 10^4$)&nbsp;— the number of test cases.</p><p>The first and only line of each test case contains the string $s$ ($1 \le |s| \le 3 \cdot 10^5$) consisting of characters <span class="tex-font-style-tt">0</span>, <span class="tex-font-style-tt">1</span>, and/or <span class="tex-font-style-tt">?</span>.</p><p>The sum of the string lengths over all test cases does not exceed $3 \cdot 10^5$.</p>

## Output

<p>For each test case, print a binary string with the minimum possible cost among those that match the given pattern. If there are multiple answers, print any of them.</p>





```input1|2,4
4
??01?
10100
1??10?
0?1?10?10
```




```output1
00011
10100
111101
011110010
```



## Note

<p>In the first test case of the example, the cost of the resulting string is $0$.</p><p>In the second test case, the cost of the resulting string is $2$: we can reverse the substring from the $1$-st character to the $5$-th character, and we obtain the string <span class="tex-font-style-tt">00101</span>. Then we reverse the substring from the $3$-rd to the $4$-th character, and we obtain the string <span class="tex-font-style-tt">00011</span>, which is sorted in non-descending order.</p>
