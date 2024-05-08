## Description

<div><p><span class="tex-font-style-it">No, not "random" numbers.</span></p><p>Ranom digits are denoted by uppercase Latin letters from <span class="tex-font-style-tt">A</span> to <span class="tex-font-style-tt">E</span>. Moreover, the value of the letter <span class="tex-font-style-tt">A</span> is $1$, <span class="tex-font-style-tt">B</span> is $10$, <span class="tex-font-style-tt">C</span> is $100$, <span class="tex-font-style-tt">D</span> is $1000$, <span class="tex-font-style-tt">E</span> is $10000$.</p><p>A Ranom number is a sequence of Ranom digits. The value of the Ranom number is calculated as follows: the values of all digits are summed up, but some digits are taken with negative signs: a digit is taken with negative sign if there is a digit with a <span class="tex-font-style-bf">strictly greater</span> value to the right of it (not necessarily immediately after it); otherwise, that digit is taken with a positive sign.</p><p>For example, the value of the Ranom number <span class="tex-font-style-tt">DAAABDCA</span> is $1000 - 1 - 1 - 1 - 10 + 1000 + 100 + 1 = 2088$.</p><p>You are given a Ranom number. You can change no more than one digit in it. Calculate the maximum possible value of the resulting number.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains a string $s$ ($1 \le |s| \le 2 \cdot 10^5$) consisting of uppercase Latin letters from <span class="tex-font-style-tt">A</span> to <span class="tex-font-style-tt">E</span> — the Ranom number you are given.</p><p>The sum of the string lengths over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print a single integer&nbsp;— the maximum possible value of the number, if you can change no more than one digit in it.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains a string $s$ ($1 \le |s| \le 2 \cdot 10^5$) consisting of uppercase Latin letters from <span class="tex-font-style-tt">A</span> to <span class="tex-font-style-tt">E</span> — the Ranom number you are given.</p><p>The sum of the string lengths over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, print a single integer&nbsp;— the maximum possible value of the number, if you can change no more than one digit in it.</p>





```input1|2,4
4
DAAABDCA
AB
ABCDEEDCBA
DDDDAAADDABECD
```




```output1
11088
10010
31000
15886
```



## Note

<p>In the first example, you can get <span class="tex-font-style-tt">EAAABDCA</span> with the value $10000-1-1-1-10+1000+100+1=11088$.</p><p>In the second example, you can get <span class="tex-font-style-tt">EB</span> with the value $10000+10=10010$.</p>
