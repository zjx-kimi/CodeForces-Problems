## Description

<div><p>Let's recall that an increasing subsequence of the array $a$ is a sequence that can be obtained from it by removing some elements without changing the order of the remaining elements, and the remaining elements are strictly increasing (i. e $a_{b_1} &lt; a_{b_2} &lt; \dots &lt; a_{b_k}$ and $b_1 &lt; b_2 &lt; \dots &lt; b_k$). Note that an empty subsequence is also increasing.</p><p>You are given a positive integer $X$. Your task is to find an array of integers of length <span class="tex-font-style-bf">at most $200$</span>, such that it has exactly $X$ increasing subsequences, or report that there is no such array. If there are several answers, you can print any of them.</p><p>If two subsequences consist of the same elements, but correspond to different positions in the array, they are considered different (for example, the array $[2, 2]$ has two different subsequences equal to $[2]$).</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains a single integer $X$ ($2 \le X \le 10^{18}$).</p></div><div class="output-specification"><p>For each query, print the answer to it. If it is impossible to find the required array, print <span class="tex-font-style-tt">-1</span> on the first line. Otherwise, print a positive integer $n$ on the first line&nbsp;— the length of the array. On the second line, print $n$ integers&nbsp;— the required array itself. If there are several answers, you can print any of them. All elements of the array should be in the range $[-10^9; 10^9]$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains a single integer $X$ ($2 \le X \le 10^{18}$).</p>

## Output

<p>For each query, print the answer to it. If it is impossible to find the required array, print <span class="tex-font-style-tt">-1</span> on the first line. Otherwise, print a positive integer $n$ on the first line&nbsp;— the length of the array. On the second line, print $n$ integers&nbsp;— the required array itself. If there are several answers, you can print any of them. All elements of the array should be in the range $[-10^9; 10^9]$.</p>





```input1|2,4
4
2
5
13
37
```




```output1
1
0
3
0 1 0
5
2 2 3 4 2
7
-1 -1 0 0 2 3 -1
```


