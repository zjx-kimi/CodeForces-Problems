## Description

<div><p>Dmitry has a string $s$, consisting of lowercase Latin letters.</p><p>Dmitry decided to remove two <span class="tex-font-style-bf">consecutive</span> characters from the string $s$ and you are wondering how many different strings can be obtained after such an operation.</p><p>For example, Dmitry has a string "<span class="tex-font-style-tt">aaabcc</span>". You can get the following different strings: "<span class="tex-font-style-tt">abcc</span>"(by deleting the first two or second and third characters), "<span class="tex-font-style-tt">aacc</span>"(by deleting the third and fourth characters),"<span class="tex-font-style-tt">aaac</span>"(by deleting the fourth and the fifth character) and "<span class="tex-font-style-tt">aaab</span>" (by deleting the last two).</p></div><div class="input-specification"><p>The first line of input data contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— number of test cases. </p><p>The descriptions of the test cases follow.</p><p>The first line of the description of each test case contains an integer $n$ ($3 \le n \le 2 \cdot 10^5$).</p><p>The second line of the description of each test case contains a string $s$ of length $n$ consisting of lowercase Latin letters.</p><p>It is guaranteed that the sum of $n$ for all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case print one integer — the number of distinct strings that can be obtained by removing two consecutive letters.</p></div>

## Input

<p>The first line of input data contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— number of test cases. </p><p>The descriptions of the test cases follow.</p><p>The first line of the description of each test case contains an integer $n$ ($3 \le n \le 2 \cdot 10^5$).</p><p>The second line of the description of each test case contains a string $s$ of length $n$ consisting of lowercase Latin letters.</p><p>It is guaranteed that the sum of $n$ for all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case print one integer — the number of distinct strings that can be obtained by removing two consecutive letters.</p>





```input1|2,3,6,7,10,11,14,15
7
6
aaabcc
10
aaaaaaaaaa
6
abcdef
7
abacaba
6
cccfff
4
abba
5
ababa
```




```output1
4
1
5
3
3
3
1
```



## Note

<p>The first example is explained in the statement.</p><p>In the third example, the following strings are obtained: "<span class="tex-font-style-tt">cdef</span>", "<span class="tex-font-style-tt">adef</span>", "<span class="tex-font-style-tt">abef</span>", "<span class="tex-font-style-tt">abcf</span>", "<span class="tex-font-style-tt">abcd</span>".</p><p>In the seventh example, any deletion will result in the string "<span class="tex-font-style-tt">aba</span>".</p>
