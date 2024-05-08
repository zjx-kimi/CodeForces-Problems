## Description

<div><p>Congratulations, you have been accepted to the Master's Assistance Center! However, you were extremely bored in class and got tired of doing nothing, so you came up with a game for yourself.</p><p>You are given a string $s$ and an <span class="tex-font-style-bf">even</span> integer $n$. There are two types of operations that you can apply to it:</p><ol> <li> Add the reversed string $s$ to the end of the string $s$ (for example, if $s = $ <span class="tex-font-style-tt">cpm</span>, then after applying the operation $s = $ <span class="tex-font-style-tt">cpmmpc</span>). </li><li> Reverse the current string $s$ (for example, if $s = $ <span class="tex-font-style-tt">cpm</span>, then after applying the operation $s = $ <span class="tex-font-style-tt">mpc</span>). </li></ol><p>It is required to determine the lexicographically smallest$^{\dagger}$ string that can be obtained after applying <span class="tex-font-style-bf">exactly</span> $n$ operations. Note that you can apply operations of different types in any order, but you must apply exactly $n$ operations in total.</p><p>$^{\dagger}$A string $a$ is lexicographically smaller than a string $b$ if and only if one of the following holds: </p><ul> <li> $a$ is a prefix of $b$, but $a \ne b$; </li><li> in the first position where $a$ and $b$ differ, the string $a$ has a letter that appears earlier in the alphabet than the corresponding letter in $b$. </li></ul></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 500$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single <span class="tex-font-style-bf">even</span> integer $n$ ($2 \leq n \leq 10^9$) — the number of operations applied to the string $s$.</p><p>The second line of each test case contains a single string $s$ ($1 \leq |s| \leq 100$), consisting of lowercase English letters, — the string to which the operations are applied.</p></div><div class="output-specification"><p>For each test case, output a single line — the lexicographically smallest string that can be obtained after applying exactly $n$ operations.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 500$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single <span class="tex-font-style-bf">even</span> integer $n$ ($2 \leq n \leq 10^9$) — the number of operations applied to the string $s$.</p><p>The second line of each test case contains a single string $s$ ($1 \leq |s| \leq 100$), consisting of lowercase English letters, — the string to which the operations are applied.</p>

## Output

<p>For each test case, output a single line — the lexicographically smallest string that can be obtained after applying exactly $n$ operations.</p>





```input1|2,3,6,7,10,11
5
4
cpm
2
grib
10
kupitimilablodarbuz
1000000000
capybara
6
abacaba
```




```output1
cpm
birggrib
kupitimilablodarbuz
arabypaccapybara
abacaba
```



## Note

<p>In the first test case, you can apply the operation of the second type (i.e., reverse the string $s$) $4$ times. Then the string $s$ will remain equal to <span class="tex-font-style-tt">cpm</span>.</p><p>In the second test case, you can do the following: </p><ul> <li> Apply the operation of the second type, after which $s$ will become equal to <span class="tex-font-style-tt">birg</span>. </li><li> Apply operation of the first type (i.e., add the reversed string $s$ to the end of the string $s$), after which $s$ will become equal to <span class="tex-font-style-tt">birggrib</span>. </li></ul>
