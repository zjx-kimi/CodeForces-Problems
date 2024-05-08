## Description

<div><p>There are $n$ bags numbered from $1$ to $n$, the $i$-th bag contains $a_i$ golden coins and $b_i$ silver coins.</p><p>The value of a gold coin is $1$. The value of a silver coin is either $0$ or $1$, determined for each silver coin independently ($0$ with probability $\frac{1}{2}$, $1$ with probability $\frac{1}{2}$).</p><p>You have to answer $q$ independent queries. Each query is the following: </p><ul> <li> $l$ $r$&nbsp;— calculate the probability that the total value of coins in bags from $l$ to $r$ is strictly greater than the total value in all other bags. </li></ul></div><div class="input-specification"><p>The first line contains two integers $n$ and $q$ ($1 \le n, q \le 3 \cdot 10^5$)&nbsp;— the number of bags and the number of queries, respectively.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($0 \le a_i \le 10^6$)&nbsp;— the number of gold coins in the $i$-th bag.</p><p>The third line contains $n$ integers $b_1, b_2, \dots, b_n$ ($0 \le b_i \le 10^6$)&nbsp;— the number of silver coins in the $i$-th bag.</p><p>Next $q$ lines contain queries. The $j$-th of the next $q$ lines contains two integers $l_j$ and $r_j$ ($1 \le l_j \le r_j \le n$)&nbsp;— the description of the $j$-th query.</p><p>Additional constraints on the input: </p><ul> <li> the sum of the array $a$ doesn't exceed $10^6$; </li><li> the sum of the array $b$ doesn't exceed $10^6$. </li></ul></div><div class="output-specification"><p>For each query, print one integer&nbsp;— the probability that the total value of coins in bags from $l$ to $r$ is strictly greater than the total value in all other bags, taken modulo $998244353$.</p><p>Formally, the probability can be expressed as an irreducible fraction $\frac{x}{y}$. You have to print the value of $x \cdot y^{-1} \bmod 998244353$, where $y^{-1}$ is an integer such that $y \cdot y^{-1} \bmod 998244353 = 1$.</p></div>

## Input

<p>The first line contains two integers $n$ and $q$ ($1 \le n, q \le 3 \cdot 10^5$)&nbsp;— the number of bags and the number of queries, respectively.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($0 \le a_i \le 10^6$)&nbsp;— the number of gold coins in the $i$-th bag.</p><p>The third line contains $n$ integers $b_1, b_2, \dots, b_n$ ($0 \le b_i \le 10^6$)&nbsp;— the number of silver coins in the $i$-th bag.</p><p>Next $q$ lines contain queries. The $j$-th of the next $q$ lines contains two integers $l_j$ and $r_j$ ($1 \le l_j \le r_j \le n$)&nbsp;— the description of the $j$-th query.</p><p>Additional constraints on the input: </p><ul> <li> the sum of the array $a$ doesn't exceed $10^6$; </li><li> the sum of the array $b$ doesn't exceed $10^6$. </li></ul>

## Output

<p>For each query, print one integer&nbsp;— the probability that the total value of coins in bags from $l$ to $r$ is strictly greater than the total value in all other bags, taken modulo $998244353$.</p><p>Formally, the probability can be expressed as an irreducible fraction $\frac{x}{y}$. You have to print the value of $x \cdot y^{-1} \bmod 998244353$, where $y^{-1}$ is an integer such that $y \cdot y^{-1} \bmod 998244353 = 1$.</p>





```input1|
2 2
1 0
0 2
2 2
1 1
```




```input2|
4 3
2 3 4 5
1 0 7 3
3 3
2 3
1 4
```




```output1
748683265 748683265
```




```output2
997756929 273932289 1
```



## Note

<p>In both queries from the first example, the answer is $\frac{1}{4}$.</p>
