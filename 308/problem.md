## Description

<div><p>After (finally) qualifying for the IOI 2023, wxhtzdy was very happy, so he decided to do what most competitive programmers do: trying to guess the problems that will be on IOI. During this process, he accidentally made a problem, which he thought was really cool.</p><p>You are given a tree (a connected acyclic graph) with $n$ vertices and $n-1$ edges. Vertex $i$ ($1 \le i \le n$) has a value $a_i$. </p><p>Lets' define $g(u, v)$ as the <a href="http://tiny.cc/bitwise_or">bitwise or</a> of the values of all vertices on the shortest path from $u$ to $v$. For example, let's say that we want to calculate $g(3, 4)$, on the tree from the first test case in the example. On the path from $3$ to $4$ are vertices $3$, $1$, $4$. Then, $g(3, 4) = a_3 \ | \ a_1 \ | \ a_4$ (here, $|$ represents the <a href="http://tiny.cc/bitwise_or">bitwise OR operation</a>).</p><p>Also, you are given $q$ queries, and each query looks like this:</p><p>You are given $x$ and $y$. Let's consider all vertices $z$ such that $z$ is on the shortest path from $x$ to $y$ (inclusive).</p><p>Lets define the <span class="tex-font-style-it">niceness</span> of a vertex $z$ as the sum of the number of non-zero bits in $g(x, z)$ and the number of non-zero bits in $g(y, z)$. You need to find the maximum <span class="tex-font-style-it">niceness</span> among all vertices $z$ on the shortest path from $x$ to $y$.</p><p>Since his brain is really tired after solving an output only problem on SIO (he had to do it to qualify for the IOI), he wants your help with this problem.</p></div><div class="input-specification"><p>The first line of input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of vertices.</p><p>The second line of each test case contains $n$ positive integers $a_1, a_2, \dots, a_n$ ($1 \le a_v \le 10^9$)&nbsp;— the value of each vertex, the $i$-th integer in this line corresponds to the vertex $i$.</p><p>Following $n - 1$ lines are the description of a tree.</p><p>Each line contains two integers $u$ and $v$ ($1 \le u, v \le n, u \ne v$)&nbsp;— indicating that vertices $u$ and $v$ are connected by an edge.</p><p>The next line contains a single integer $q$ ($1 \le q \le 10^5$)&nbsp;— number of queries.</p><p>Following $q$ lines contain 2 integers $x, y$ ($1 \le x, y \le n$)&nbsp;— the vertices $x$ and $y$ for each query.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p><p>It is guaranteed that the sum of $q$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case output $q$ integers, each of which is the answer to the corresponding query.</p></div>

## Input

<p>The first line of input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of vertices.</p><p>The second line of each test case contains $n$ positive integers $a_1, a_2, \dots, a_n$ ($1 \le a_v \le 10^9$)&nbsp;— the value of each vertex, the $i$-th integer in this line corresponds to the vertex $i$.</p><p>Following $n - 1$ lines are the description of a tree.</p><p>Each line contains two integers $u$ and $v$ ($1 \le u, v \le n, u \ne v$)&nbsp;— indicating that vertices $u$ and $v$ are connected by an edge.</p><p>The next line contains a single integer $q$ ($1 \le q \le 10^5$)&nbsp;— number of queries.</p><p>Following $q$ lines contain 2 integers $x, y$ ($1 \le x, y \le n$)&nbsp;— the vertices $x$ and $y$ for each query.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p><p>It is guaranteed that the sum of $q$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case output $q$ integers, each of which is the answer to the corresponding query.</p>





```input1|2,3,4,5,6,7,8,9,10,20,21,22,23
3
4
1 2 3 4
1 3
1 2
1 4
3
1 1
1 3
1 4
3
7 6 3
3 1
2 1
4
1 1
1 2
1 3
2 3
1
4
1
1 1
```




