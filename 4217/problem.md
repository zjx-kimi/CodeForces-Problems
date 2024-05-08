## Description

<div><p>Traveling around the world you noticed that many shop owners raise prices to inadequate values if the see you are a foreigner.</p><p>You define inadequate numbers as follows: </p><ul> <li> all integers from $1$ to $9$ are inadequate; </li><li> for an integer $x \ge 10$ to be inadequate, it is required that the integer $\lfloor x / 10 \rfloor$ is inadequate, but that's not the only condition. Let's sort all the inadequate integers. Let $\lfloor x / 10 \rfloor$ have number $k$ in this order. Then, the integer $x$ is inadequate only if the last digit of $x$ is strictly less than the reminder of division of $k$ by $11$. </li></ul><p>Here $\lfloor x / 10 \rfloor$ denotes $x/10$ rounded down.</p><p>Thus, if $x$ is the $m$-th in increasing order inadequate number, and $m$ gives the remainder $c$ when divided by $11$, then integers $10 \cdot x + 0, 10 \cdot x + 1 \ldots, 10 \cdot x + (c - 1)$ are inadequate, while integers $10 \cdot x + c, 10 \cdot x + (c + 1), \ldots, 10 \cdot x + 9$ are not inadequate.</p><p>The first several inadequate integers are $1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 20, 21, 30, 31, 32 \ldots$. After that, since $4$ is the fourth inadequate integer, $40, 41, 42, 43$ are inadequate, while $44, 45, 46, \ldots, 49$ are not inadequate; since $10$ is the $10$-th inadequate number, integers $100, 101, 102, \ldots, 109$ are all inadequate. And since $20$ is the $11$-th inadequate number, none of $200, 201, 202, \ldots, 209$ is inadequate.</p><p>You wrote down all the prices you have seen in a trip. Unfortunately, all integers got concatenated in one large digit string $s$ and you lost the bounds between the neighboring integers. You are now interested in the number of substrings of the resulting string that form an inadequate number. If a substring appears more than once at different positions, all its appearances are counted separately.</p></div><div class="input-specification"><p>The only line contains the string $s$ ($1 \le |s| \le 10^5$), consisting only of digits. It is guaranteed that the first digit of $s$ is not zero.</p></div><div class="output-specification"><p>In the only line print the number of substrings of $s$ that form an inadequate number.</p></div>

## Input

<p>The only line contains the string $s$ ($1 \le |s| \le 10^5$), consisting only of digits. It is guaranteed that the first digit of $s$ is not zero.</p>

## Output

<p>In the only line print the number of substrings of $s$ that form an inadequate number.</p>





```input1
4021
```




```input2
110
```




```output1
6
```




```output2
3
```



## Note

<p>In the first example the inadequate numbers in the string are $1, 2, 4, 21, 40, 402$. </p><p>In the second example the inadequate numbers in the string are $1$ and $10$, and $1$ appears twice (on the first and on the second positions).</p>
