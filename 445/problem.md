## Description

<div><p>You have a set $S$ of $n$ distinct integers between $1$ and $m$.</p><p>Each second you do the following steps: </p><ol> <li> Pick an element $x$ in $S$ uniformly at random. </li><li> Remove $x$ from $S$. </li><li> If $x+1 \leq m$ and $x+1$ is not in $S$, add $x+1$ to $S$. </li></ol><p>What is the expected number of seconds until $S$ is empty?</p><p>Output the answer modulo $1\,000\,000\,007$.</p><p>Formally, let $P = 1\,000\,000\,007$. It can be shown that the answer can be expressed as an irreducible fraction $\frac{a}{b}$, where $a$ and $b$ are integers and $b \not \equiv 0 \pmod{P}$. Output the integer equal to $a \cdot b^{-1} \bmod P$. In other words, output an integer $z$ such that $0 \le z &lt; P$ and $z \cdot b \equiv a \pmod{P}$.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $m$ ($1 \leq n \leq m \leq 500$)&nbsp;— the number of elements in the set $S$ and the upper bound on the value of the elements in $S$.</p><p>The second line contains $n$ integers $S_1,\,S_2,\,\dots,\,S_n$ ($1 \leq S_1 &lt; S_2 &lt; \ldots &lt; S_n \leq m$)&nbsp;— the elements of the set $S$.</p></div><div class="output-specification"><p>Output a single integer&nbsp;— the expected number of seconds until $S$ is empty, modulo $1\,000\,000\,007$.</p></div>

## Input

<p>The first line contains two integers $n$ and $m$ ($1 \leq n \leq m \leq 500$)&nbsp;— the number of elements in the set $S$ and the upper bound on the value of the elements in $S$.</p><p>The second line contains $n$ integers $S_1,\,S_2,\,\dots,\,S_n$ ($1 \leq S_1 &lt; S_2 &lt; \ldots &lt; S_n \leq m$)&nbsp;— the elements of the set $S$.</p>

## Output

<p>Output a single integer&nbsp;— the expected number of seconds until $S$ is empty, modulo $1\,000\,000\,007$.</p>





```input1
2 3
1 3
```




```input2
5 10
1 2 3 4 5
```




```input3
5 10
2 3 6 8 9
```




```input4
1 100
1
```




```output1
750000009
```




```output2
300277731
```




```output3
695648216
```




```output4
100
```



## Note

<p>For test 1, here is a list of all the possible scenarios and their probabilities:</p><ol> <li> $[1, 3]$ (50% chance) $\to$ $[1]$ $\to$ $[2]$ $\to$ $[3]$ $\to$ $[]$ </li><li> $[1, 3]$ (50% chance) $\to$ $[2, 3]$ (50% chance) $\to$ $[2]$ $\to$ $[3]$ $\to$ $[]$ </li><li> $[1, 3]$ (50% chance) $\to$ $[2, 3]$ (50% chance) $\to$ $[3]$ $\to$ $[]$ </li></ol><p>Adding them up, we get $\frac{1}{2}\cdot 4 + \frac{1}{4} \cdot 4 + \frac{1}{4} \cdot 3 = \frac{15}{4}$. We see that $750000009 \cdot 4 \equiv 15 \pmod{1\,000\,000\,007}$.</p>
