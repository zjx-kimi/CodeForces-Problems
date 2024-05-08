## Description

<div><p>Mocha likes arrays, and Serval gave her an array consisting of positive integers as a gift.</p><p>Mocha thinks that for an array of positive integers $a$, it is <span class="tex-font-style-it">good</span> iff the <a href="https://en.wikipedia.org/wiki/Greatest_common_divisor">greatest common divisor</a> of all the elements in $a$ is no more than its length. And for an array of at least $2$ positive integers, it is <span class="tex-font-style-it">beautiful</span> iff all of its prefixes whose length is no less than $2$ are good. </p><p>For example:</p><ul> <li> $[3,6]$ is not good, because $\gcd(3,6)=3$ is greater than its length $2$. </li><li> $[1,2,4]$ is both good and beautiful, because all of its prefixes whose length is no less than $2$, which are $[1,2]$ and $[1,2,4]$, are both good. </li><li> $[3,6,1]$ is good but not beautiful, because $[3,6]$ is not good. </li></ul><p>Now Mocha gives you the gift array $a$ of $n$ positive integers, and she wants to know whether array $a$ could become beautiful by reordering the elements in $a$. It is allowed to keep the array $a$ unchanged.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1\leq t\leq 500$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2\leq n\leq 100$) — the length of array $a$.</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($1\leq a_1,a_2,\ldots,a_n\leq 10^6$) — the elements of array $a$.</p></div><div class="output-specification"><p>For each test case, print <span class="tex-font-style-tt">Yes</span> if it is possible to reorder the elements in $a$ to make it beautiful, and print <span class="tex-font-style-tt">No</span> if not.</p><p>You can output <span class="tex-font-style-tt">Yes</span> and <span class="tex-font-style-tt">No</span> in any case (for example, strings <span class="tex-font-style-tt">yEs</span>, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span> and <span class="tex-font-style-tt">YES</span> will be recognized as a positive response).</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1\leq t\leq 500$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2\leq n\leq 100$) — the length of array $a$.</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($1\leq a_1,a_2,\ldots,a_n\leq 10^6$) — the elements of array $a$.</p>

## Output

<p>For each test case, print <span class="tex-font-style-tt">Yes</span> if it is possible to reorder the elements in $a$ to make it beautiful, and print <span class="tex-font-style-tt">No</span> if not.</p><p>You can output <span class="tex-font-style-tt">Yes</span> and <span class="tex-font-style-tt">No</span> in any case (for example, strings <span class="tex-font-style-tt">yEs</span>, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span> and <span class="tex-font-style-tt">YES</span> will be recognized as a positive response).</p>





```input1|2,3,6,7,10,11
6
2
3 6
3
1 2 4
3
3 6 1
3
15 35 21
4
35 10 35 14
5
1261 227821 143 4171 1941
```




```output1
No
Yes
Yes
No
Yes
Yes
```



## Note

<p>In the first test case, neither $[3,6]$ nor $[6,3]$ are beautiful, so it's impossible to obtain a beautiful array by reordering the elements in $a$.</p><p>In the second test case, $[1,2,4]$ is already beautiful. Keeping the array $a$ unchanged can obtain a beautiful array.</p>
