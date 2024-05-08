## Description

<div><p>In order to win his toughest battle, Mircea came up with a great strategy for his army. He has $n$ soldiers and decided to arrange them in a certain way in camps. Each soldier has to belong to exactly one camp, and there is one camp at each integer point on the $x$-axis (at points $\cdots, -2, -1, 0, 1, 2, \cdots$).</p><p>The strategy consists of $m$ conditions. Condition $i$ tells that soldier $a_i$ should belong to a camp that is situated $d_i$ meters in front of the camp that person $b_i$ belongs to. (If $d_i &lt; 0$, then $a_i$'s camp should be $-d_i$ meters behind $b_i$'s camp.)</p><p>Now, Mircea wonders if there exists a partition of soldiers that respects the condition and he asks for your help! Answer "<span class="tex-font-style-tt">YES</span>" if there is a partition of the $n$ soldiers that satisfies <span class="tex-font-style-bf">all</span> of the $m$ conditions and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>Note that two different soldiers <span class="tex-font-style-bf">may</span> be placed in the same camp.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 100$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two positive integers $n$ and $m$ ($2 \leq n \leq 2 \cdot 10^5$; $1 \leq m \leq n$)&nbsp;— the number of soldiers, and the number of conditions respectively.</p><p>Then $m$ lines follow, each of them containing $3$ integers: $a_i$, $b_i$, $d_i$ ($a_i \neq b_i$; $1 \leq a_i, b_i \leq n$; $-10^9 \leq d_i \leq 10^9$)&nbsp;— denoting the conditions explained in the statement. Note that if $d_i$ is positive, $a_i$ should be $d_i$ meters in front of $b_i$ and if it is negative, $a_i$ should be $-d_i$ meters behind $b_i$.</p><p>Note that the sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if there is an arrangement of the $n$ soldiers that satisfies <span class="tex-font-style-bf">all</span> of the $m$ conditions and "<span class="tex-font-style-tt">NO</span>" otherwise.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 100$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two positive integers $n$ and $m$ ($2 \leq n \leq 2 \cdot 10^5$; $1 \leq m \leq n$)&nbsp;— the number of soldiers, and the number of conditions respectively.</p><p>Then $m$ lines follow, each of them containing $3$ integers: $a_i$, $b_i$, $d_i$ ($a_i \neq b_i$; $1 \leq a_i, b_i \leq n$; $-10^9 \leq d_i \leq 10^9$)&nbsp;— denoting the conditions explained in the statement. Note that if $d_i$ is positive, $a_i$ should be $d_i$ meters in front of $b_i$ and if it is negative, $a_i$ should be $-d_i$ meters behind $b_i$.</p><p>Note that the sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if there is an arrangement of the $n$ soldiers that satisfies <span class="tex-font-style-bf">all</span> of the $m$ conditions and "<span class="tex-font-style-tt">NO</span>" otherwise.</p>





```input1|2,3,4,5,12,13,14
4
5 3
1 2 2
2 3 4
4 2 -6
6 5
1 2 2
2 3 4
4 2 -6
5 4 4
3 5 100
2 2
1 2 5
1 2 4
4 1
1 2 3
```




```output1
YES
NO
NO
YES
```



## Note

<p>For the first test case, we can partition the soldiers into camps in the following way: soldier:</p><ul> <li> Soldier $1$ in the camp with the coordinate $x = 3$. </li><li> Soldier $2$ in the camp with the coordinate $x = 5$. </li><li> Soldier $3$ in the camp with the coordinate $x = 9$. </li><li> Soldier $4$ in the camp with the coordinate $x = 11$. </li></ul><p>For the second test case, there is no partition that can satisfy all the constraints at the same time.</p><p>For the third test case, there is no partition that satisfies all the constraints since we get contradictory information about the same pair.</p><p>For the fourth test case, in order to satisfy the only condition, a possible partition is:</p><ul> <li> Soldier $1$ in the camp with the coordinate $x = 10$. </li><li> Soldier $2$ in the camp with the coordinate $x = 13$. </li><li> Soldier $3$ in the camp with the coordinate $x = -2023$. </li><li> Soldier $4$ in the camp with the coordinate $x = -2023$. </li></ul>
