## Description

<div><p>Mihai has just learned about the <a href="https://en.wikipedia.org/wiki/Mex_(mathematics)">MEX</a> concept and since he liked it so much, he decided to use it right away.</p><p>Given an array $a$ of $n$ non-negative integers, Mihai wants to create <span class="tex-font-style-bf">a new array $b$</span> that is formed in the following way:</p><p>While $a$ is not empty: </p><ul> <li> Choose an integer $k$ ($1 \leq k \leq |a|$). </li><li> Append the MEX of the first $k$ numbers of the array $a$ to the end of array $b$ and erase them from the array $a$, shifting the positions of the remaining numbers in $a$. </li></ul><p>But, since Mihai loves big arrays as much as the MEX concept, he wants the new array $b$ to be the <span class="tex-font-style-bf">lexicographically maximum</span>. So, Mihai asks you to tell him what the maximum array $b$ that can be created by constructing the array optimally is.</p><p>An array $x$ is lexicographically greater than an array $y$ if in the first position where $x$ and $y$ differ $x_i &gt; y_i$ or if $|x| &gt; |y|$ and $y$ is a prefix of $x$ (where $|x|$ denotes the size of the array $x$).</p><p>The <span class="tex-font-style-bf">MEX</span> of a set of non-negative integers is the minimal non-negative integer such that it is not in the set. For example, <span class="tex-font-style-bf">MEX</span>({${1, 2, 3}$}) $= 0$ and <span class="tex-font-style-bf">MEX</span>({${0, 1, 2, 4, 5}$}) $= 3$.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 100$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 2 \cdot 10^5$) — the number of elements in the array $a$.</p><p>The second line of each test case contains $n$ <span class="tex-font-style-bf">non-negative</span> integers $a_1, \ldots, a_n$ ($0 \leq a_i \leq n$), where $a_i$ is the $i$-th integer from the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case print $m$ — the length of the maximum array $b$ Mihai can create, followed by $m$ integers denoting the elements of the array $b$.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 100$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 2 \cdot 10^5$) — the number of elements in the array $a$.</p><p>The second line of each test case contains $n$ <span class="tex-font-style-bf">non-negative</span> integers $a_1, \ldots, a_n$ ($0 \leq a_i \leq n$), where $a_i$ is the $i$-th integer from the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case print $m$ — the length of the maximum array $b$ Mihai can create, followed by $m$ integers denoting the elements of the array $b$.</p>





```input1|2,3,6,7,10,11
6
5
1 0 2 0 3
8
2 2 3 4 0 1 2 0
1
1
5
0 1 2 3 4
4
0 1 1 0
10
0 0 2 1 1 1 0 0 1 1
```




```output1
1
4 
2
5 1 
1
0 
1
5 
2
2 2 
4
3 2 2 0
```



## Note

<p>In the first test case, the lexicographically maximum array $b$ is obtained by selecting $k=5$, resulting in the $MEX$ of the whole array $a$. It is lexicographically maximum because an array starting with a smaller number than $4$ is lexicographically smaller, and choosing a $k&lt;5$ would result in an array starting with a number smaller than $4$.</p><p>In the second test case, there are two ways to obtain the maximum array: first selecting $k=6$, then $k=2$, or first selecting $k=7$ and then $k=1$.</p>
