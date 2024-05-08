## Description

<div><p>You are given a binary string $s$ (a string consisting only of <span class="tex-font-style-tt">0</span>-s and <span class="tex-font-style-tt">1</span>-s).</p><p>You can perform two types of operations on $s$: </p><ol> <li> delete one character from $s$. This operation costs $1$ coin; </li><li> swap any pair of characters in $s$. This operation is free (costs $0$ coins). </li></ol><p>You can perform these operations any number of times and in any order.</p><p>Let's name a string you've got after performing operations above as $t$. The string $t$ is <span class="tex-font-style-it">good</span> if for each $i$ from <span class="tex-font-style-bf">$1$ to $|t|$</span> $t_i \neq s_i$ ($|t|$ is the length of the string $t$). The empty string is <span class="tex-font-style-it">always good</span>. Note that you are comparing the resulting string $t$ with the <span class="tex-font-style-it">initial string</span> $s$.</p><p>What is the minimum total cost to make the string $t$ good?</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then $t$ test cases follow.</p><p>The only line of each test case contains a binary string $s$ ($1 \le |s| \le 2 \cdot 10^5$; $s_i \in \{$<span class="tex-font-style-tt">0</span>, <span class="tex-font-style-tt">1</span>$\}$)&nbsp;— the initial string, consisting of characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span>.</p><p>Additional constraint on the input: the total length of all strings $s$ doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print one integer — the minimum total cost to make string $t$ good.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then $t$ test cases follow.</p><p>The only line of each test case contains a binary string $s$ ($1 \le |s| \le 2 \cdot 10^5$; $s_i \in \{$<span class="tex-font-style-tt">0</span>, <span class="tex-font-style-tt">1</span>$\}$)&nbsp;— the initial string, consisting of characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span>.</p><p>Additional constraint on the input: the total length of all strings $s$ doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, print one integer — the minimum total cost to make string $t$ good.</p>





```input1|2,4
4
0
011
0101110001
111100
```




```output1
1
1
0
4
```



## Note

<p>In the first test case, you have to delete a character from $s$ to get the empty string $t$. Only then $t$ becomes good. One deletion costs $1$ coin.</p><p>In the second test case, you can, for example, delete the second character from $s$ to get the string <span class="tex-font-style-tt">01</span>, and then swap the first and second characters to get the string $t$ $=$ <span class="tex-font-style-tt">10</span>. String $t$ is good, since $t_1 \neq s_1$ and $t_2 \neq s_2$. The total cost is $1$ coin.</p><p>In the third test case, you can, for example, swap $s_1$ with $s_2$, swap $s_3$ with $s_4$, swap $s_5$ with $s_7$, $s_6$ with $s_8$ and $s_9$ with $s_{10}$. You'll get $t$ $=$ <span class="tex-font-style-tt">1010001110</span>. All swap operations are free, so the total cost is $0$.</p>
