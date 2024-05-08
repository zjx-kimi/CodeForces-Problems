## Description

<div><p>Anya received a string $s$ of length $n$ brought from Rome. The string $s$ consists of lowercase Latin letters and at first glance does not raise any suspicions. An instruction was attached to the string.</p><p><span class="tex-font-style-it">Start of the instruction.</span></p><p>A palindrome is a string that reads the same from left to right and right to left. For example, the strings "<span class="tex-font-style-tt">anna</span>", "<span class="tex-font-style-tt">aboba</span>", "<span class="tex-font-style-tt">level</span>" are palindromes, while the strings "<span class="tex-font-style-tt">gorilla</span>", "<span class="tex-font-style-tt">banan</span>", "<span class="tex-font-style-tt">off</span>" are not.</p><p>A substring $[l \ldots r]$ of string $s$ is a string $s_l s_{l+1} \ldots s_{r-1} s_r$. For example, the substring $[4 \ldots 6]$ of the string "<span class="tex-font-style-tt">generation</span>" is the string "<span class="tex-font-style-tt">era</span>".</p><p>A string is called <span class="tex-font-style-it">beautiful</span> if it <span class="tex-font-style-bf">does not</span> contain a substring of length <span class="tex-font-style-bf">at least</span> two that is a palindrome. For example, the strings "<span class="tex-font-style-tt">fox</span>", "<span class="tex-font-style-tt">abcdef</span>", and "<span class="tex-font-style-tt">yioy</span>" are <span class="tex-font-style-it">beautiful</span>, while the strings "<span class="tex-font-style-tt">xyxx</span>", "<span class="tex-font-style-tt">yikjkitrb</span>" are not.</p><p>When an integer $x$ is added to the character $s_i$, it is replaced $x$ times with the <span class="tex-font-style-bf">next</span> character in the alphabet, with "<span class="tex-font-style-tt">z</span>" being replaced by "<span class="tex-font-style-tt">a</span>".</p><p>When an integer $x$ is added to the substring $[l, r]$ of string $s$, it becomes the string $s_1 s_2 \ldots s_{l-1} (s_l + x) (s_{l+1} + x) \ldots (s_{r-1} + x) (s_r + x) s_{r+1} \ldots s_n$. For example, when the substring $[2, 4]$ of the string "<span class="tex-font-style-tt">abazaba</span>" is added with the number $6$, the resulting string is "<span class="tex-font-style-tt">ahgfaba</span>".</p><p><span class="tex-font-style-it">End of the instruction.</span></p><p>After reading the instruction, Anya resigned herself to the fact that she has to answer $m$ queries. The queries can be of two types:</p><ol> <li> Add the number $x$ to the substring $[l \ldots r]$ of string $s$. </li><li> Determine whether the substring $[l \ldots r]$ of string $s$ is <span class="tex-font-style-it">beautiful</span>. </li></ol></div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \le t \le 10^4$) - the number of test cases.</p><p>The descriptions of the test cases follow.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \le n, m \le 2 \cdot 10^5$) - the length of the string $s$ and the number of queries.</p><p>The second line of each test case contains the string $s$ of length $n$, consisting of lowercase Latin letters.</p><p>The next $m$ lines contain the queries:</p><ul> <li> $1$ $l$ $r$ $x$ ($1 \le l \le r \le n$, $1 \le x \le 10^9$) - description of a query of the first type; </li><li> $2$ $l$ $r$ ($1 \le l \le r \le n$) - description of a query of the second type. </li></ul><p>It is guaranteed that the sum of $n$ and the sum of $m$ over all test cases <span class="tex-font-style-bf">do not exceed</span> $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each query of the second type, output "<span class="tex-font-style-tt">YES</span>" if the substring $[l \ldots r]$ of string $s$ is <span class="tex-font-style-it">beautiful</span>, otherwise output "<span class="tex-font-style-tt">NO</span>".</p><p>You can output "<span class="tex-font-style-tt">YES</span>" and "<span class="tex-font-style-tt">NO</span>" in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive answers).</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \le t \le 10^4$) - the number of test cases.</p><p>The descriptions of the test cases follow.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \le n, m \le 2 \cdot 10^5$) - the length of the string $s$ and the number of queries.</p><p>The second line of each test case contains the string $s$ of length $n$, consisting of lowercase Latin letters.</p><p>The next $m$ lines contain the queries:</p><ul> <li> $1$ $l$ $r$ $x$ ($1 \le l \le r \le n$, $1 \le x \le 10^9$) - description of a query of the first type; </li><li> $2$ $l$ $r$ ($1 \le l \le r \le n$) - description of a query of the second type. </li></ul><p>It is guaranteed that the sum of $n$ and the sum of $m$ over all test cases <span class="tex-font-style-bf">do not exceed</span> $2 \cdot 10^5$.</p>

