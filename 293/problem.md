## Description

<div><p>You have $n$ sets of integers $S_{1}, S_{2}, \ldots, S_{n}$. We call a set $S$ <span class="tex-font-style-it">attainable</span>, if it is possible to choose some (possibly, none) of the sets $S_{1}, S_{2}, \ldots, S_{n}$ so that $S$ is equal to their union$^{\dagger}$. If you choose none of $S_{1}, S_{2}, \ldots, S_{n}$, their union is an empty set.</p><p>Find the maximum number of elements in an attainable $S$ such that $S \neq S_{1} \cup S_{2} \cup \ldots \cup S_{n}$.</p><p>$^{\dagger}$ The union of sets $A_1, A_2, \ldots, A_k$ is defined as the set of elements present in at least one of these sets. It is denoted by $A_1 \cup A_2 \cup \ldots \cup A_k$. For example, $\{2, 4, 6\} \cup \{2, 3\} \cup \{3, 6, 7\} = \{2, 3, 4, 6, 7\}$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 50$).</p><p>The following $n$ lines describe the sets $S_1, S_2, \ldots, S_n$. The $i$-th of these lines contains an integer $k_{i}$ ($1 \le k_{i} \le 50$)&nbsp;— the number of elements in $S_{i}$, followed by $k_{i}$ integers $s_{i, 1}, s_{i, 2}, \ldots, s_{i, k_{i}}$ ($1 \le s_{i, 1} &lt; s_{i, 2} &lt; \ldots &lt; s_{i, k_{i}} \le 50$)&nbsp;— the elements of $S_{i}$.</p></div><div class="output-specification"><p>For each test case, print a single integer&nbsp;— the maximum number of elements in an attainable $S$ such that $S \neq S_{1} \cup S_{2} \cup \ldots \cup S_{n}$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 50$).</p><p>The following $n$ lines describe the sets $S_1, S_2, \ldots, S_n$. The $i$-th of these lines contains an integer $k_{i}$ ($1 \le k_{i} \le 50$)&nbsp;— the number of elements in $S_{i}$, followed by $k_{i}$ integers $s_{i, 1}, s_{i, 2}, \ldots, s_{i, k_{i}}$ ($1 \le s_{i, 1} &lt; s_{i, 2} &lt; \ldots &lt; s_{i, k_{i}} \le 50$)&nbsp;— the elements of $S_{i}$.</p>

## Output

<p>For each test case, print a single integer&nbsp;— the maximum number of elements in an attainable $S$ such that $S \neq S_{1} \cup S_{2} \cup \ldots \cup S_{n}$.</p>





```input1|2,3,4,5,11,12,13,14,15,16
4
3
3 1 2 3
2 4 5
2 3 4
4
4 1 2 3 4
3 2 5 6
3 3 5 6
3 4 5 6
5
1 1
3 3 6 10
1 9
2 1 3
3 5 8 9
1
2 4 28
```




```output1
4
5
6
0
```



## Note

<p>In the first test case, $S = S_{1} \cup S_{3} = \{1, 2, 3, 4\}$ is the largest attainable set not equal to $S_1 \cup S_2 \cup S_3 = \{1, 2, 3, 4, 5\}$.</p><p>In the second test case, we can pick $S = S_{2} \cup S_{3} \cup S_{4} = \{2, 3, 4, 5, 6\}$.</p><p>In the third test case, we can pick $S = S_{2} \cup S_{5} = S_{2} \cup S_{3} \cup S_{5} = \{3, 5, 6, 8, 9, 10\}$.</p><p>In the fourth test case, the only attainable set is $S = \varnothing$.</p>
