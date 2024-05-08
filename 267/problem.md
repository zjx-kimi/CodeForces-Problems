## Description

<div><p>Let's call an array $b_1, b_2, \ldots, b_m$ ($m \ge 2$) <span class="tex-font-style-it">good</span> if it can be split into two parts such that all elements in the left part are strictly smaller than all elements in the right part. In other words, there must exist an index $1 \le i &lt; m$ such that every element from $b_1, \ldots, b_i$ is strictly smaller than every element from $b_{i+1}, \ldots, b_m$.</p><p>Given an array $a_1, a_2, \ldots a_n$ consisting of <span class="tex-font-style-bf">distinct</span> integers from $1$ to $n$. There are $q$ queries. Each query consists of two numbers $l$ and $r$. For each query, determine whether the array $a_l, a_{l+1}, \ldots, a_r$ is good.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($2 \le n \le 3 \cdot 10^5$)&nbsp;— the size of the array.</p><p>The second line contains $n$ <span class="tex-font-style-bf">distinct</span> integers $a_1, a_2, \ldots, a_n$ ($1 \le a_n \le n$)&nbsp;— the elements of the array $a$.</p><p>The third line contains a single integer $q$ ($1 \le q \le 3 \cdot 10^5$)&nbsp;— the number of queries.</p><p>Each of the next $q$ lines contains two integers $l_i$ and $r_i$ ($1 \le l_i &lt; r_i \le n$)&nbsp;— the description of the $i$-th query.</p></div><div class="output-specification"><p>For each query, output "<span class="tex-font-style-tt">Yes</span>" (without quotes) if the array $a_l, a_{l+1}, \ldots, a_r$ is good, and "<span class="tex-font-style-tt">No</span>" (without quotes) otherwise.</p><p>You can output "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">No</span>" in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p></div>

## Input

<p>The first line contains a single integer $n$ ($2 \le n \le 3 \cdot 10^5$)&nbsp;— the size of the array.</p><p>The second line contains $n$ <span class="tex-font-style-bf">distinct</span> integers $a_1, a_2, \ldots, a_n$ ($1 \le a_n \le n$)&nbsp;— the elements of the array $a$.</p><p>The third line contains a single integer $q$ ($1 \le q \le 3 \cdot 10^5$)&nbsp;— the number of queries.</p><p>Each of the next $q$ lines contains two integers $l_i$ and $r_i$ ($1 \le l_i &lt; r_i \le n$)&nbsp;— the description of the $i$-th query.</p>

## Output

<p>For each query, output "<span class="tex-font-style-tt">Yes</span>" (without quotes) if the array $a_l, a_{l+1}, \ldots, a_r$ is good, and "<span class="tex-font-style-tt">No</span>" (without quotes) otherwise.</p><p>You can output "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">No</span>" in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p>





```input1
5
3 2 1 4 5
5
1 5
1 3
1 4
1 2
2 5
```




```input2
6
1 6 2 4 3 5
3
3 5
2 6
4 6
```




```output1
Yes
No
Yes
No
Yes
```




```output2
Yes
No
Yes
```



## Note

<p>In the first example:</p><ul><li> The array $[3,2,1,4,5]$ can be split into two parts: $[3,2,1]$ and $[4,5]$.</li><li> The array $[3,2,1]$ cannot be split into two parts such that all elements in the left part are smaller than all elements in the right part.</li><li> The array $[3,2,1,4]$ can be split into two parts: $[3,2,1]$ and $[4]$.</li><li> The array $[3,2]$ cannot be split into two parts such that all elements in the left part are smaller than all elements in the right part.</li><li> The array $[2,1,4,5]$ can be split into two parts: $[2,1]$ and $[4,5]$.</li></ul><p>In the second example:</p><ul><li> The array $[2,4,3]$ can be split into two parts: $[2]$ and $[4,3]$.</li><li> The array $[6,2,4,3,5]$ cannot be split into two parts such that all elements in the left part are smaller than all elements in the right part.</li><li> The array $[4,3,5]$ can be split into two parts: $[4,3]$ and $[5]$.</li></ul>
