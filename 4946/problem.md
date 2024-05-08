## Description

<div><p>Li Hua has a tree of $n$ vertices and $n-1$ edges. The root of the tree is vertex $1$. Each vertex $i$ has importance $a_i$. Denote the <span class="tex-font-style-it">size</span> of a subtree as the number of vertices in it, and the <span class="tex-font-style-it">importance</span> as the sum of the importance of vertices in it. Denote the <span class="tex-font-style-it">heavy son</span> of a non-leaf vertex as the son with the <span class="tex-font-style-bf">largest</span> subtree <span class="tex-font-style-it">size</span>. If multiple of them exist, the <span class="tex-font-style-it">heavy son</span> is the one with the <span class="tex-font-style-bf">minimum</span> index.</p><p>Li Hua wants to perform $m$ operations:</p><ul> <li> "1 $x$" ($1\leq x \leq n$)&nbsp;— calculate the <span class="tex-font-style-it">importance</span> of the subtree whose root is $x$. </li><li> "2 $x$" ($2\leq x \leq n$)&nbsp;— rotate the <span class="tex-font-style-it">heavy son</span> of $x$ up. Formally, denote $son_x$ as the <span class="tex-font-style-it">heavy son</span> of $x$, $fa_x$ as the father of $x$. He wants to remove the edge between $x$ and $fa_x$ and connect an edge between $son_x$ and $fa_x$. It is guaranteed that $x$ is not root, but <span class="tex-font-style-bf">not</span> guaranteed that $x$ is not a leaf. If $x$ is a leaf, please ignore the operation. </li></ul><p>Suppose you were Li Hua, please solve this problem.</p></div><div class="input-specification"><p>The first line contains 2 integers $n,m$ ($2\le n\le 10^{5},1\le m\le 10^{5}$)&nbsp;— the number of vertices in the tree and the number of operations.</p><p>The second line contains $n$ integers $a_{1},a_{2},\ldots ,a_{n}$ ($-10^{9}\le a_{i}\le 10^{9}$)&nbsp;— the importance of each vertex.</p><p>Next $n-1$ lines contain the edges of the tree. The $i$-th line contains two integers $u_i$ and $v_i$ ($1\le u_i,v_i\le n$, $u_i\ne v_i$)&nbsp;— the corresponding edge. The given edges form a tree.</p><p>Next $m$ lines contain operations&nbsp;— one operation per line. The $j$-th operation contains two integers $t_{j},x_{j}$ ($t_{j}\in \{1,2\}$, $1 \leq x_{j} \leq n$, $x_{j}\neq 1$ if $t_j = 2$)&nbsp;— the $j$-th operation. </p></div><div class="output-specification"><p>For each query "1 $x$", output the answer in an independent line.</p></div>

## Input

<p>The first line contains 2 integers $n,m$ ($2\le n\le 10^{5},1\le m\le 10^{5}$)&nbsp;— the number of vertices in the tree and the number of operations.</p><p>The second line contains $n$ integers $a_{1},a_{2},\ldots ,a_{n}$ ($-10^{9}\le a_{i}\le 10^{9}$)&nbsp;— the importance of each vertex.</p><p>Next $n-1$ lines contain the edges of the tree. The $i$-th line contains two integers $u_i$ and $v_i$ ($1\le u_i,v_i\le n$, $u_i\ne v_i$)&nbsp;— the corresponding edge. The given edges form a tree.</p><p>Next $m$ lines contain operations&nbsp;— one operation per line. The $j$-th operation contains two integers $t_{j},x_{j}$ ($t_{j}\in \{1,2\}$, $1 \leq x_{j} \leq n$, $x_{j}\neq 1$ if $t_j = 2$)&nbsp;— the $j$-th operation. </p>

## Output

<p>For each query "1 $x$", output the answer in an independent line.</p>





```input1
7 4
1 1 1 1 1 1 1
1 2
1 3
2 4
2 5
3 6
6 7
1 6
2 3
1 6
1 2
```




```input2
10 14
-160016413 -90133231 -671446275 -314847579 -910548234 121155052 -359359950 83112406 -704889624 145489303
1 6
1 10
10 8
1 4
3 4
2 7
2 5
3 2
9 8
1 4
2 2
2 4
1 4
1 10
2 10
1 9
1 6
2 8
2 10
1 5
1 8
1 1
2 5
```




```output1
2
3
3
```




```output2
-2346335269
-314847579
-476287915
-704889624
121155052
-1360041415
228601709
-2861484545
```



## Note

<p>In the first example:</p><p>The initial tree is shown in the following picture:</p><center> <table class="tex-tabular"><tbody><tr><td class="tex-tabular-text-align-center"><img class="tex-graphics" src="file://Syhx9Mh2.png" style="max-width: 100.0%;max-height: 100.0%;"></td></tr></tbody></table> </center><p>The <span class="tex-font-style-it">importance</span> of the subtree of $6$ is $a_6+a_7=2$.</p><p>After rotating the <span class="tex-font-style-it">heavy son</span> of $3$ (which is $6$) up, the tree is shown in the following picture:</p><center> <table class="tex-tabular"><tbody><tr><td class="tex-tabular-text-align-center"><img class="tex-graphics" src="file://WiMEDJCJ.png" style="max-width: 100.0%;max-height: 100.0%;"></td></tr></tbody></table> </center><p>The <span class="tex-font-style-it">importance</span> of the subtree of $6$ is $a_6+a_3+a_7=3$.</p><p>The <span class="tex-font-style-it">importance</span> of the subtree of $2$ is $a_2+a_4+a_5=3$.</p>