```input2|2,3,4,5,6,7,8,9,10,11,12,13,14,27,28,29,30,31,32,33,34,35,36,37
3
7
4 7 7 4 10 8 10
6 1
3 1
2 1
7 4
1 5
4 2
4
7 5
2 3
4 5
2 5
6
9 5 6 2 4 6
5 1
2 1
1 6
4 3
1 3
4
6 1
1 4
4 3
3 5
7
5 1 3 7 5 1 6
2 1
5 4
2 3
3 4
7 6
6 3
2
4 2
7 7
```




```input3|2,3,4,5,6,7,8,9,10,11,12,13,14
1
7
6 8 7 2 5 8 7
2 1
3 2
4 3
4 6
4 5
6 7
4
1 5
6 7
4 5
1 4
```




```output1
2 4 3 
6 6 6 6 
2
```




```output2
8 6 7 7 
6 6 4 7 
6 4
```




```output3
7 7 5 7
```



## Note

<p>The image below shows the tree from the second example, first test case. </p><center> <img class="tex-graphics" src="file://yEqqaPkD.png" style="max-width: 100.0%;max-height: 100.0%;">   <span class="tex-font-size-small">Tree from the second example, first test case</span> </center><p>In the <span class="tex-font-style-bf">first query</span>, we have $x=7$, $y=5$. The shortest path from $7$ to $5$ is $7-4-2-1-5$. </p><p>Let's calculate the <span class="tex-font-style-it">niceness</span> of vertex $7$ on this path. We have $g(7,7)=a_7=10=(1010)_2$ and $g(5,7)=a_5 \ | \ a_1 \ | \ a_2 \ | \ a_4 \ | \ a_7=10 \ | \ 4 \ | \ 7 \ | \ 4 \ | \ 10=15=(1111)_2$, so its <span class="tex-font-style-it">niceness</span> is equal to $2 + 4 = 6$.</p><p>Now let's calculate the <span class="tex-font-style-it">niceness</span> of vertex $4$ on this path. We have $g(7,4)=a_7 \ | \ a_4=10 \ | \ 4=14=(1110)_2$ and $g(5,4)=a_5 \ | \ a_1 \ | \ a_2 \ | \ a_4=10 \ | \ 4 \ | \ 7 \ | \ 4=15=(1111)_2$, so its <span class="tex-font-style-it">niceness</span> is equal to $3 + 4 = 7$.</p><p>Now let's calculate the <span class="tex-font-style-it">niceness</span> of vertex $2$ on this path. We have $g(7,2)=a_7 \ | \ a_4 \ | \ a_2=10 \ | \ 4 \ | \ 7=15=(1111)_2$ and $g(5,2)=a_5 \ | \ a_1 \ | \ a_2=10 \ | \ 4 \ | \ 7=15=(1111)_2$, so its <span class="tex-font-style-it">niceness</span> is equal to $4 + 4 = 8$.</p><p>Now let's calculate the <span class="tex-font-style-it">niceness</span> of vertex $1$ on this path. We have $g(7,1)=a_7 \ | \ a_4 \ | \ a_2 \ | \ a_1=10 \ | \ 4 \ | \ 7 \ | \ 4=15=(1111)_2$ and $g(5,1)=a_5 \ | \ a_1=10 \ | \ 4=14=(1110)_2$, so its <span class="tex-font-style-it">niceness</span> is equal to $4 + 3 = 7$.</p><p>Finally, let's calculate the <span class="tex-font-style-it">niceness</span> of vertex $5$ on this path. We have $g(7,5)=a_7 \ | \ a_4 \ | \ a_2 \ | \ a_1 \ | \ a_5=10 \ | \ 4 \ | \ 7 \ | \ 4 \ | \ 10=15=(1111)_2$ and $g(5,5)=a_5=10=(1010)_2$, so its <span class="tex-font-style-it">niceness</span> is equal to $4 + 2 = 6$.</p><p>The maximum <span class="tex-font-style-it">niceness</span> on this path is at vertex $2$, and it is $8$.</p>
