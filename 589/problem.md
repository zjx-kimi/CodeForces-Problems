## Description

<div><p>Initially you have a single pile with $n$ gold nuggets. In an operation you can do the following: </p><ul> <li> Take any pile and split it into two piles, so that one of the resulting piles has exactly twice as many gold nuggets as the other. (All piles should have an integer number of nuggets.) </li></ul> <center> <img class="tex-graphics" src="file://UdjszuQQ.png" style="max-width: 100.0%;max-height: 100.0%;"><p><span class="tex-font-size-small">One possible move is to take a pile of size $6$ and split it into piles of sizes $2$ and $4$, which is valid since $4$ is twice as large as $2$.</span> </p></center> Can you make a pile with <span class="tex-font-style-bf">exactly</span> $m$ gold nuggets using zero or more operations?</div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains two integers $n$ and $m$ ($1 \leq n, m \leq 10^7$)&nbsp;— the starting and target pile sizes, respectively.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if you can make a pile of size exactly $m$, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains two integers $n$ and $m$ ($1 \leq n, m \leq 10^7$)&nbsp;— the starting and target pile sizes, respectively.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if you can make a pile of size exactly $m$, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p>





```input1|2,4,6,8,10,12
11
6 4
9 4
4 2
18 27
27 4
27 2
27 10
1 1
3 1
5 1
746001 2984004
```




```output1
YES
YES
NO
NO
YES
YES
NO
YES
YES
NO
NO
```



## Note

<p>The first test case is pictured in the statement. We can make a pile of size $4$.</p><p>In the second test case, we can perform the following operations: $\{\color{red}{9}\} \to \{\color{red}{6},3\} \to \{4,2,3\}$. The pile that is split apart is colored red before each operation.</p><p>In the third test case, we can't perform a single operation.</p><p>In the fourth test case, we can't end up with a larger pile than we started with.</p>
