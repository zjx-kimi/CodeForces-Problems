## Description

<div><p>You are given a string $s$ consisting of lowercase Latin characters. In an operation, you can take a character and replace <span class="tex-font-style-bf">all</span> occurrences of this character with $\texttt{0}$ or replace <span class="tex-font-style-bf">all</span> occurrences of this character with $\texttt{1}$.</p><p>Is it possible to perform some number of moves so that the resulting string is an alternating binary string$^{\dagger}$? </p><p>For example, consider the string $\texttt{abacaba}$. You can perform the following moves: </p><ul> <li> Replace $\texttt{a}$ with $\texttt{0}$. Now the string is $\color{red}{\texttt{0}}\texttt{b}\color{red}{\texttt{0}}\texttt{c}\color{red}{\texttt{0}}\texttt{b}\color{red}{\texttt{0}}$. </li><li> Replace $\texttt{b}$ with $\texttt{1}$. Now the string is ${\texttt{0}}\color{red}{\texttt{1}}{\texttt{0}}\texttt{c}{\texttt{0}}\color{red}{\texttt{1}}{\texttt{0}}$. </li><li> Replace $\texttt{c}$ with $\texttt{1}$. Now the string is ${\texttt{0}}{\texttt{1}}{\texttt{0}}\color{red}{\texttt{1}}{\texttt{0}}{\texttt{1}}{\texttt{0}}$. This is an alternating binary string. </li></ul><p>$^{\dagger}$An <span class="tex-font-style-it">alternating binary string</span> is a string of $\texttt{0}$s and $\texttt{1}$s such that no two adjacent bits are equal. For example, $\texttt{01010101}$, $\texttt{101}$, $\texttt{1}$ are alternating binary strings, but $\texttt{0110}$, $\texttt{0a0a0}$, $\texttt{10100}$ are not.</p></div><div class="input-specification"><p>The input consists of multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 100$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ ($1 \leq n \leq 2000$)&nbsp;— the length of the string $s$.</p><p>The second line of each test case contains a string consisting of $n$ lowercase Latin characters&nbsp;— the string $s$.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" (without quotes) if you can make the string into an alternating binary string, and "<span class="tex-font-style-tt">NO</span>" (without quotes) otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p></div>

## Input

<p>The input consists of multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 100$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ ($1 \leq n \leq 2000$)&nbsp;— the length of the string $s$.</p><p>The second line of each test case contains a string consisting of $n$ lowercase Latin characters&nbsp;— the string $s$.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" (without quotes) if you can make the string into an alternating binary string, and "<span class="tex-font-style-tt">NO</span>" (without quotes) otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p>





```input1|2,3,6,7,10,11,14,15
8
7
abacaba
2
aa
1
y
4
bkpt
6
ninfia
6
banana
10
codeforces
8
testcase
```




```output1
YES
NO
YES
YES
NO
YES
NO
NO
```



## Note

<p>The first test case is explained in the statement.</p><p>In the second test case, the only possible binary strings you can make are $\texttt{00}$ and $\texttt{11}$, neither of which are alternating.</p><p>In the third test case, you can make $\texttt{1}$, which is an alternating binary string.</p>
