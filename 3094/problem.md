## Description

<div><p>Johnny has a new toy. As you may guess, it is a little bit extraordinary. The toy is a permutation $P$ of numbers from $1$ to $n$, written in one row next to each other. </p><p>For each $i$ from $1$ to $n - 1$ between $P_i$ and $P_{i + 1}$ there is a weight $W_i$ written, and those weights form a permutation of numbers from $1$ to $n - 1$. There are also extra weights $W_0 = W_n = 0$.</p><p>The instruction defines subsegment $[L, R]$ as good if $W_{L - 1} &lt; W_i$ and $W_R &lt; W_i$ for any $i$ in $\{L, L + 1, \ldots, R - 1\}$. For such subsegment it also defines $W_M$ as minimum of set $\{W_L, W_{L + 1}, \ldots, W_{R - 1}\}$. </p><p>Now the fun begins. In one move, the player can choose one of the good subsegments, cut it into $[L, M]$ and $[M + 1, R]$ and swap the two parts. More precisely, before one move the chosen subsegment of our toy looks like: $$W_{L - 1}, P_L, W_L, \ldots, W_{M - 1}, P_M, W_M, P_{M + 1}, W_{M + 1}, \ldots, W_{R - 1}, P_R, W_R$$ and afterwards it looks like this: $$W_{L - 1}, P_{M + 1}, W_{M + 1}, \ldots, W_{R - 1}, P_R, W_M, P_L, W_L, \ldots, W_{M - 1}, P_M, W_R$$ Such a move can be performed multiple times (possibly zero), and the goal is to achieve the minimum number of inversions in $P$. </p><p>Johnny's younger sister Megan thinks that the rules are too complicated, so she wants to test her brother by choosing some pair of indices $X$ and $Y$, and swapping $P_X$ and $P_Y$ ($X$ might be equal $Y$). After each sister's swap, Johnny wonders, what is the minimal number of inversions that he can achieve, starting with current $P$ and making legal moves?</p><p>You can assume that the input is generated <span class="tex-font-style-bf">randomly</span>. $P$ and $W$ were chosen independently and equiprobably over all permutations; also, Megan's requests were chosen independently and equiprobably over all pairs of indices.</p></div><div class="input-specification"><p>The first line contains single integer $n$ $(2 \leq n \leq 2 \cdot 10^5)$ denoting the length of the toy.</p><p>The second line contains $n$ distinct integers $P_1, P_2, \ldots, P_n$ $(1 \leq P_i \leq n)$ denoting the initial permutation $P$. The third line contains $n - 1$ distinct integers $W_1, W_2, \ldots, W_{n - 1}$ $(1 \leq W_i \leq n - 1)$ denoting the weights.</p><p>The fourth line contains single integer $q$ $(1 \leq q \leq 5 \cdot 10^4)$&nbsp;— the number of Megan's swaps. The following $q$ lines contain two integers $X$ and $Y$ $(1 \leq X, Y \leq n)$&nbsp;— the indices of elements of $P$ to swap. The queries aren't independent; after each of them, the permutation is changed.</p></div><div class="output-specification"><p>Output $q$ lines. The $i$-th line should contain exactly one integer&nbsp;— the minimum number of inversions in permutation, which can be obtained by starting with the $P$ after first $i$ queries and making moves described in the game's instruction.</p></div>

## Input

<p>The first line contains single integer $n$ $(2 \leq n \leq 2 \cdot 10^5)$ denoting the length of the toy.</p><p>The second line contains $n$ distinct integers $P_1, P_2, \ldots, P_n$ $(1 \leq P_i \leq n)$ denoting the initial permutation $P$. The third line contains $n - 1$ distinct integers $W_1, W_2, \ldots, W_{n - 1}$ $(1 \leq W_i \leq n - 1)$ denoting the weights.</p><p>The fourth line contains single integer $q$ $(1 \leq q \leq 5 \cdot 10^4)$&nbsp;— the number of Megan's swaps. The following $q$ lines contain two integers $X$ and $Y$ $(1 \leq X, Y \leq n)$&nbsp;— the indices of elements of $P$ to swap. The queries aren't independent; after each of them, the permutation is changed.</p>

## Output

<p>Output $q$ lines. The $i$-th line should contain exactly one integer&nbsp;— the minimum number of inversions in permutation, which can be obtained by starting with the $P$ after first $i$ queries and making moves described in the game's instruction.</p>





```input1
3
3 2 1
2 1
3
1 3
3 2
3 1
```




```input2
5
4 3 2 5 1
3 2 1 4
7
5 4
5 2
1 5
2 4
2 4
4 3
3 3
```




```output1
0
1
0
```




```output2
3
1
2
1
2
3
3
```



## Note

<p>Consider the first sample. After the first query, $P$ is sorted, so we already achieved a permutation with no inversions. </p><p>After the second query, $P$ is equal to [$1$, $3$, $2$], it has one inversion, it can be proven that it is impossible to achieve $0$ inversions. </p><p>In the end, $P$ is equal to [$2$, $3$, $1$]; we can make a move on the whole permutation, as it is a good subsegment itself, which results in $P$ equal to [$1$, $2$, $3$], which has $0$ inversions.</p>
