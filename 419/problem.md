## Description

<div><p>You are given a binary string $s$ (a binary string is a string consisting of characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span>).</p><p>Let's call a binary string <span class="tex-font-style-bf">balanced</span> if the number of subsequences <span class="tex-font-style-tt">01</span> (the number of indices $i$ and $j$ such that $1 \le i &lt; j \le n$, $s_i=0$ and $s_j=1$) equals to the number of subsequences <span class="tex-font-style-tt">10</span> (the number of indices $k$ and $l$ such that $1 \le k &lt; l \le n$, $s_k=1$ and $s_l=0$) in it.</p><p>For example, the string <span class="tex-font-style-tt">1000110</span> is balanced, because both the number of subsequences <span class="tex-font-style-tt">01</span> and the number of subsequences <span class="tex-font-style-tt">10</span> are equal to $6$. On the other hand, <span class="tex-font-style-tt">11010</span> is not balanced, because the number of subsequences <span class="tex-font-style-tt">01</span> is $1$, but the number of subsequences <span class="tex-font-style-tt">10</span> is $5$. </p><p>You can perform the following operation any number of times: choose two characters in $s$ and swap them. Your task is to calculate the minimum number of operations to make the string $s$ balanced.</p></div><div class="input-specification"><p>The only line contains the string $s$ ($3 \le |s| \le 100$) consisting of characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span>. </p><p>Additional constraint on the input: the string $s$ can be made balanced.</p></div><div class="output-specification"><p>Print a single integer&nbsp;— the minimum number of swap operations to make the string $s$ balanced.</p></div>

## Input

<p>The only line contains the string $s$ ($3 \le |s| \le 100$) consisting of characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span>. </p><p>Additional constraint on the input: the string $s$ can be made balanced.</p>

## Output

<p>Print a single integer&nbsp;— the minimum number of swap operations to make the string $s$ balanced.</p>





```input1
101
```




```input2
1000110
```




```input3
11010
```




```input4
11001100
```




```output1
0
```




```output2
0
```




```output3
1
```




```output4
2
```



## Note

<p>In the first example, the string is already balanced, the number of both <span class="tex-font-style-tt">01</span> and <span class="tex-font-style-tt">10</span> is equal to $1$.</p><p>In the second example, the string is already balanced, the number of both <span class="tex-font-style-tt">01</span> and <span class="tex-font-style-tt">10</span> is equal to $6$.</p><p>In the third example, one of the possible answers is the following one: <span class="tex-font-style-tt">11010</span> $\rightarrow$ <span class="tex-font-style-tt">01110</span>. After that, the number of both <span class="tex-font-style-tt">01</span> and <span class="tex-font-style-tt">10</span> is equal to $3$.</p><p>In the fourth example, one of the possible answers is the following one: <span class="tex-font-style-tt">11001100</span> $\rightarrow$ <span class="tex-font-style-tt">11001010</span> $\rightarrow$ <span class="tex-font-style-tt">11000011</span>. After that, the number of both <span class="tex-font-style-tt">01</span> and <span class="tex-font-style-tt">10</span> is equal to $8$.</p>
