## Description

<div><p><span class="tex-font-style-bf">This is the easy version of the problem. The difference between the two versions is that you do not have to minimize the number of operations in this version. You can make hacks only if both versions of the problem are solved.</span></p><p>You have two permutations$^{\dagger}$ $p_{1}, p_{2}, \ldots, p_{n}$ (of integers $1$ to $n$) and $q_{1}, q_{2}, \ldots, q_{m}$ (of integers $1$ to $m$). Initially $p_{i}=a_{i}$ for $i=1, 2, \ldots, n$, and $q_{j} = b_{j}$ for $j = 1, 2, \ldots, m$. You can apply the following operation on the permutations several (possibly, zero) times.</p><p>In one operation, $p$ and $q$ will change according to the following three steps:</p><ul> <li> You choose integers $i$, $j$ which satisfy $1 \le i \le n$ and $1 \le j \le m$. </li><li> Permutation $p$ is partitioned into three parts using $p_i$ as a pivot: the left part is formed by elements $p_1, p_2, \ldots, p_{i-1}$ (this part may be empty), the middle part is the single element $p_i$, and the right part is $p_{i+1}, p_{i+2}, \ldots, p_n$ (this part may be empty). To proceed, swap the left and the right parts of this partition. Formally, after this step, $p$ will become $p_{i+1}, p_{i+2}, \ldots, p_{n}, p_{i}, p_{1}, p_{2}, \ldots, p_{i-1}$. The elements of the newly formed $p$ will be reindexed starting from $1$. </li><li> Perform the same transformation on $q$ with index $j$. Formally, after this step, $q$ will become $q_{j+1}, q_{j+2}, \ldots, q_{m}, q_{j}, q_{1}, q_{2}, \ldots, q_{j-1}$. The elements of the newly formed $q$ will be reindexed starting from $1$. </li></ul><p>Your goal is to simultaneously make $p_{i}=i$ for $i=1, 2, \ldots, n$, and $q_{j} = j$ for $j = 1, 2, \ldots, m$.</p><p>Find any valid way to achieve the goal using at most $10\,000$ operations, or say that none exists. Please note that you <span class="tex-font-style-bf">do not have to</span> minimize the number of operations.</p><p>It can be proved that if it is possible to achieve the goal, then there exists a way to do so using at most $10\,000$ operations.</p><p>$^{\dagger}$ A permutation of length $k$ is an array consisting of $k$ distinct integers from $1$ to $k$ in arbitrary order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation ($2$ appears twice in the array), and $[1,3,4]$ is also not a permutation ($k=3$ but there is $4$ in the array).</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $m$ ($1 \le n, m \le 2500$).</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le n$).</p><p>The third line contains $m$ integers $b_1, b_2, \ldots, b_m$ ($1 \le b_i \le m$).</p><p>It is guaranteed that $a$ and $b$ are permutations.</p></div><div class="output-specification"><p>If there is no solution, print a single integer $-1$.</p><p>Otherwise, print an integer $k$ ($0 \le k \le 10\,000$)&nbsp;— the number of operations to perform, followed by $k$ lines, each containing two integers $i$ and $j$ ($1 \le i \le n$, $1 \le j \le m$)&nbsp;— the integers chosen for the operation.</p><p>If there are multiple solutions, print any of them.</p><p>Please note that you <span class="tex-font-style-bf">do not have to</span> minimize the number of operations.</p></div>

## Input

<p>The first line contains two integers $n$ and $m$ ($1 \le n, m \le 2500$).</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le n$).</p><p>The third line contains $m$ integers $b_1, b_2, \ldots, b_m$ ($1 \le b_i \le m$).</p><p>It is guaranteed that $a$ and $b$ are permutations.</p>

## Output

<p>If there is no solution, print a single integer $-1$.</p><p>Otherwise, print an integer $k$ ($0 \le k \le 10\,000$)&nbsp;— the number of operations to perform, followed by $k$ lines, each containing two integers $i$ and $j$ ($1 \le i \le n$, $1 \le j \le m$)&nbsp;— the integers chosen for the operation.</p><p>If there are multiple solutions, print any of them.</p><p>Please note that you <span class="tex-font-style-bf">do not have to</span> minimize the number of operations.</p>





```input1
3 5
2 1 3
5 2 1 4 3
```




```input2
4 4
3 4 2 1
2 4 1 3
```




```input3
2 2
1 2
2 1
```




```output1
2
3 4
2 4
```




```output2
5
4 2
3 3
1 4
3 2
4 1
```




```output3
-1
```



## Note

<p>In the first example, we can achieve the goal within $2$ operations: </p><ol> <li> In the first operation, choose $i = 3$, $j = 4$. After this, $p$ becomes $[3, 2, 1]$ and $q$ becomes $[3, 4, 5, 2, 1]$. </li><li> In the second operation, choose $i = 2$, $j = 4$. After this, $p$ becomes $[1, 2, 3]$ and $q$ becomes $[1, 2, 3, 4, 5]$. </li></ol><p>In the third example, it is impossible to achieve the goal.</p>
