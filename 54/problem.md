## Description

<div><p>There is an edge-weighted complete binary tree with $n$ leaves. A complete binary tree is defined as a tree where every non-leaf vertex has exactly 2 children. For each non-leaf vertex, we label one of its children as the left child and the other as the right child.</p><p>The binary tree has a very strange property. For every non-leaf vertex, one of the edges to its children has weight $0$ while the other edge has weight $1$. Note that the edge with weight $0$ can be connected to either its left or right child.</p><p>You forgot what the tree looks like, but luckily, you still remember some information about the leaves in the form of an array $a$ of size $n$. For each $i$ from $1$ to $n$, $a_i$ represents the distance$^\dagger$ from the root to the $i$-th leaf in dfs order$^\ddagger$. Determine whether there exists a complete binary tree which satisfies array $a$. Note that you <span class="tex-font-style-bf">do not</span> need to reconstruct the tree.</p><p>$^\dagger$ The distance from vertex $u$ to vertex $v$ is defined as the sum of weights of the edges on the path from vertex $u$ to vertex $v$.</p><p>$^\ddagger$ The dfs order of the leaves is found by calling the following $\texttt{dfs}$ function on the root of the binary tree. </p><pre class="verbatim"><br>dfs_order = []<br><br>function dfs(v):<br>    if v is leaf:<br>        append v to the back of dfs_order<br>    else:<br>        dfs(left child of v)<br>        dfs(right child of v)<br><br>dfs(root)<br></pre></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 2\cdot 10^5$)&nbsp;— the size of array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i \le n - 1$)&nbsp;— the distance from the root to the $i$-th leaf.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print "YES" if there exists a complete binary tree which satisfies array $a$ and "NO" otherwise.</p><p>You may print each letter in any case (for example, "YES", "Yes", "yes", "yEs" will all be recognized as a positive answer).</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 2\cdot 10^5$)&nbsp;— the size of array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i \le n - 1$)&nbsp;— the distance from the root to the $i$-th leaf.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p>

## Output

<p>For each test case, print "YES" if there exists a complete binary tree which satisfies array $a$ and "NO" otherwise.</p><p>You may print each letter in any case (for example, "YES", "Yes", "yes", "yEs" will all be recognized as a positive answer).</p>





```input1|2,3
2
5
2 1 0 1 1
5
1 0 2 1 3
```




```output1
YES
NO
```



## Note

<p>In the first test case, the following tree satisfies the array.</p><p><img class="tex-graphics" src="file://YEmuoBmD.png" style="max-width: 100.0%;max-height: 100.0%;"></p><p>In the second test case, it can be proven that there is no complete binary tree that satisfies the array.</p>
