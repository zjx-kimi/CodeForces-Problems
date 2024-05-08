## Description

<div><p>You are given a permutation $p$ of length $n$&nbsp;— an array, consisting of integers from $1$ to $n$, all distinct.</p><p>Let $p_{l,r}$ denote a subarray&nbsp;— an array formed by writing down elements from index $l$ to index $r$, inclusive.</p><p>Let $\mathit{maxpos}_{l,r}$ denote the <span class="tex-font-style-bf">index</span> of the maximum element on $p_{l,r}$. Similarly, let $\mathit{minpos}_{l,r}$ denote the index of the minimum element on it.</p><p>Calculate the number of subarrays $p_{l,r}$ such that $\mathit{maxpos}_{l,r} &gt; \mathit{minpos}_{l,r}$.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($1 \le n \le 10^6$)&nbsp;— the number of elements in the permutation.</p><p>The second line contains $n$ integers $p_1, p_2, \dots, p_n$ ($1 \le p_i \le n$). All $p_i$ are distinct.</p></div><div class="output-specification"><p>Print a single integer&nbsp;— the number of subarrays $p_{l,r}$ such that $\mathit{maxpos}_{l,r} &gt; \mathit{minpos}_{l,r}$.</p></div>

## Input

<p>The first line contains a single integer $n$ ($1 \le n \le 10^6$)&nbsp;— the number of elements in the permutation.</p><p>The second line contains $n$ integers $p_1, p_2, \dots, p_n$ ($1 \le p_i \le n$). All $p_i$ are distinct.</p>

## Output

<p>Print a single integer&nbsp;— the number of subarrays $p_{l,r}$ such that $\mathit{maxpos}_{l,r} &gt; \mathit{minpos}_{l,r}$.</p>





```input1
3
1 2 3
```




```input2
6
5 3 6 1 4 2
```




```input3
10
5 1 6 2 8 3 4 10 9 7
```




```output1
3
```




```output2
4
```




```output3
38
```


