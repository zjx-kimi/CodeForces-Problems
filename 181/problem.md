## Description

<div><p>You are given a tree consisting of $n$ vertices. A number is written on each vertex; the number on vertex $i$ is equal to $a_i$.</p><p>You can perform the following operation any number of times (possibly zero): </p><ul> <li> choose a vertex which has <span class="tex-font-style-bf">at most $1$</span> incident edge and remove this vertex from the tree. </li></ul><p>Note that you can delete all vertices.</p><p>After all operations are done, you're compressing the tree. The compression process is done as follows. While there is a vertex having <span class="tex-font-style-bf">exactly $2$</span> incident edges in the tree, perform the following operation: </p><ul> <li> delete this vertex, connect its neighbors with an edge. </li></ul><p>It can be shown that if there are multiple ways to choose a vertex to delete during the compression process, the resulting tree is still the same.</p><p>Your task is to calculate the maximum possible sum of numbers written on vertices after applying the aforementioned operation any number of times, and then compressing the tree.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 5 \cdot 10^5$)&nbsp;— the number of vertices.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($-10^9 \le a_i \le 10^9$).</p><p>Each of the next $n - 1$ lines describes an edge of the tree. Edge $i$ is denoted by two integers $v_i$ and $u_i$, the labels of vertices it connects ($1 \le v_i, u_i \le n$, $v_i \ne u_i$). These edges form a tree. </p><p>Additional constraint on the input: the sum of $n$ over all test cases doesn't exceed $5 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print a single integer&nbsp;— the maximum possible sum of numbers written on vertices after applying the aforementioned operation any number of times, and then compressing the tree.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 5 \cdot 10^5$)&nbsp;— the number of vertices.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($-10^9 \le a_i \le 10^9$).</p><p>Each of the next $n - 1$ lines describes an edge of the tree. Edge $i$ is denoted by two integers $v_i$ and $u_i$, the labels of vertices it connects ($1 \le v_i, u_i \le n$, $v_i \ne u_i$). These edges form a tree. </p><p>Additional constraint on the input: the sum of $n$ over all test cases doesn't exceed $5 \cdot 10^5$.</p>

## Output

<p>For each test case, print a single integer&nbsp;— the maximum possible sum of numbers written on vertices after applying the aforementioned operation any number of times, and then compressing the tree.</p>





```input1|2,3,4,5,6,10,11,12,13,14,15,16,17
3
4
1 -2 2 1
1 2
3 2
2 4
2
-2 -5
2 1
7
-2 4 -2 3 3 2 -1
1 2
2 3
3 4
3 5
4 6
4 7
```




```output1
3
0
9
```


