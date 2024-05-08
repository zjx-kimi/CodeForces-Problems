## Description

<div><p>There are $n$ people, numbered from $1$ to $n$, sitting at a round table. Person $i+1$ is sitting to the right of person $i$ (with person $1$ sitting to the right of person $n$).</p><p>You have come up with a better seating arrangement, which is given as a permutation $p_1, p_2, \dots, p_n$. More specifically, you want to change the seats of the people so that at the end person $p_{i+1}$ is sitting to the right of person $p_i$ (with person $p_1$ sitting to the right of person $p_n$). Notice that for each seating arrangement there are $n$ permutations that describe it (which can be obtained by rotations).</p><p>In order to achieve that, you can swap two people sitting at adjacent places; but there is a catch: for all $1 \le x \le n-1$ you cannot swap person $x$ and person $x+1$ (notice that you <span class="tex-font-style-bf">can</span> swap person $n$ and person $1$). What is the minimum number of swaps necessary? It can be proven that any arrangement can be achieved.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains an integer $t$ ($1\le t\le 10\,000$) — the number of test cases. The descriptions of the $t$ test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($3 \le n \le 200\,000$) — the number of people sitting at the table. </p><p>The second line contains $n$ distinct integers $p_1, p_2, \dots, p_n$ ($1 \le p_i \le n$, $p_i \ne p_j$ for $i \ne j$) — the desired final order of the people around the table.</p><p>The sum of the values of $n$ over all test cases does not exceed $200\,000$.</p></div><div class="output-specification"><p>For each test case, print the minimum number of swaps necessary to achieve the desired order.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains an integer $t$ ($1\le t\le 10\,000$) — the number of test cases. The descriptions of the $t$ test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($3 \le n \le 200\,000$) — the number of people sitting at the table. </p><p>The second line contains $n$ distinct integers $p_1, p_2, \dots, p_n$ ($1 \le p_i \le n$, $p_i \ne p_j$ for $i \ne j$) — the desired final order of the people around the table.</p><p>The sum of the values of $n$ over all test cases does not exceed $200\,000$.</p>

## Output

<p>For each test case, print the minimum number of swaps necessary to achieve the desired order.</p>





```input1|2,3,6,7
3
4
2 3 1 4
5
5 4 3 2 1
7
4 1 6 5 3 7 2
```




```output1
1
10
22
```



## Note

<p>In the <span class="tex-font-style-bf">first test case</span>, we can swap person $4$ and person $1$ (who are adjacent) in the initial configuration and get the order $[4, 2, 3, 1]$ which is equivalent to the desired one. Hence in this case a single swap is sufficient.</p>
