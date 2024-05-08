## Description

<div><p>The FB-string is formed as follows. Initially, it is empty. We go through all positive integers, starting from $1$, in ascending order, and do the following for each integer:</p><ul> <li> if the current integer is divisible by $3$, append <span class="tex-font-style-tt">F</span> to the end of the FB-string; </li><li> if the current integer is divisible by $5$, append <span class="tex-font-style-tt">B</span> to the end of the FB-string. </li></ul><p>Note that if an integer is divisible by both $3$ and $5$, we append <span class="tex-font-style-tt">F</span>, and then <span class="tex-font-style-tt">B</span>, not in the opposite order.</p><p>The first $10$ characters of the FB-string are <span class="tex-font-style-tt">FBFFBFFBFB</span>: the first <span class="tex-font-style-tt">F</span> comes from the integer $3$, the next character (<span class="tex-font-style-tt">B</span>) comes from $5$, the next <span class="tex-font-style-tt">F</span> comes from the integer $6$, and so on. It's easy to see that this string is infinitely long. Let $f_i$ be the $i$-th character of FB-string; so, $f_1$ is <span class="tex-font-style-tt">F</span>, $f_2$ is <span class="tex-font-style-tt">B</span>, $f_3$ is <span class="tex-font-style-tt">F</span>, $f_4$ is <span class="tex-font-style-tt">F</span>, and so on.</p><p>You are given a string $s$, consisting of characters <span class="tex-font-style-tt">F</span> and/or <span class="tex-font-style-tt">B</span>. You have to determine whether it is a substring (contiguous subsequence) of the FB-string. In other words, determine if it is possible to choose two integers $l$ and $r$ ($1 \le l \le r$) so that the string $f_l f_{l+1} f_{l+2} \dots f_r$ is exactly $s$.</p><p>For example:</p><ul> <li> <span class="tex-font-style-tt">FFB</span> is a substring of the FB-string: if we pick $l = 3$ and $r = 5$, the string $f_3 f_4 f_5$ is exactly <span class="tex-font-style-tt">FFB</span>; </li><li> <span class="tex-font-style-tt">BFFBFFBF</span> is a substring of the FB-string: if we pick $l = 2$ and $r = 9$, the string $f_2 f_3 f_4 \dots f_9$ is exactly <span class="tex-font-style-tt">BFFBFFBF</span>; </li><li> <span class="tex-font-style-tt">BBB</span> is not a substring of the FB-string. </li></ul></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 2046$) — the number of test cases.</p><p>Each test case consists of two lines. The first line contains one integer $k$ ($1 \le k \le 10$) — the number of characters in $s$. The second line contains $s$, which is a string of exactly $k$ characters. Each character of $s$ is either <span class="tex-font-style-tt">F</span> or <span class="tex-font-style-tt">B</span>.</p></div><div class="output-specification"><p>For each test case, print <span class="tex-font-style-tt">YES</span> if $s$ is a substring of the FB-string, or <span class="tex-font-style-tt">NO</span> otherwise.</p><p>You may print each letter in any case (<span class="tex-font-style-tt">YES</span>, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span> will all be recognized as positive answer, <span class="tex-font-style-tt">NO</span>, <span class="tex-font-style-tt">no</span> and <span class="tex-font-style-tt">nO</span> will all be recognized as negative answer).</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 2046$) — the number of test cases.</p><p>Each test case consists of two lines. The first line contains one integer $k$ ($1 \le k \le 10$) — the number of characters in $s$. The second line contains $s$, which is a string of exactly $k$ characters. Each character of $s$ is either <span class="tex-font-style-tt">F</span> or <span class="tex-font-style-tt">B</span>.</p>

## Output

<p>For each test case, print <span class="tex-font-style-tt">YES</span> if $s$ is a substring of the FB-string, or <span class="tex-font-style-tt">NO</span> otherwise.</p><p>You may print each letter in any case (<span class="tex-font-style-tt">YES</span>, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span> will all be recognized as positive answer, <span class="tex-font-style-tt">NO</span>, <span class="tex-font-style-tt">no</span> and <span class="tex-font-style-tt">nO</span> will all be recognized as negative answer).</p>





```input1|2,3,6,7
3
3
FFB
8
BFFBFFBF
3
BBB
```




```output1
YES
YES
NO
```


