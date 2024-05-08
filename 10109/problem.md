## Description

<div><p>Anton got bored during the hike and wanted to solve something. He asked Kirill if he had any new problems, and of course, Kirill had one.</p><p>You are given a permutation $p$ of size $n$, and a number $x$ that needs to be found. A permutation of length $n$ is an array consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation ($2$ appears twice in the array), and $[1,3,4]$ is also not a permutation ($n=3$ but there is $4$ in the array).</p><p>You decided that you are a cool programmer, so you will use an advanced algorithm for the search — binary search. However, you forgot that for binary search, the array must be sorted.</p><p>You did not give up and decided to apply this algorithm anyway, and in order to get the correct answer, you can perform the following operation <span class="tex-font-style-bf">no more than</span> $2$ times before running the algorithm: choose the indices $i$, $j$ ($1\le i, j \le n$) and swap the elements at positions $i$ and $j$.</p><p>After that, the binary search is performed. At the beginning of the algorithm, two variables $l = 1$ and $r = n + 1$ are declared. Then the following loop is executed:</p><ol> <li> If $r - l = 1$, end the loop </li><li> $m = \lfloor \frac{r + l}{2} \rfloor$ </li><li> If $p_m \le x$, assign $l = m$, otherwise $r = m$. </li></ol><p>The goal is to rearrange the numbers in the permutation before the algorithm so that after the algorithm is executed, $p_l$ is equal to $x$. It can be shown that $2$ operations are always sufficient.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 2\cdot 10^4$) — the number of test cases. Then follow the descriptions of the test cases.</p><p>The first line of each test case contains two integers $n$ and $x$ ($1 \le x \le n \le 2\cdot 10^5$) — the length of the permutation and the number to be found.</p><p>The second line contains the permutation $p$ separated by spaces ($1 \le p_i \le n$).</p><p>It is guaranteed that the sum of the values of $n$ for all test cases does not exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output an integer $k$ ($0 \le k \le 2$) on the first line — the number of operations performed by you. In the next $k$ lines, output $2$ integers $i$, $j$ ($1 \le i, j \le n$) separated by a space, indicating that you are swapping the elements at positions $i$ and $j$.</p><p>Note that you do not need to minimize the number of operations.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 2\cdot 10^4$) — the number of test cases. Then follow the descriptions of the test cases.</p><p>The first line of each test case contains two integers $n$ and $x$ ($1 \le x \le n \le 2\cdot 10^5$) — the length of the permutation and the number to be found.</p><p>The second line contains the permutation $p$ separated by spaces ($1 \le p_i \le n$).</p><p>It is guaranteed that the sum of the values of $n$ for all test cases does not exceed $2\cdot 10^5$.</p>

## Output

<p>For each test case, output an integer $k$ ($0 \le k \le 2$) on the first line — the number of operations performed by you. In the next $k$ lines, output $2$ integers $i$, $j$ ($1 \le i, j \le n$) separated by a space, indicating that you are swapping the elements at positions $i$ and $j$.</p><p>Note that you do not need to minimize the number of operations.</p>





```input1|2,3,6,7,10,11
5
6 3
1 2 3 4 5 6
6 5
3 1 6 5 2 4
5 1
3 5 4 2 1
6 3
4 3 1 5 2 6
3 2
3 2 1
```




```output1
0
1
3 4
2
2 4
1 5
2
4 5
2 4
1
1 3
```


