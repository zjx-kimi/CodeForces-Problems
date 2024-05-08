## Description

<div><p>Consider a permutation $p_1, p_2, \dots p_n$ of integers from 1 to $n$. We call a sub-segment $p_l, p_{l+1}, \dots, p_{r-1}, p_{r}$ of the permutation an <span class="tex-font-style-underline">interval</span> if it is a reordering of some set of consecutive integers. For example, the permutation $(6,7,1,8,5,3,2,4)$ has the intervals $(6,7)$, $(5,3,2,4)$, $(3,2)$, and others. </p><p>Each permutation has some trivial intervals&nbsp;— the full permutation itself and every single element. We call a permutation <span class="tex-font-style-underline">interval-free</span> if it does not have non-trivial intervals. In other words, interval-free permutation does not have intervals of length between 2 and $n - 1$ inclusive. </p><p>Your task is to count the number of interval-free permutations of length $n$ modulo prime number $p$. </p></div><div class="input-specification"><p>In the first line of the input there are two integers $t$ ($1 \le t \le 400$) and $p$ ($10^8 \le p \le 10^9$)&nbsp;— the number of test cases to solve and the prime modulo. In each of the next $t$ lines there is one integer $n$ ($1 \le n \le 400$)&nbsp;— the length of the permutation. </p></div><div class="output-specification"><p>For each of $t$ test cases print a single integer&nbsp;— the number of interval-free permutations modulo $p$. </p></div>

## Input

<p>In the first line of the input there are two integers $t$ ($1 \le t \le 400$) and $p$ ($10^8 \le p \le 10^9$)&nbsp;— the number of test cases to solve and the prime modulo. In each of the next $t$ lines there is one integer $n$ ($1 \le n \le 400$)&nbsp;— the length of the permutation. </p>

## Output

<p>For each of $t$ test cases print a single integer&nbsp;— the number of interval-free permutations modulo $p$. </p>





```input1
4 998244353
1
4
5
9
```




```input2
1 437122297
20
```




```output1
1
2
6
28146
```




```output2
67777575
```



## Note

<p>For $n = 1$ the only permutation is interval-free. For $n = 4$ two interval-free permutations are $(2,4,1,3)$ and $(3,1,4,2)$. For $n = 5$ — $(2,4,1,5,3)$, $(2,5,3,1,4)$, $(3,1,5,2,4)$, $(3,5,1,4,2)$, $(4,1,3,5,2)$, and $(4,2,5,1,3)$. We will not list all 28146 for $n = 9$, but for example $(4,7,9,5,1,8,2,6,3)$, $(2,4,6,1,9,7,3,8,5)$, $(3,6,9,4,1,5,8,2,7)$, and $(8,4,9,1,3,6,2,7,5)$ are interval-free.</p><p>The exact value for $n = 20$ is 264111424634864638. </p>
