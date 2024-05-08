## Description

<div><p>A <span class="tex-font-style-it">pseudotree</span> is a connected graph which has <span class="tex-font-style-bf">exactly one</span> cycle and <span class="tex-font-style-bf">no</span> self-loops. Note that a pseudotree <span class="tex-font-style-bf">may contain multiple-edges</span>. It can be shown that a pseudotree with $n$ vertices always contains $n$ edges.</p><p>After deleting all edges on the cycle in the pseudotree, a forest$^{\dagger}$ will be formed. It can be shown that each tree in the forest will contain exactly one vertex which is on cycle before removing the edges. If all trees in the forest have the same depth$^{\ddagger}$ when picking the vertex on cycle as root, we call the original pseudotree <span class="tex-font-style-it">flower-like</span>.</p><p>Our friend sszcdjr, had a flower-like pseudotree with $n$ vertices and $n$ edges. However, he forgot all the edges in the pseudotree. Fortunately, he still remembers the degrees of vertices. Specifically, the degree of the $i$-th vertex is $d_i$.</p><p>You have to help sszcdjr construct a possible flower-like pseudotree with $n$ vertices, where the degree of the $i$-th vertex is <span class="tex-font-style-bf">exactly</span> $d_i$, or tell him that it is impossible.</p><p>$^{\dagger}$ A forest is a graph in which all connectivity components are trees. A connected graph without cycles and self-loops is called a tree.</p><p>$^{\ddagger}$ The depth of a tree with a root is the maximum distance from the root to the vertex of this tree.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1\leq t\leq 10^5$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2\leq n\leq 10^6$) — the number of vertices.</p><p>The second line of each test case contains $n$ integers $d_1,d_2,\ldots,d_n$ ($1\leq d_i\leq n$) — the degree of each vertex.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^6$.</p></div><div class="output-specification"><p>For each test case, if there exist a possible flower-like pseudotree:</p><ul> <li> Print "<span class="tex-font-style-tt">Yes</span>" (without quotes) in the first line. </li><li> Then, output $n$ lines, in each line print two integers $u_i$ and $v_i$ — the two vertices that the $i$-th edge connects. </li></ul><p>If there are multiple answers, you may output any of them.</p><p>Otherwise, print "<span class="tex-font-style-tt">No</span>" (without quotes) in the only line of output.</p><p>You can output the first line of each test case in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1\leq t\leq 10^5$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2\leq n\leq 10^6$) — the number of vertices.</p><p>The second line of each test case contains $n$ integers $d_1,d_2,\ldots,d_n$ ($1\leq d_i\leq n$) — the degree of each vertex.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^6$.</p>

## Output

<p>For each test case, if there exist a possible flower-like pseudotree:</p><ul> <li> Print "<span class="tex-font-style-tt">Yes</span>" (without quotes) in the first line. </li><li> Then, output $n$ lines, in each line print two integers $u_i$ and $v_i$ — the two vertices that the $i$-th edge connects. </li></ul><p>If there are multiple answers, you may output any of them.</p><p>Otherwise, print "<span class="tex-font-style-tt">No</span>" (without quotes) in the only line of output.</p><p>You can output the first line of each test case in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p>





```input1|2,3,6,7,10,11
6
3
2 2 2
4
1 2 3 4
7
4 3 3 1 1 1 1
6
1 1 2 2 3 3
10
1 1 5 2 1 1 1 1 1 6
9
1 1 3 1 1 4 1 1 5
```




```output1
Yes
1 2
2 3
3 1
No
Yes
1 2
2 3
3 1
1 4
1 5
2 6
3 7
Yes
5 6
6 5
1 3
2 4
3 5
4 6
No
Yes
3 6
6 9
9 3
1 3
2 6
4 6
5 9
7 9
8 9
```



## Note

<p>In the first test case, the only possible flower-like psuedotree is:</p><center> <img class="tex-graphics" src="file://EZ9vfLGT.png" style="max-width: 100.0%;max-height: 100.0%;" width="227px"> </center><p>After deleting all edges on the cycle in the pseudotree, each tree has depth $0$.</p><p>In the second test case, it can be proven that there's no such flower-like psuedotree.</p><p>In the third test case, one of the possible flower-like psuedotrees is:</p><center> <img class="tex-graphics" src="file://f0JqgXwy.png" style="max-width: 100.0%;max-height: 100.0%;" width="227px"> </center>
