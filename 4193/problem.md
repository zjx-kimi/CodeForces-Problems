## Description

<div><p>You are planning to build housing on a street. There are $n$ spots available on the street on which you can build a house. The spots are labeled from $1$ to $n$ from left to right. In each spot, you can build a house with an integer height between $0$ and $h$.</p><p>In each spot, if a house has height $a$, you can gain $a^2$ dollars from it.</p><p>The city has $m$ zoning restrictions though. The $i$-th restriction says that if the tallest house from spots $l_i$ to $r_i$ is strictly more than $x_i$, you must pay a fine of $c_i$.</p><p>You would like to build houses to maximize your profit (sum of dollars gained minus fines). Determine the maximum profit possible.</p></div><div class="input-specification"><p>The first line contains three integers $n,h,m$ ($1 \leq n,h,m \leq 50$)&nbsp;— the number of spots, the maximum height, and the number of restrictions, respectively.</p><p>Each of the next $m$ lines contains four integers $l_i, r_i, x_i, c_i$ ($1 \leq l_i \leq r_i \leq n$, $0 \leq x_i \leq h$, $1 \leq c_i \leq 5\,000$).</p></div><div class="output-specification"><p>Print a single integer denoting the maximum profit you can make.</p></div>

## Input

<p>The first line contains three integers $n,h,m$ ($1 \leq n,h,m \leq 50$)&nbsp;— the number of spots, the maximum height, and the number of restrictions, respectively.</p><p>Each of the next $m$ lines contains four integers $l_i, r_i, x_i, c_i$ ($1 \leq l_i \leq r_i \leq n$, $0 \leq x_i \leq h$, $1 \leq c_i \leq 5\,000$).</p>

## Output

<p>Print a single integer denoting the maximum profit you can make.</p>





```input1
3 3 3
1 1 1 1000
2 2 3 1000
3 3 2 1000
```




```input2
4 10 2
2 3 8 76
3 4 7 39
```




```output1
14
```




```output2
289
```



## Note

<p>In the first example, it's optimal to build houses with heights $[1, 3, 2]$. We get a gain of $1^2+3^2+2^2 = 14$. We don't violate any restrictions, so there are no fees, so the total profit is $14 - 0 = 14$.</p><p>In the second example, it's optimal to build houses with heights $[10, 8, 8, 10]$. We get a gain of $10^2+8^2+8^2+10^2 = 328$, and we violate the second restriction for a fee of $39$, thus the total profit is $328-39 = 289$. Note that even though there isn't a restriction on building $1$, we must still limit its height to be at most $10$.</p>
