## Description

<div><p>You are given an array $a_1, a_2, \ldots, a_n$. You need to find an array $b_1, b_2, \ldots, b_n$ consisting of numbers $1$, $2$, $3$ such that <span class="tex-font-style-bf">exactly two</span> out of the following three conditions are satisfied:</p><ol><li> There exist indices $1 \leq i, j \leq n$ such that $a_i = a_j$, $b_i = 1$, $b_j = 2$.</li><li> There exist indices $1 \leq i, j \leq n$ such that $a_i = a_j$, $b_i = 1$, $b_j = 3$.</li><li> There exist indices $1 \leq i, j \leq n$ such that $a_i = a_j$, $b_i = 2$, $b_j = 3$.</li></ol><p>If such an array does not exist, you should report it.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ $(1 \leq t \leq 500)$&nbsp;— the number of test cases. Each test case is described as follows.</p><p>The first line of each test case contains an integer $n$ $(1 \leq n \leq 100)$&nbsp;— the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ $(1 \leq a_i \leq 100)$&nbsp;— the elements of the array $a$.</p></div><div class="output-specification"><p>For each test case, print <span class="tex-font-style-tt">-1</span> if there is no solution. Otherwise, print $b_1, b_2, \ldots, b_n$&nbsp;— an array consisting of numbers $1$, $2$, $3$ that satisfies <span class="tex-font-style-bf">exactly two</span> out of three conditions. If there are multiple possible answers, you can print any of them.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ $(1 \leq t \leq 500)$&nbsp;— the number of test cases. Each test case is described as follows.</p><p>The first line of each test case contains an integer $n$ $(1 \leq n \leq 100)$&nbsp;— the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ $(1 \leq a_i \leq 100)$&nbsp;— the elements of the array $a$.</p>

## Output

<p>For each test case, print <span class="tex-font-style-tt">-1</span> if there is no solution. Otherwise, print $b_1, b_2, \ldots, b_n$&nbsp;— an array consisting of numbers $1$, $2$, $3$ that satisfies <span class="tex-font-style-bf">exactly two</span> out of three conditions. If there are multiple possible answers, you can print any of them.</p>





```input1|2,3,6,7,10,11,14,15,18,19
9
6
1 2 3 2 2 3
7
7 7 7 7 7 7 7
4
1 1 2 2
7
1 2 3 4 5 6 7
5
2 3 3 3 2
3
1 2 1
9
1 1 1 7 7 7 9 9 9
1
1
18
93 84 50 21 88 52 16 50 63 1 30 85 29 67 63 58 37 69
```




```output1
1 2 3 1 1 1 
-1
3 2 2 1 
-1
2 1 2 1 3 
-1
1 1 2 2 1 2 2 3 3
-1
3 2 1 3 3 3 3 2 2 1 1 2 3 1 3 1 1 2
```



## Note

<p>In the first test case, $b = [1, 2, 3, 1, 1, 1]$ satisfies condition $1$ because for $i = 4$, $j = 2$: $a_i = a_j$, $b_i = 1$, and $b_j = 2$. It also satisfies condition $2$ because for $i = 6$, $j = 3$: $a_i = a_j$, $b_i = 1$, and $b_j = 3$. However, it <span class="tex-font-style-bf">does not</span> satisfy condition $3$. In total, <span class="tex-font-style-bf">exactly</span> two out of three conditions are satisfied.</p>
