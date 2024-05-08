## Description

<div><p>Vanya really likes math. One day when he was solving another math problem, he came up with an interesting tree. This tree is built as follows.</p><p>Initially, the tree has only one vertex with the number $1$&nbsp;— the root of the tree. Then, Vanya adds two children to it, assigning them consecutive numbers&nbsp;— $2$ and $3$, respectively. After that, he will add children to the vertices in increasing order of their numbers, starting from $2$, assigning their children the minimum unused indices. As a result, Vanya will have an infinite tree with the root in the vertex $1$, where each vertex will have exactly two children, and the vertex numbers will be arranged sequentially by layers.</p><center> <img class="tex-graphics" src="file://mwN0hBU7.png" style="max-width: 100.0%;max-height: 100.0%;">   <span class="tex-font-size-small">Part of Vanya's tree.</span> </center><p>Vanya wondered what the sum of the vertex numbers on the path from the vertex with number $1$ to the vertex with number $n$ in such a tree is equal to. Since Vanya doesn't like counting, he asked you to help him find this sum.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>This is followed by $t$ lines&nbsp;— the description of the test cases. Each line contains one integer $n$ ($1 \le n \le 10^{16}$)&nbsp;— the number of vertex for which Vanya wants to count the sum of vertex numbers on the path from the root to that vertex.</p></div><div class="output-specification"><p>For each test case, print one integer&nbsp;— the desired sum.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>This is followed by $t$ lines&nbsp;— the description of the test cases. Each line contains one integer $n$ ($1 \le n \le 10^{16}$)&nbsp;— the number of vertex for which Vanya wants to count the sum of vertex numbers on the path from the root to that vertex.</p>

## Output

<p>For each test case, print one integer&nbsp;— the desired sum.</p>





```input1|2,4,6
6
3
10
37
1
10000000000000000
15
```




```output1
4
18
71
1
19999999999999980
26
```



## Note

<p>In the first test case of example on the path from the root to the vertex $3$ there are two vertices $1$ and $3$, their sum equals $4$.</p><p>In the second test case of example on the path from the root to the vertex with number $10$ there are vertices $1$, $2$, $5$, $10$, sum of their numbers equals $1+2+5+10 = 18$. </p>
