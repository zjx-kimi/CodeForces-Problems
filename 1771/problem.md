## Description

<div><p>There are $n$ heaps of stone. The $i$-th heap has $h_i$ stones. You want to change the number of stones in the heap by performing the following process once: </p><ul> <li> You go through the heaps from the $3$-rd heap to the $n$-th heap, in this order. </li><li> Let $i$ be the number of the current heap. </li><li> You can choose a number $d$ ($0 \le 3 \cdot d \le h_i$), move $d$ stones from the $i$-th heap to the $(i - 1)$-th heap, and $2 \cdot d$ stones from the $i$-th heap to the $(i - 2)$-th heap. </li><li> So after that $h_i$ is decreased by $3 \cdot d$, $h_{i - 1}$ is increased by $d$, and $h_{i - 2}$ is increased by $2 \cdot d$. </li><li> You can choose different or same $d$ for different operations. Some heaps may become empty, but they still count as heaps. </li></ul><p>What is the maximum number of stones in the smallest heap after the process?</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 2\cdot 10^5$). Description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($3 \le n \le 2 \cdot 10^5$).</p><p>The second lines of each test case contains $n$ integers $h_1, h_2, h_3, \ldots, h_n$ ($1 \le h_i \le 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print the maximum number of stones that the smallest heap can contain.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 2\cdot 10^5$). Description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($3 \le n \le 2 \cdot 10^5$).</p><p>The second lines of each test case contains $n$ integers $h_1, h_2, h_3, \ldots, h_n$ ($1 \le h_i \le 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, print the maximum number of stones that the smallest heap can contain.</p>





```input1
4
4
1 2 10 100
4
100 100 100 1
5
5 1 1 1 8
6
1 2 3 4 5 6
```




```output1
7
1
1
3
```



## Note

<p>In the first test case, the initial heap sizes are $[1, 2, 10, 100]$. We can move the stones as follows. </p><ul> <li> move $3$ stones and $6$ from the $3$-rd heap to the $2$-nd and $1$ heap respectively. The heap sizes will be $[7, 5, 1, 100]$; </li><li> move $6$ stones and $12$ stones from the last heap to the $3$-rd and $2$-nd heap respectively. The heap sizes will be $[7, 17, 7, 82]$. </li></ul><p>In the second test case, the last heap is $1$, and we can not increase its size.</p><p>In the third test case, it is better not to move any stones.</p><p>In the last test case, the final achievable configuration of the heaps can be $[3, 5, 3, 4, 3, 3]$.</p>
