## Description

<div><p>Arkady wants to water his only flower. Unfortunately, he has a very poor watering system that was designed for $n$ flowers and so it looks like a pipe with $n$ holes. Arkady can only use the water that flows from the first hole.</p><p>Arkady can block some of the holes, and then pour $A$ liters of water into the pipe. After that, the water will flow out from the non-blocked holes proportionally to their sizes $s_1, s_2, \ldots, s_n$. In other words, if the sum of sizes of non-blocked holes is $S$, and the $i$-th hole is not blocked, $\frac{s_i \cdot A}{S}$ liters of water will flow out of it.</p><p>What is the minimum number of holes Arkady should block to make at least $B$ liters of water flow out of the first hole?</p></div><div class="input-specification"><p>The first line contains three integers $n$, $A$, $B$ ($1 \le n \le 100\,000$, $1 \le B \le A \le 10^4$)&nbsp;— the number of holes, the volume of water Arkady will pour into the system, and the volume he wants to get out of the first hole.</p><p>The second line contains $n$ integers $s_1, s_2, \ldots, s_n$ ($1 \le s_i \le 10^4$)&nbsp;— the sizes of the holes.</p></div><div class="output-specification"><p>Print a single integer&nbsp;— the number of holes Arkady should block.</p></div>

## Input

<p>The first line contains three integers $n$, $A$, $B$ ($1 \le n \le 100\,000$, $1 \le B \le A \le 10^4$)&nbsp;— the number of holes, the volume of water Arkady will pour into the system, and the volume he wants to get out of the first hole.</p><p>The second line contains $n$ integers $s_1, s_2, \ldots, s_n$ ($1 \le s_i \le 10^4$)&nbsp;— the sizes of the holes.</p>

## Output

<p>Print a single integer&nbsp;— the number of holes Arkady should block.</p>





```input1
4 10 3
2 2 2 2

```




```input2
4 80 20
3 2 1 4

```




```input3
5 10 10
1000 1 1 1 1

```




```output1
1

```




```output2
0

```




```output3
4

```



## Note

<p>In the first example Arkady should block at least one hole. After that, $\frac{10 \cdot 2}{6} \approx 3.333$ liters of water will flow out of the first hole, and that suits Arkady.</p><p>In the second example even without blocking any hole, $\frac{80 \cdot 3}{10} = 24$ liters will flow out of the first hole, that is not less than $20$.</p><p>In the third example Arkady has to block all holes except the first to make all water flow out of the first hole.</p>
