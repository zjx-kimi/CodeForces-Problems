## Description

<div><p>Pavel has several sticks with lengths equal to powers of two.</p><p>He has $a_0$ sticks of length $2^0 = 1$, $a_1$ sticks of length $2^1 = 2$, ..., $a_{n-1}$ sticks of length $2^{n-1}$. </p><p>Pavel wants to make the maximum possible number of triangles using these sticks. The triangles should have strictly positive area, each stick can be used in at most one triangle.</p><p>It is forbidden to break sticks, and each triangle should consist of exactly three sticks.</p><p>Find the maximum possible number of triangles.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($1 \leq n \leq 300\,000$)&nbsp;— the number of different lengths of sticks.</p><p>The second line contains $n$ integers $a_0$, $a_1$, ..., $a_{n-1}$ ($1 \leq a_i \leq 10^9$), where $a_i$ is the number of sticks with the length equal to $2^i$.</p></div><div class="output-specification"><p>Print a single integer&nbsp;— the maximum possible number of non-degenerate triangles that Pavel can make.</p></div>

## Input

<p>The first line contains a single integer $n$ ($1 \leq n \leq 300\,000$)&nbsp;— the number of different lengths of sticks.</p><p>The second line contains $n$ integers $a_0$, $a_1$, ..., $a_{n-1}$ ($1 \leq a_i \leq 10^9$), where $a_i$ is the number of sticks with the length equal to $2^i$.</p>

## Output

<p>Print a single integer&nbsp;— the maximum possible number of non-degenerate triangles that Pavel can make.</p>





```input1
5
1 2 2 2 2
```




```input2
3
1 1 1
```




```input3
3
3 3 3
```




```output1
3
```




```output2
0
```




```output3
3
```



## Note

<p>In the first example, Pavel can, for example, make this set of triangles (the lengths of the sides of the triangles are listed): $(2^0, 2^4, 2^4)$, $(2^1, 2^3, 2^3)$, $(2^1, 2^2, 2^2)$.</p><p>In the second example, Pavel cannot make a single triangle.</p><p>In the third example, Pavel can, for example, create this set of triangles (the lengths of the sides of the triangles are listed): $(2^0, 2^0, 2^0)$, $(2^1, 2^1, 2^1)$, $(2^2, 2^2, 2^2)$.</p>
