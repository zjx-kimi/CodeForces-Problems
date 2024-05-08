## Description

<div><p>Fedya is playing a new game called "The Legend of Link", in which one of the character's abilities is to combine two materials into one weapon. Each material has its own strength, which can be represented by a positive integer $x$. The strength of the resulting weapon is determined as the sum of the absolute differences of the digits in the <span class="tex-font-style-bf">decimal</span> representation of the integers at each position.</p><p>Formally, let the first material have strength $X = \overline{x_{1}x_{2} \ldots x_{n}}$, and the second material have strength $Y = \overline{y_{1}y_{2} \ldots y_{n}}$. Then the strength of the weapon is calculated as $|x_{1} - y_{1}| + |x_{2} - y_{2}| + \ldots + |x_{n} - y_{n}|$. If the integers have different lengths, then the shorter integer is <span class="tex-font-style-bf">padded with leading zeros</span>.</p><p>Fedya has an unlimited supply of materials with all possible strengths from $L$ to $R$, inclusive. Help him find the maximum possible strength of the weapon he can obtain.</p><p>An integer $C = \overline{c_{1}c_{2} \ldots c_{k}}$ is defined as an integer obtained by sequentially writing the digits $c_1, c_2, \ldots, c_k$ from left to right, i.e. $10^{k-1} \cdot c_1 + 10^{k-2} \cdot c_2 + \ldots + c_k$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 500$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $L$ and $R$ ($1 \le L \le R &lt; 10^{100}$)&nbsp;— the decimal representation of the integers representing the minimum and maximum strength of the materials that Fedya has. It is guaranteed that the integers $L$ and $R$ do not contain leading zeros.</p><p>Note that the input data may not fit into standard $32$-bit or $64$-bit integer data types.</p></div><div class="output-specification"><p>For each test case print one integer&nbsp;— the maximum possible strength of the weapon that Fedya can obtain from the given materials.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 500$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $L$ and $R$ ($1 \le L \le R &lt; 10^{100}$)&nbsp;— the decimal representation of the integers representing the minimum and maximum strength of the materials that Fedya has. It is guaranteed that the integers $L$ and $R$ do not contain leading zeros.</p><p>Note that the input data may not fit into standard $32$-bit or $64$-bit integer data types.</p>

## Output

<p>For each test case print one integer&nbsp;— the maximum possible strength of the weapon that Fedya can obtain from the given materials.</p>





```input1|2,4,6
6
53 57
179 239
13 37
132228 132228
54943329752812629795 55157581939688863366
88 1914
```




```output1
4
19
11
0
163
28
```



## Note

<p>In the first test case, the weapon made from materials with strengths $53$ and $57$ will have the maximum possible strength: $|5 - 5| + |3 - 7| = 4$.</p><p>In the second test case, the maximum strength is achieved with materials with strengths $190$ and $209$: $|1 - 2| + |9 - 0| + |0 - 9| = 19$.</p><p>In the fourth test case, there is only one valid strength, so the answer is $0$.</p><p>In the sixth test case, the maximum strength is achieved with materials with strengths $1909$ and $90$: $|1 - 0| + |9 - 0| + |0 - 9| + |9 - 0| = 28$. Note that the shorter integer was padded with leading zeros.</p>
