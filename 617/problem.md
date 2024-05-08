## Description

<div><p>A <span class="tex-font-style-it">palindrome</span> is a string that reads the same backwards as forwards. For example, the string <span class="tex-font-style-tt">abcba</span> is palindrome, while the string <span class="tex-font-style-tt">abca</span> is not.</p><p>Let $p(t)$ be the number of <span class="tex-font-style-it">unique palindromic substrings</span> of string $t$, i.&nbsp;e. the number of substrings $t[l \dots r]$ that are palindromes themselves. Even if some substring occurs in $t$ several times, it's counted exactly once. (The whole string $t$ is also counted as a substring of $t$).</p><p>For example, string $t$ $=$ <span class="tex-font-style-tt">abcbbcabcb</span> has $p(t) = 6$ unique palindromic substrings: <span class="tex-font-style-tt">a</span>, <span class="tex-font-style-tt">b</span>, <span class="tex-font-style-tt">c</span>, <span class="tex-font-style-tt">bb</span>, <span class="tex-font-style-tt">bcb</span> and <span class="tex-font-style-tt">cbbc</span>.</p><p>Now, let's define $p(s, m) = p(t)$ where $t = s[1 \dots m]$. In other words, $p(s, m)$ is the number of palindromic substrings in the prefix of $s$ of length $m$. For example, $p($<span class="tex-font-style-tt">abcbbcabcb</span>$, 5)$ $=$ $p($<span class="tex-font-style-tt">abcbb</span>$) = 5$.</p><p>You are given an integer $n$ and $k$ "conditions" ($k \le 20$). Let's say that string $s$, consisting of $n$ lowercase Latin letters, is <span class="tex-font-style-bf">good</span> if all $k$ conditions are satisfied <span class="tex-font-style-bf">at the same time</span>. A condition is a pair $(x_i, c_i)$ and have the following meaning: </p><ul> <li> $p(s, x_i) = c_i$, i.&nbsp;e. a prefix of $s$ of length $x_i$ contains exactly $c_i$ unique palindromic substrings. </li></ul> Find a good string $s$ or report that such $s$ doesn't exist.<p>Look in Notes if you need further clarifications.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($3 \le n \le 2 \cdot 10^5$; $1 \le k \le 20$)&nbsp;— length of good string $s$ and number of conditions.</p><p>The second line of each test case contains $k$ integers $x_1, x_2, \dots, x_k$ ($3 \le x_1 &lt; x_2 &lt; \dots &lt; x_k = n$) where $x_i$ is the length of the prefix in the $i$-th condition.</p><p>The third line of each test case contains $k$ integers $c_1, c_2, \dots, c_k$ ($3 \le c_1 \le c_2 \le \dots \le c_k \le \min{\left(10^9, \frac{(n + 1) n}{2} \right)}$) where $c_i$ is the number of palindromic substrings in the $i$-th condition.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10 ^ 5$.</p></div><div class="output-specification"><p>For each test case, if there is no good string $s$ of length $n$ that satisfies all conditions, print <span class="tex-font-style-tt">NO</span>.</p><p>Otherwise, print <span class="tex-font-style-tt">YES</span> and a string $s$ of length $n$, consisting of lowercase Latin letters, that satisfies all conditions. If there are multiple answers, print any of them.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($3 \le n \le 2 \cdot 10^5$; $1 \le k \le 20$)&nbsp;— length of good string $s$ and number of conditions.</p><p>The second line of each test case contains $k$ integers $x_1, x_2, \dots, x_k$ ($3 \le x_1 &lt; x_2 &lt; \dots &lt; x_k = n$) where $x_i$ is the length of the prefix in the $i$-th condition.</p><p>The third line of each test case contains $k$ integers $c_1, c_2, \dots, c_k$ ($3 \le c_1 \le c_2 \le \dots \le c_k \le \min{\left(10^9, \frac{(n + 1) n}{2} \right)}$) where $c_i$ is the number of palindromic substrings in the $i$-th condition.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10 ^ 5$.</p>

## Output

