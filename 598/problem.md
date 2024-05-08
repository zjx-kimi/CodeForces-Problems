## Description

<div><p>A <span class="tex-font-style-it">substring</span> is a continuous and non-empty segment of letters from a given string, without any reorders.</p><p>An <span class="tex-font-style-it">even palindrome</span> is a string that reads the same backward as forward and has an even length. For example, strings "<span class="tex-font-style-tt">zz</span>", "<span class="tex-font-style-tt">abba</span>", "<span class="tex-font-style-tt">abccba</span>" are even palindromes, but strings "<span class="tex-font-style-tt">codeforces</span>", "<span class="tex-font-style-tt">reality</span>", "<span class="tex-font-style-tt">aba</span>", "<span class="tex-font-style-tt">c</span>" are not.</p><p>A <span class="tex-font-style-it">beautiful string</span> is an even palindrome or a string that can be partitioned into some smaller even palindromes.</p><p>You are given a string $s$, consisting of $n$ lowercase Latin letters. Count the number of <span class="tex-font-style-bf">beautiful substrings</span> of $s$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 5\cdot 10^5$).</p><p>The second line of each test case contains a string $s$. String $s$ consists of only lowercase Latin letters and has a length of $n$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case print the number of beautiful substrings.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 5\cdot 10^5$).</p><p>The second line of each test case contains a string $s$. String $s$ consists of only lowercase Latin letters and has a length of $n$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5\cdot 10^5$.</p>

## Output

<p>For each test case print the number of beautiful substrings.</p>





```input1|2,3,6,7,10,11
6
6
abaaba
1
a
2
aa
6
abcdef
12
accabccbacca
6
abbaaa
```




```output1
3
0
1
0
14
6
```



## Note

<p>In the first test case, the beautiful substrings are "<span class="tex-font-style-tt">abaaba</span>", "<span class="tex-font-style-tt">baab</span>", "<span class="tex-font-style-tt">aa</span>".</p><p>In the last test case, the beautiful substrings are "<span class="tex-font-style-tt">aa</span>" (counted twice), "<span class="tex-font-style-tt">abba</span>", "<span class="tex-font-style-tt">bb</span>", "<span class="tex-font-style-tt">bbaa</span>", "<span class="tex-font-style-tt">abbaaa</span>".</p>
