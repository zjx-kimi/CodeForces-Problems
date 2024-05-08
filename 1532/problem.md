## Description

<div><p>While searching for the pizza, baby Hosssam came across two permutations $a$ and $b$ of length $n$.</p><p>Recall that a permutation is an array consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation ($2$ appears twice in the array) and $[1,3,4]$ is also not a permutation ($n=3$ but there is $4$ in the array).</p><p>Baby Hosssam forgot about the pizza and started playing around with the two permutations. While he was playing with them, some elements of the first permutation got mixed up with some elements of the second permutation, and to his surprise those elements also formed a permutation of size $n$.</p><p>Specifically, he mixed up the permutations to form a new array $c$ in the following way.</p><ul> <li> For each $i$ ($1\le i\le n$), he either made $c_i=a_i$ or $c_i=b_i$. </li><li> The array $c$ is a permutation. </li></ul><p>You know permutations $a$, $b$, and values at some positions in $c$. Please count the number different permutations $c$ that are consistent with the described process and the given values. Since the answer can be large, print it modulo $10^9+7$.</p><p>It is guaranteed that there exists at least one permutation $c$ that satisfies all the requirements.</p></div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \le t \le 10^5$) — the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1\le n\le 10^5$) — the length of the permutations.</p><p>The next line contains $n$ distinct integers $a_1,a_2,\ldots,a_n$ ($1\le a_i\le n$) — the first permutation.</p><p>The next line contains $n$ distinct integers $b_1,b_2,\ldots,b_n$ ($1\le b_i\le n$) — the second permutation.</p><p>The next line contains $n$ distinct integers $d_1,d_2,\ldots,d_n$ ($d_i$ is either $0$, $a_i$, or $b_i$) — the description of the known values of $c$. If $d_i=0$, then there are no requirements on the value of $c_i$. Otherwise, it is required that $c_i=d_i$.</p><p>It is guaranteed that there exists at least one permutation $c$ that satisfies all the requirements.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print the number of possible permutations $c$, modulo $10^9+7$.</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \le t \le 10^5$) — the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1\le n\le 10^5$) — the length of the permutations.</p><p>The next line contains $n$ distinct integers $a_1,a_2,\ldots,a_n$ ($1\le a_i\le n$) — the first permutation.</p><p>The next line contains $n$ distinct integers $b_1,b_2,\ldots,b_n$ ($1\le b_i\le n$) — the second permutation.</p><p>The next line contains $n$ distinct integers $d_1,d_2,\ldots,d_n$ ($d_i$ is either $0$, $a_i$, or $b_i$) — the description of the known values of $c$. If $d_i=0$, then there are no requirements on the value of $c_i$. Otherwise, it is required that $c_i=d_i$.</p><p>It is guaranteed that there exists at least one permutation $c$ that satisfies all the requirements.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5 \cdot 10^5$.</p>

## Output

<p>For each test case, print the number of possible permutations $c$, modulo $10^9+7$.</p>





```input1|2,3,4,5,10,11,12,13,18,19,20,21,26,27,28,29,34,35,36,37
9
7
1 2 3 4 5 6 7
2 3 1 7 6 5 4
2 0 1 0 0 0 0
1
1
1
0
6
1 5 2 4 6 3
6 5 3 1 4 2
6 0 0 0 0 0
8
1 6 4 7 2 3 8 5
3 2 8 1 4 5 6 7
1 0 0 7 0 3 0 5
10
1 8 6 2 4 7 9 3 10 5
1 9 2 3 4 10 8 6 7 5
1 9 2 3 4 10 8 6 7 5
7
1 2 3 4 5 6 7
2 3 1 7 6 5 4
0 0 0 0 0 0 0
5
1 2 3 4 5
1 2 3 4 5
0 0 0 0 0
5
1 2 3 4 5
1 2 3 5 4
0 0 0 0 0
3
1 2 3
3 1 2
0 0 0
```




```output1
4
1
2
2
1
8
1
2
2
```



## Note

<p>In the first test case, there are $4$ distinct permutation that can be made using the process: $[2,3,1,4,5,6,7]$, $[2,3,1,7,6,5,4]$, $[2,3,1,4,6,5,7]$, $[2,3,1,7,5,6,4]$.</p><p>In the second test case, there is only one distinct permutation that can be made using the process: $[1]$.</p><p>In the third test case, there are $2$ distinct permutation that can be made using the process: $[6,5,2,1,4,3]$, $[6,5,3,1,4,2]$.</p><p>In the fourth test case, there are $2$ distinct permutation that can be made using the process: $[1,2,8,7,4,3,6,5]$, $[1,6,4,7,2,3,8,5]$.</p><p>In the fifth test case, there is only one distinct permutation that can be made using the process: $[1,9,2,3,4,10,8,6,7,5]$.</p>
