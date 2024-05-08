## Description

<div><p><span class="tex-font-style-bf">This is the hard version of the problem. It differs from the easy one only in constraints on $n$. You can make hacks only if you lock both versions.</span></p><p>Let $a_1, a_2, \ldots, a_n$ be an array of non-negative integers. Let $F(a_1, a_2, \ldots, a_n)$ be the sorted in the non-decreasing order array of $n - 1$ smallest numbers of the form $a_i + a_j$, where $1 \le i &lt; j \le n$. In other words, $F(a_1, a_2, \ldots, a_n)$ is the sorted in the non-decreasing order array of $n - 1$ smallest sums of all possible pairs of elements of the array $a_1, a_2, \ldots, a_n$. For example, $F(1, 2, 5, 7) = [1 + 2, 1 + 5, 2 + 5] = [3, 6, 7]$.</p><p>You are given an array of non-negative integers $a_1, a_2, \ldots, a_n$. Determine the single element of the array $\underbrace{F(F(F\ldots F}_{n-1}(a_1, a_2, \ldots, a_n)\ldots))$. Since the answer can be quite large, output it modulo $10^9+7$.</p></div><div class="input-specification"><p>The first line contains one integer $n$ ($2 \le n \le 2 \cdot 10^5$)&nbsp;— the initial length of the array.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i \le 10^9$)&nbsp;— the array elements.</p></div><div class="output-specification"><p>Output a single number&nbsp;— the answer modulo $10^9 + 7$.</p></div>

## Input

<p>The first line contains one integer $n$ ($2 \le n \le 2 \cdot 10^5$)&nbsp;— the initial length of the array.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i \le 10^9$)&nbsp;— the array elements.</p>

## Output

<p>Output a single number&nbsp;— the answer modulo $10^9 + 7$.</p>





```input1
5
1 2 4 5 6
```




```input2
9
1 1 1 7 7 7 9 9 9
```




```input3
7
1 7 9 2 0 0 9
```




```input4
3
1000000000 1000000000 777
```




```output1
34
```




```output2
256
```




```output3
20
```




```output4
1540
```



## Note

<p>In the first test, the array is transformed as follows: $[1, 2, 4, 5, 6] \to [3, 5, 6, 6] \to [8, 9, 9] \to [17, 17] \to [34]$. The only element of the final array is $34$.</p><p>In the second test, $F(a_1, a_2, \ldots, a_n)$ is $[2, 2, 2, 8, 8, 8, 8, 8]$. This array is made up of $3$ numbers of the form $1 + 1$ and $5$ numbers of the form $1 + 7$. </p><p>In the fourth test, the array is transformed as follows: $[10^9, 10^9, 777] \to [10^9+777, 10^9+777] \to [2 \cdot 10^9 + 1554]$. $2 \cdot 10^9 + 1554$ modulo $10^9+7$ equals $1540$.</p>
