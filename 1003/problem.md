## Description

<div><p>You are given five integers $n$, $i$, $j$, $x$, and $y$. Find the number of bitonic permutations $B$, of the numbers $1$ to $n$, such that $B_i=x$, and $B_j=y$. Since the answer can be large, compute it modulo $10^9+7$.</p><p>A bitonic permutation is a permutation of numbers, such that the elements of the permutation first increase till a certain index $k$, $2 \le k \le n-1$, and then decrease till the end. Refer to notes for further clarification.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 100$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The only line of each test case contains five integers, $n$, $i$, $j$, $x$, and $y$ ($3 \le n \le 100$ and $1 \le i,j,x,y \le n$). It is guaranteed that $i &lt; j$ and $x \ne y$.</p></div><div class="output-specification"><p>For each test case, output a single line containing the number of bitonic permutations satisfying the above conditions modulo $10^9+7$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 100$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The only line of each test case contains five integers, $n$, $i$, $j$, $x$, and $y$ ($3 \le n \le 100$ and $1 \le i,j,x,y \le n$). It is guaranteed that $i &lt; j$ and $x \ne y$.</p>

## Output

<p>For each test case, output a single line containing the number of bitonic permutations satisfying the above conditions modulo $10^9+7$.</p>





```input1|2,4,6,8
7
3 1 3 2 3
3 2 3 3 2
4 3 4 3 1
5 2 5 2 4
5 3 4 5 4
9 3 7 8 6
20 6 15 8 17
```




```output1
0
1
1
1
3
0
4788
```



## Note

<p>A permutation is an array consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation ($2$ appears twice in the array) and $[1,3,4]$ is also not a permutation ($n=3$ but there is $4$ in the array).</p><p>An array of $n \ge 3$ elements is bitonic if its elements are first increasing till an index $k$, $2 \le k \le n-1$, and then decreasing till the end. For example, $[2,5,8,6,1]$ is a bitonic array with $k=3$, but $[2,5,8,1,6]$ is not a bitonic array (elements first increase till $k=3$, then decrease, and then increase again).</p><p>A bitonic permutation is a permutation in which the elements follow the above-mentioned bitonic property. For example, $[2,3,5,4,1]$ is a bitonic permutation, but $[2,3,5,1,4]$ is not a bitonic permutation (since it is not a bitonic array) and $[2,3,4,4,1]$ is also not a bitonic permutation (since it is not a permutation).</p><p><span class="tex-font-style-bf">Sample Test Case Description</span></p><p>For $n=3$, possible permutations are $[1,2,3]$, $[1,3,2]$, $[2,1,3]$, $[2,3,1]$, $[3,1,2]$, and $[3,2,1]$. Among the given permutations, the bitonic permutations are $[1,3,2]$ and $[2,3,1]$.</p><p>In the first test case, the expected permutation must be of the form $[2,?,3]$, which does not satisfy either of the two bitonic permutations with $n=3$, therefore the answer is 0.</p><p>In the second test case, the expected permutation must be of the form $[?,3,2]$, which only satisfies the bitonic permutation $[1,3,2]$, therefore, the answer is 1.</p>
