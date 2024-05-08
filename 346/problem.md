## Description

<div><p>You are given two integers $l \le r$. You need to find <span class="tex-font-style-bf">positive</span> integers $a$ and $b$ such that the following conditions are simultaneously satisfied:</p><ul><li> $l \le a + b \le r$</li><li> $\gcd(a, b) \neq 1$</li></ul><p>or report that they do not exist.</p><p>$\gcd(a, b)$ denotes the <a href="https://en.wikipedia.org/wiki/Greatest_common_divisor">greatest common divisor</a> of numbers $a$ and $b$. For example, $\gcd(6, 9) = 3$, $\gcd(8, 9) = 1$, $\gcd(4, 2) = 2$.</p></div><div class="input-specification"><p>The first line of the input contains an integer $t$ ($1 \le t \le 500$)&nbsp;— the number of test cases.</p><p>Then the descriptions of the test cases follow.</p><p>The only line of the description of each test case contains $2$ integers $l, r$ ($1 \le l \le r \le 10^7$).</p></div><div class="output-specification"><p>For each test case, output the integers $a, b$ that satisfy all the conditions on a separate line. If there is no answer, instead output a single number $-1$.</p><p>If there are multiple answers, you can output any of them.</p></div>

## Input

<p>The first line of the input contains an integer $t$ ($1 \le t \le 500$)&nbsp;— the number of test cases.</p><p>Then the descriptions of the test cases follow.</p><p>The only line of the description of each test case contains $2$ integers $l, r$ ($1 \le l \le r \le 10^7$).</p>

## Output

<p>For each test case, output the integers $a, b$ that satisfy all the conditions on a separate line. If there is no answer, instead output a single number $-1$.</p><p>If there are multiple answers, you can output any of them.</p>





```input1|2,4,6,8,10,12
11
11 15
1 3
18 19
41 43
777 777
8000000 10000000
2000 2023
1791791 1791791
1 4
2 3
9840769 9840769
```




```output1
6 9
-1
14 4
36 6
111 666
4000000 5000000 
2009 7
-1
2 2
-1
6274 9834495
```



## Note

<p>In the first test case, $11 \le 6 + 9 \le 15$, $\gcd(6, 9) = 3$, and all conditions are satisfied. Note that this is not the only possible answer, for example, $\{4, 10\}, \{5, 10\}, \{6, 6\}$ are also valid answers for this test case.</p><p>In the second test case, the only pairs $\{a, b\}$ that satisfy the condition $1 \le a + b \le 3$ are $\{1, 1\}, \{1, 2\}, \{2, 1\}$, but in each of these pairs $\gcd(a, b)$ equals $1$, so there is no answer.</p><p>In the third sample test, $\gcd(14, 4) = 2$.</p>
