## Description

<div><p>Joey is low on money. His friend Chandler wants to lend Joey some money, but can't give him directly, as Joey is too proud of himself to accept it. So, in order to trick him, Chandler asks Joey to play a game.</p><p>In this game, Chandler gives Joey an array $a_1, a_2, \dots, a_n$ ($n \geq 2$) of positive integers ($a_i \ge 1$).</p><p>Joey can perform the following operation on the array any number of times: </p><ol> <li> Take two indices $i$ and $j$ ($1 \le i &lt; j \le n)$. </li><li> Choose two <span class="tex-font-style-it">integers</span> $x$ and $y$ ($x, y \ge 1$) such that $x \cdot y = a_i \cdot a_j$. </li><li> Replace $a_i$ by $x$ and $a_j$ by $y$. </li></ol><p>In the end, Joey will get the money equal to <span class="tex-font-style-bf">the sum</span> of elements of the final array. </p><p>Find the maximum amount of money $\mathrm{ans}$ Joey can get <span class="tex-font-style-bf">but print</span> $2022 \cdot \mathrm{ans}$. Why multiplied by $2022$? Because we are never gonna see it again!</p><p>It is guaranteed that the product of all the elements of the array $a$ doesn't exceed $10^{12}$. </p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 4000$). Description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \leq n \leq 50$)&nbsp;— the length of the array $a$.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \leq a_i \leq 10^6$)&nbsp;— the array itself.</p><p>It's guaranteed that the product of all $a_i$ doesn't exceed $10^{12}$ (i.&nbsp;e. $a_1 \cdot a_2 \cdot \ldots \cdot a_n \le 10^{12}$).</p></div><div class="output-specification"><p>For each test case, print the maximum money Joey can get <span class="tex-font-style-bf">multiplied by</span> $2022$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 4000$). Description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \leq n \leq 50$)&nbsp;— the length of the array $a$.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \leq a_i \leq 10^6$)&nbsp;— the array itself.</p><p>It's guaranteed that the product of all $a_i$ doesn't exceed $10^{12}$ (i.&nbsp;e. $a_1 \cdot a_2 \cdot \ldots \cdot a_n \le 10^{12}$).</p>

## Output

<p>For each test case, print the maximum money Joey can get <span class="tex-font-style-bf">multiplied by</span> $2022$.</p>





```input1|2,3,6,7
3
3
2 3 2
2
1 3
3
1000000 1000000 1
```




```output1
28308
8088
2022000000004044
```



## Note

<p>In the first test case, Joey can do the following: </p><ol> <li> He chooses $i = 1$ and $j = 2$ (so he has $a[i] \cdot a[j] = 6$), chooses $x = 6$ and $y = 1$ and makes $a[i] = 6$ and $a[j] = 1$. $$[2, 3, 2] \xrightarrow[x = 6,\; y = 1]{i = 1,\; j = 2} [6, 1, 2]$$</li><li> He chooses $i = 1$ and $j = 3$ (so he has $a[i] \cdot a[j] = 12$), chooses $x = 12$ and $y = 1$ and makes $a[i] = 12$ and $a[j] = 1$. $$[6, 1, 2] \xrightarrow[x = 12,\; y = 1]{i = 1,\; j = 3} [12, 1, 1]$$ </li></ol> The sum is $14$ which is the maximum of all possible sums. The answer is $2022 \cdot 14 = 28308$.
