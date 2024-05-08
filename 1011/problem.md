## Description

<div><p>A binary string$^\dagger$ $b$ of odd length $m$ is <span class="tex-font-style-it">good</span> if $b_i$ is the median$^\ddagger$ of $b[1,i]^\S$ for all <span class="tex-font-style-bf">odd</span> indices $i$ ($1 \leq i \leq m$).</p><p>For a binary string $a$ of length $k$, a binary string $b$ of length $2k-1$ is an <span class="tex-font-style-it">extension</span> of $a$ if $b_{2i-1}=a_i$ for all $i$ such that $1 \leq i \leq k$. For example, <span class="tex-font-style-tt"><span class="tex-font-style-underline">1</span>0<span class="tex-font-style-underline">0</span>1<span class="tex-font-style-underline">0</span>1<span class="tex-font-style-underline">1</span></span> and <span class="tex-font-style-tt"><span class="tex-font-style-underline">1</span>1<span class="tex-font-style-underline">0</span>1<span class="tex-font-style-underline">0</span>0<span class="tex-font-style-underline">1</span></span> are <span class="tex-font-style-it">extensions</span> of the string <span class="tex-font-style-tt">1001</span>. String $x=$<span class="tex-font-style-tt">1011011</span> is not an <span class="tex-font-style-it">extension</span> of string $y=$<span class="tex-font-style-tt">1001</span> because $x_3 \neq y_2$. Note that there are $2^{k-1}$ different <span class="tex-font-style-it">extensions</span> of $a$.</p><p>You are given a binary string $s$ of length $n$. Find the sum of the number of <span class="tex-font-style-it">good</span> <span class="tex-font-style-it">extensions</span> over all prefixes of $s$. In other words, find $\sum_{i=1}^{n} f(s[1,i])$, where $f(x)$ gives number of <span class="tex-font-style-it">good</span> <span class="tex-font-style-it">extensions</span> of string $x$. Since the answer can be quite large, you only need to find it modulo $998\,244\,353$.</p><p>$^\dagger$ A binary string is a string whose elements are either $\mathtt{0}$ or $\mathtt{1}$.</p><p>$^\ddagger$ For a binary string $a$ of length $2m-1$, the median of $a$ is the (unique) element that occurs at least $m$ times in $a$.</p><p>$^\S$ $a[l,r]$ denotes the string of length $r-l+1$ which is formed by the concatenation of $a_l,a_{l+1},\ldots,a_r$ in that order.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$), where $n$ is the length of the binary string $s$.</p><p>The second line of each test case contains the binary string $s$ of length $n$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print the answer modulo $998\,244\,353$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$), where $n$ is the length of the binary string $s$.</p><p>The second line of each test case contains the binary string $s$ of length $n$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, print the answer modulo $998\,244\,353$.</p>





```input1|2,3,6,7,10,11
6
1
1
1
0
2
11
3
010
9
101101111
37
1011011111011010000011011111111011111
```




```output1
1
1
3
3
21
365
```



## Note

<p>In the first and second test cases, $f(s[1,1])=1$.</p><p>In the third test case, the answer is $f(s[1,1])+f(s[1,2])=1+2=3$. </p><p>In the fourth test case, the answer is $f(s[1,1])+f(s[1,2])+f(s[1,3])=1+1+1=3$.</p><p>$f(\mathtt{11})=2$ because two <span class="tex-font-style-it">good</span> <span class="tex-font-style-it">extensions</span> are possible: <span class="tex-font-style-tt">101</span> and <span class="tex-font-style-tt">111</span>.</p><p>$f(\mathtt{01})=1$ because only one <span class="tex-font-style-it">good</span> <span class="tex-font-style-it">extension</span> is possible: <span class="tex-font-style-tt">011</span>.</p>
