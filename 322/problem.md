## Description

<div><p>Chaneka has an array $[a_1,a_2,\ldots,a_n]$. Initially, all elements are white. Chaneka will choose one or more different indices and colour the elements at those chosen indices black. Then, she will choose all white elements whose indices are multiples of the index of <span class="tex-font-style-bf">at least one</span> black element and colour those elements green. After that, her score is the <span class="tex-font-style-bf">maximum</span> value of $a_i$ out of all black and green elements.</p><p>There are $2^n-1$ ways for Chaneka to choose the black indices. Find the sum of scores for all possible ways Chaneka can choose the black indices. Since the answer can be very big, print the answer modulo $998\,244\,353$.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($1 \leq n \leq 10^5$) — the size of array $a$.</p><p>The second line contains $n$ integers $a_1,a_2,a_3,\ldots,a_n$ ($0\leq a_i\leq10^5$).</p></div><div class="output-specification"><p>An integer representing the sum of scores for all possible ways Chaneka can choose the black indices, modulo $998\,244\,353$.</p></div>

## Input

<p>The first line contains a single integer $n$ ($1 \leq n \leq 10^5$) — the size of array $a$.</p><p>The second line contains $n$ integers $a_1,a_2,a_3,\ldots,a_n$ ($0\leq a_i\leq10^5$).</p>

## Output

<p>An integer representing the sum of scores for all possible ways Chaneka can choose the black indices, modulo $998\,244\,353$.</p>





```input1
4
19 14 19 9
```




```input2
1
0
```




```input3
15
90000 9000 99000 900 90900 9900 99900 90 90090 9090 99090 990 90990 9990 99990
```




```output1
265
```




```output2
0
```




```output3
266012571
```



## Note

<p>In the first example, below are the $15$ possible ways to choose the black indices: </p><ul> <li> Index $1$ is black. Indices $2$, $3$, and $4$ are green. Maximum value among them is $19$. </li><li> Index $2$ is black. Index $4$ is green. Maximum value among them is $14$. </li><li> Index $3$ is black. Maximum value among them is $19$. </li><li> Index $4$ is black. Maximum value among them is $9$. </li><li> Indices $1$ and $2$ are black. Indices $3$ and $4$ are green. Maximum value among them is $19$. </li><li> Indices $1$ and $3$ are black. Indices $2$ and $4$ are green. Maximum value among them is $19$. </li><li> Indices $1$ and $4$ are black. Indices $2$ and $3$ are green. Maximum value among them is $19$. </li><li> Indices $2$ and $3$ are black. Index $4$ is green. Maximum value among them is $19$. </li><li> Indices $2$ and $4$ are black. Maximum value among them is $14$. </li><li> Indices $3$ and $4$ are black. Maximum value among them is $19$. </li><li> Indices $1$, $2$, and $3$ are black. Index $4$ is green. Maximum value among them is $19$. </li><li> Indices $1$, $2$, and $4$ are black. Index $3$ is green. Maximum value among them is $19$. </li><li> Indices $1$, $3$, and $4$ are black. Index $2$ is green. Maximum value among them is $19$. </li><li> Indices $2$, $3$, and $4$ are black. Maximum value among them is $19$. </li><li> Indices $1$, $2$, $3$, and $4$ are black. Maximum value among them is $19$. </li></ul><p>The total sum is $19+14+19+9+19+19+19+19+14+19+19+19+19+19+19 = 265$.</p>
