## Description

<div><p>You have $n$ colored cubes, the $i$-th cube has color $a_i$.</p><p>You need to distribute all the cubes on shelves. There are a total of $m$ shelves, the $i$-th shelf can hold $s_i$ cubes. Also, $s_1 + s_2 + \ldots + s_m = n$.</p><p>Suppose on a shelf of size $k$ there are cubes of colors $c_1, c_2, \ldots, c_k$, <span class="tex-font-style-bf">in this order</span>. Then we define the <span class="tex-font-style-it">colorfulness</span> of the shelf as the minimum distance between two different cubes of the same color on the shelf. If all the cubes on the shelf have different colors, then the <span class="tex-font-style-it">colorfulness</span> is considered to be equal to the size of the shelf, that is, the number $k$.</p><p>More formally, the <span class="tex-font-style-it">colorfulness</span> of $c_1, c_2, \ldots, c_k$ is defined as follows:</p><ul><li> If all the colors $c_1, c_2, \ldots, c_k$ are different, the <span class="tex-font-style-it">colorfulness</span> is considered to be $k$.</li><li> Otherwise, the <span class="tex-font-style-it">colorfulness</span> is considered to be the smallest integer $x \geq 1$ such that there exists an index $i$ $(1 \le i \le k - x)$ such that $c_i = c_{i+x}$.</li></ul><p>For each shelf, you are given the minimum required <span class="tex-font-style-it">colorfulness</span>, that is, you are given numbers $d_1, d_2, \ldots, d_m$, which mean that shelf $i$ must have a <span class="tex-font-style-it">colorfulness</span> $\geq d_i$ for all $i$.</p><p>Distribute the available cubes among the shelves to ensure the required <span class="tex-font-style-it">colorfulness</span>, or report that it is impossible.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ $(1 \leq t \leq 10^4)$&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n, m$ $(1 \leq m \leq n \leq 2 \cdot 10^5)$&nbsp;— the number of cubes and the number of shelves to distribute them to.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ $(1 \leq a_i \leq n)$&nbsp;— the colors of the cubes.</p><p>The third line of each test case contains $m$ integers $s_1, s_2, \ldots, s_m$ $(1 \leq s_i \leq n)$&nbsp;— the sizes of the shelves. It's guaranteed, that $s_1 + \ldots + s_m = n$.</p><p>The fourth line of each test case contains $m$ integers $d_1, d_2, \ldots, d_m$ $(1 \leq d_i \leq s_i)$&nbsp;— the minimum required <span class="tex-font-style-it">colorfulness</span> of the shelves.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, if it is impossible to distribute the cubes on the shelves satisfying all the requirements, output a single number $-1$. Otherwise, output $m$ lines, where the $i$-th line should contain $s_i$ numbers representing the colors of the cubes on the $i$-th shelf, in the appropriate order.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ $(1 \leq t \leq 10^4)$&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n, m$ $(1 \leq m \leq n \leq 2 \cdot 10^5)$&nbsp;— the number of cubes and the number of shelves to distribute them to.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ $(1 \leq a_i \leq n)$&nbsp;— the colors of the cubes.</p><p>The third line of each test case contains $m$ integers $s_1, s_2, \ldots, s_m$ $(1 \leq s_i \leq n)$&nbsp;— the sizes of the shelves. It's guaranteed, that $s_1 + \ldots + s_m = n$.</p><p>The fourth line of each test case contains $m$ integers $d_1, d_2, \ldots, d_m$ $(1 \leq d_i \leq s_i)$&nbsp;— the minimum required <span class="tex-font-style-it">colorfulness</span> of the shelves.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, if it is impossible to distribute the cubes on the shelves satisfying all the requirements, output a single number $-1$. Otherwise, output $m$ lines, where the $i$-th line should contain $s_i$ numbers representing the colors of the cubes on the $i$-th shelf, in the appropriate order.</p>





```input1|2,3,4,5,10,11,12,13,18,19,20,21
6
10 3
1 1 1 1 2 2 2 3 3 4
6 2 2
4 1 1
8 2
7 7 7 7 8 8 8 8
4 4
2 2
5 1
5 4 3 2 1
5
3
7 3
1 2 2 2 2 3 4
1 2 4
1 2 4
12 7
6 6 6 6 6 6 6 6 6 7 8 9
2 2 2 2 2 1 1
1 2 2 2 1 1 1
20 2
11 20 15 6 8 18 12 16 8 20 10 12 3 12 20 11 15 8 17 17
8 12
3 5
```




```output1
1 3 4 2 1 3 
1 1 
2 2 
8 7 8 7 
8 7 8 7 
2 4 5 3 1 
-1
6 6 
7 6 
8 6 
9 6 
6 6 
6 
6 
12 17 20 15 8 20 16 11 
15 20 17 12 10 8 3 18 12 11 8 6
```


