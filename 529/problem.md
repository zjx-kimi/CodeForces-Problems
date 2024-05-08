## Description

<div><p>You are given two strings of equal length $s_1$ and $s_2$, consisting of lowercase Latin letters, and an integer $t$.</p><p>You need to answer $q$ queries, numbered from $1$ to $q$. The $i$-th query comes in the $i$-th second of time. Each query is one of three types: </p><ul> <li> block the characters at position $pos$ (indexed from $1$) in both strings for $t$ seconds; </li><li> swap two unblocked characters; </li><li> determine if the two strings are equal at the time of the query, ignoring blocked characters. </li></ul><p>Note that in queries of the second type, the characters being swapped can be from the same string or from $s_1$ and $s_2$.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $T$ ($1 \le T \le 10^4$)&nbsp;— the number of test cases.</p><p>Then follow the descriptions of the test cases.</p><p>The first line of each test case contains a string $s_1$ consisting of lowercase Latin letters (length no more than $2 \cdot 10^5$).</p><p>The second line of each test case contains a string $s_2$ consisting of lowercase Latin letters (length no more than $2 \cdot 10^5$).</p><p><span class="tex-font-style-bf">The strings have equal length.</span></p><p>The third line of each test case contains two integers $t$ and $q$ ($1 \le t, q \le 2 \cdot 10^5$). The number $t$ indicates the number of seconds for which a character is blocked. The number $q$ corresponds to the number of queries.</p><p>Each of the next $q$ lines of each test case contains a single query. Each query is one of three types: </p><ul> <li> "$1\ \ \ pos$"&nbsp;— block the characters at position $pos$ in both strings for $t$ seconds; </li><li> "$2\ \ \ 1/\;\!2\ \ \ pos_1\ \ \ 1/\;\!2\ \ \ pos_2$"&nbsp;— swap two unblocked characters. The second number in the query indicates the number of the string from which the first character for the swap is taken. The third number in the query indicates the position in that string of that character. The fourth number in the query indicates the number of the string from which the second character for the swap is taken. The fifth number in the query indicates the position in that string of that character; </li><li> "$3$"&nbsp;— determine if the two strings are equal at the time of the query, ignoring blocked characters. </li></ul><p>For queries of the first type, it is guaranteed that at the time of the query, the characters at position $pos$ are not blocked.</p><p>For queries of the second type, it is guaranteed that the characters being swapped are not blocked.</p><p>All values of $pos, pos_1, pos_2$ are in the range from $1$ to the length of the strings.</p><p>The sum of the values of $q$ over all test cases, as well as the total length of the strings $s_1$, does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each query of the third type, output "<span class="tex-font-style-tt">YES</span>" if the two strings $s_1$ and $s_2$ are equal at the time of the query, ignoring blocked characters, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output each letter in any case (lowercase or uppercase). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be accepted as a positive answer.</p></div>

## Input

<p>The first line of the input contains a single integer $T$ ($1 \le T \le 10^4$)&nbsp;— the number of test cases.</p><p>Then follow the descriptions of the test cases.</p><p>The first line of each test case contains a string $s_1$ consisting of lowercase Latin letters (length no more than $2 \cdot 10^5$).</p><p>The second line of each test case contains a string $s_2$ consisting of lowercase Latin letters (length no more than $2 \cdot 10^5$).</p><p><span class="tex-font-style-bf">The strings have equal length.</span></p><p>The third line of each test case contains two integers $t$ and $q$ ($1 \le t, q \le 2 \cdot 10^5$). The number $t$ indicates the number of seconds for which a character is blocked. The number $q$ corresponds to the number of queries.</p><p>Each of the next $q$ lines of each test case contains a single query. Each query is one of three types: </p><ul> <li> "$1\ \ \ pos$"&nbsp;— block the characters at position $pos$ in both strings for $t$ seconds; </li><li> "$2\ \ \ 1/\;\!2\ \ \ pos_1\ \ \ 1/\;\!2\ \ \ pos_2$"&nbsp;— swap two unblocked characters. The second number in the query indicates the number of the string from which the first character for the swap is taken. The third number in the query indicates the position in that string of that character. The fourth number in the query indicates the number of the string from which the second character for the swap is taken. The fifth number in the query indicates the position in that string of that character; </li><li> "$3$"&nbsp;— determine if the two strings are equal at the time of the query, ignoring blocked characters. </li></ul><p>For queries of the first type, it is guaranteed that at the time of the query, the characters at position $pos$ are not blocked.</p><p>For queries of the second type, it is guaranteed that the characters being swapped are not blocked.</p><p>All values of $pos, pos_1, pos_2$ are in the range from $1$ to the length of the strings.</p><p>The sum of the values of $q$ over all test cases, as well as the total length of the strings $s_1$, does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each query of the third type, output "<span class="tex-font-style-tt">YES</span>" if the two strings $s_1$ and $s_2$ are equal at the time of the query, ignoring blocked characters, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output each letter in any case (lowercase or uppercase). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be accepted as a positive answer.</p>





```input1|2,3,4,5,6,7,8,9,10,11
2
codeforces
codeblocks
5 7
3
1 5
1 6
1 7
1 9
3
3
cool
club
2 5
2 1 2 2 3
2 2 2 2 4
1 2
3
3
```




```output1
NO
YES
NO
YES
NO
```



## Note

<p>Let's look at the strings $s_1$ and $s_2$ after each of the $q$ queries. Blocked characters will be denoted in red.</p><p>First example input:</p><p>($codeforces$, $codeblocks$) $\rightarrow$ ($codeforces$, $codeblocks$) $\rightarrow$ ($code\color{red}{f}orces$, $code\color{red}{b}locks$) $\rightarrow$ ($code\color{red}{fo}rces$, $code\color{red}{bl}ocks$) $\rightarrow$ ($code\color{red}{for}ces$, $code\color{red}{blo}cks$) $\rightarrow$ ($code\color{red}{for}c\color{red}{e}s$, $code\color{red}{blo}c\color{red}{k}s$) $\rightarrow$ ($code\color{red}{for}c\color{red}{e}s$, $code\color{red}{blo}c\color{red}{k}s$) $\rightarrow$ ($codef\color{red}{or}c\color{red}{e}s$, $codeb\color{red}{lo}c\color{red}{k}s$)</p><p>Second example input:</p><p>($cool$, $club$) $\rightarrow$ ($cuol$, $clob$) $\rightarrow$ ($cuol$, $cbol$) $\rightarrow$ ($c\color{red}{u}ol$, $c\color{red}{b}ol$) $\rightarrow$ ($c\color{red}{u}ol$, $c\color{red}{b}ol$) $\rightarrow$ ($cuol$, $cbol$)</p>
