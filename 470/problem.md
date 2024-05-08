## Description

<div><p>For a set of integers $S$, let's define its cost as the minimum value of $x \oplus y$ among all pairs of <span class="tex-font-style-bf">different</span> integers from the set (here, $\oplus$ denotes bitwise XOR). If there are less than two elements in the set, its cost is equal to $2^{30}$.</p><p>You are given a set of integers $\{a_1, a_2, \dots, a_n\}$. You have to partition it into two sets $S_1$ and $S_2$ in such a way that every element of the given set belongs to exactly one of these two sets. The value of the partition is the <span class="tex-font-style-bf">minimum</span> among the costs of $S_1$ and $S_2$.</p><p>Find the partition with the <span class="tex-font-style-bf">maximum</span> possible value.</p></div><div class="input-specification"><p>The first line contains $n$ ($2 \le n \le 200000$) — the number of elements in the set.</p><p>The second line contains $n$ <span class="tex-font-style-bf">distinct</span> integers $a_1$, $a_2$, ..., $a_n$ ($0 \le a_i &lt; 2^{30}$) — the elements of the set.</p></div><div class="output-specification"><p>Print a string $n$ characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span> describing the partition as follows: the $i$-th character should be <span class="tex-font-style-tt">0</span> if the element $a_i$ belongs to $S_1$, otherwise, that character should be <span class="tex-font-style-tt">1</span>.</p><p>If there are multiple optimal answers, print any of them.</p></div>

## Input

<p>The first line contains $n$ ($2 \le n \le 200000$) — the number of elements in the set.</p><p>The second line contains $n$ <span class="tex-font-style-bf">distinct</span> integers $a_1$, $a_2$, ..., $a_n$ ($0 \le a_i &lt; 2^{30}$) — the elements of the set.</p>

## Output

<p>Print a string $n$ characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span> describing the partition as follows: the $i$-th character should be <span class="tex-font-style-tt">0</span> if the element $a_i$ belongs to $S_1$, otherwise, that character should be <span class="tex-font-style-tt">1</span>.</p><p>If there are multiple optimal answers, print any of them.</p>





```input1
5
42 13 1337 37 152

```




```input2
4
1 2 3 4

```




```input3
2
1 2

```




```input4
8
7 6 5 4 3 2 1 0

```




```output1
10001

```




```output2
1100

```




```output3
10

```




```output4
10010110

```