<p>For each test case, if there is no good string $s$ of length $n$ that satisfies all conditions, print <span class="tex-font-style-tt">NO</span>.</p><p>Otherwise, print <span class="tex-font-style-tt">YES</span> and a string $s$ of length $n$, consisting of lowercase Latin letters, that satisfies all conditions. If there are multiple answers, print any of them.</p>





```input1|2,3,4,8,9,10,14,15,16,20,21,22
7
10 2
5 10
5 6
3 1
3
3
4 2
3 4
3 3
4 2
3 4
3 4
4 1
4
5
10 3
4 6 10
4 5 8
10 4
4 6 7 10
4 5 7 8
```




```output1
YES
abcbbcabcb
YES
foo
YES
ayda
YES
wada
NO
YES
abcbcacbab
NO
```



## Note

<p>In the first test case, string $s$ $=$ <span class="tex-font-style-tt">abcbbcabcb</span> satisfies $k = 2$ conditions: </p><ul> <li> $p(s, x_1) = p(s, 5) =$ $p($<span class="tex-font-style-tt">abcbb</span>$) = 5 = s_1$. Palindromic substrings are <span class="tex-font-style-tt">a</span>, <span class="tex-font-style-tt">b</span>, <span class="tex-font-style-tt">c</span>, <span class="tex-font-style-tt">bb</span> and <span class="tex-font-style-tt">bcb</span>. </li><li> $p(s, x_2) = p(s, 10) =$ $p($<span class="tex-font-style-tt">abcbbcabcb</span>$) = 6 = s_2$. Palindromic substrings are the same as above, and one extra substring <span class="tex-font-style-tt">cbbc</span>. </li></ul><p>In the second test case, string <span class="tex-font-style-tt">foo</span> satisfies $k = 1$ condition: </p><ul> <li> $p($<span class="tex-font-style-tt">foo</span>$) = 3$. Palindromic substrings are <span class="tex-font-style-tt">f</span>, <span class="tex-font-style-tt">o</span> and <span class="tex-font-style-tt">oo</span>. </li></ul> There are other possible answers.<p>In the third test case, string <span class="tex-font-style-tt">ayda</span> satisfies $k = 2$ conditions: </p><ul> <li> $p($<span class="tex-font-style-tt">ayd</span>$) = 3$. Palindromic substrings are <span class="tex-font-style-tt">a</span>, <span class="tex-font-style-tt">y</span> and <span class="tex-font-style-tt">d</span>. </li><li> $p($<span class="tex-font-style-tt">ayda</span>$) = 3$. Palindromic substrings are the same. </li></ul><p>In the fourth test case, string <span class="tex-font-style-tt">wada</span> satisfies $k = 2$ conditions: </p><ul> <li> $p($<span class="tex-font-style-tt">wad</span>$) = 3$. Palindromic substrings are <span class="tex-font-style-tt">w</span>, <span class="tex-font-style-tt">a</span> and <span class="tex-font-style-tt">d</span>. </li><li> $p($<span class="tex-font-style-tt">wada</span>$) = 4$. Palindromic substrings are the same, and one extra substring <span class="tex-font-style-tt">ada</span>. </li></ul><p>In the fifth test case, it can be proven that there is no string of length $4$ which has $5$ palindromic substrings.</p><p>In the sixth test case, string <span class="tex-font-style-tt">abcbcacbab</span> satisfies $k = 3$ conditions: </p><ul> <li> $p($<span class="tex-font-style-tt">abcb</span>$) = 4$. Palindromic substrings are <span class="tex-font-style-tt">a</span>, <span class="tex-font-style-tt">b</span>, <span class="tex-font-style-tt">c</span> and <span class="tex-font-style-tt">bcb</span>. </li><li> $p($<span class="tex-font-style-tt">abcbca</span>$) = 5$. Palindromic substrings are the same, and one extra substring <span class="tex-font-style-tt">cbc</span>. </li><li> $p($<span class="tex-font-style-tt">abcbcacbab</span>$) = 8$. Palindromic substrings are the same, and three extra substrings <span class="tex-font-style-tt">cac</span>, <span class="tex-font-style-tt">bab</span> and <span class="tex-font-style-tt">bcacb</span>. </li></ul>