## Output

<p>For each query of the second type, output "<span class="tex-font-style-tt">YES</span>" if the substring $[l \ldots r]$ of string $s$ is <span class="tex-font-style-it">beautiful</span>, otherwise output "<span class="tex-font-style-tt">NO</span>".</p><p>You can output "<span class="tex-font-style-tt">YES</span>" and "<span class="tex-font-style-tt">NO</span>" in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive answers).</p>





```input1|2,3,4,5,6,7,8,9,10,11,18,19,20,21,22,27,28,29,30,31
5
12 8
tedubcyyxopz
2 2 5
1 4 8 2
2 1 7
1 3 5 40
1 9 11 3
1 10 10 9
2 4 10
2 10 12
10 4
ubnxwwgzjt
2 4 10
2 10 10
1 6 10 8
2 7 7
11 3
hntcxfxyhtu
1 4 6 1
2 4 10
1 4 10 21
13 2
yxhlmzfhqctir
1 5 9 3
1 8 13 15
2 3
bp
1 1 2 15
1 1 2 18
1 2 2 1000000000
```




```output1
YES
NO
NO
YES
NO
YES
YES
YES
```



## Note

<p>In the first test case of the first test, the following happens:</p><ul> <li> <span class="tex-font-style-tt">t<span class="tex-font-style-bf">edub</span>cyyxopz</span>: the string <span class="tex-font-style-tt">edub</span> is <span class="tex-font-style-it">beautiful</span>; </li><li> <span class="tex-font-style-tt">ted<span class="tex-font-style-bf">ubcyy</span>xopz</span> $\to$ <span class="tex-font-style-tt">tedwdeaaxopz</span>; </li><li> <span class="tex-font-style-tt"><span class="tex-font-style-bf">tedwdea</span>axopz</span>: the string <span class="tex-font-style-tt">tedwdea</span> is not <span class="tex-font-style-it">beautiful</span> as it contains the palindrome <span class="tex-font-style-tt">edwde</span>; </li><li> <span class="tex-font-style-tt">te<span class="tex-font-style-bf">dwd</span>eaaxopz</span> $\to$ <span class="tex-font-style-tt">terkreaaxopz</span>; </li><li> <span class="tex-font-style-tt">terkreaa<span class="tex-font-style-bf">xop</span>z</span> $\to$ <span class="tex-font-style-tt">terkreaaarsz</span>; </li><li> <span class="tex-font-style-tt">terkreaaa<span class="tex-font-style-bf">r</span>sz</span> $\to$ <span class="tex-font-style-tt">terkreaaaasz</span>; </li><li> <span class="tex-font-style-tt">ter<span class="tex-font-style-bf">kreaaaa</span>sz</span>: the string <span class="tex-font-style-tt">kreaaaa</span> is not <span class="tex-font-style-it">beautiful</span> as it contains the palindrome <span class="tex-font-style-tt">aaaa</span>; </li><li> <span class="tex-font-style-tt">terkreaaa<span class="tex-font-style-bf">asz</span></span>: the string <span class="tex-font-style-tt">asz</span> is <span class="tex-font-style-it">beautiful</span>. </li></ul>
