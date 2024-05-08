## Description

<div><p>Keksic keeps getting left on seen by Anji. Through a mutual friend, he's figured out that Anji really likes binary trees and decided to solve her problem in order to get her attention.</p><p>Anji has given Keksic a binary tree with $n$ vertices. Vertex $1$ is the root and does not have a parent. All other vertices have exactly one parent. Each vertex can have up to $2$ children, a left child, and a right child. For each vertex, Anji tells Keksic index of both its left and its right child or tells him that they do not exist. </p><p>Additionally, each of the vertices has a letter $s_i$ on it, which is either '<span class="tex-font-style-tt">U</span>', '<span class="tex-font-style-tt">L</span>' or '<span class="tex-font-style-tt">R</span>'.</p><p>Keksic begins his journey on the root, and in each move he does the following: </p><ul> <li> If the letter on his current vertex is '<span class="tex-font-style-tt">U</span>', he moves to its parent. If it doesn't exist, he does nothing. </li><li> If the letter on his current vertex is '<span class="tex-font-style-tt">L</span>', he moves to its left child. If it doesn't exist, he does nothing. </li><li> If the letter on his current vertex is '<span class="tex-font-style-tt">R</span>', he moves to its right child. If it doesn't exist, he does nothing. </li></ul> Before his journey, he can perform the following operations: choose any node, and replace the letter written on it with another one. <p>You are interested in the minimal number of operations he needs to do before his journey, such that when he starts his journey, he will reach a leaf at some point. A leaf is a vertex that has no children. It does not matter which leaf he reaches. Note that it does not matter whether he will stay in the leaf, he just needs to move to it. Additionally, note that it does not matter how many times he needs to move before reaching a leaf.</p><p>Help Keksic solve Anji's tree so that he can win her heart, and make her come to Čačak.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 5 \cdot 10^4$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 3 \cdot 10^5$)&nbsp;— the number of vertices in a tree.</p><p>The second line of each test case contains a string $s$ of $n$ characters&nbsp;— characters are written on the vertices. It is guaranteed that $s$ consists only of characters '<span class="tex-font-style-tt">U</span>', '<span class="tex-font-style-tt">L</span>', and '<span class="tex-font-style-tt">R</span>'.</p><p>The $i$-th of the next $n$ lines contains two integers $l_i$ and $r_i$ ($0 \le l_i, r_i \le n$)&nbsp;— indices of left and right child of the vertex $i$. If $l_i = 0$, it means that vertex $i$ does not have a left child. If $r_i = 0$, it means that vertex $i$ does not have a right child. It is guaranteed that this data describes a valid binary tree rooted at $1$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $3 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the minimal number of operations Keksic needs to do to reach a leaf.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 5 \cdot 10^4$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 3 \cdot 10^5$)&nbsp;— the number of vertices in a tree.</p><p>The second line of each test case contains a string $s$ of $n$ characters&nbsp;— characters are written on the vertices. It is guaranteed that $s$ consists only of characters '<span class="tex-font-style-tt">U</span>', '<span class="tex-font-style-tt">L</span>', and '<span class="tex-font-style-tt">R</span>'.</p><p>The $i$-th of the next $n$ lines contains two integers $l_i$ and $r_i$ ($0 \le l_i, r_i \le n$)&nbsp;— indices of left and right child of the vertex $i$. If $l_i = 0$, it means that vertex $i$ does not have a left child. If $r_i = 0$, it means that vertex $i$ does not have a right child. It is guaranteed that this data describes a valid binary tree rooted at $1$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $3 \cdot 10^5$.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the minimal number of operations Keksic needs to do to reach a leaf.</p>





```input1|2,3,4,5,6,12,13,14,15,22,23,24,25,26,27,28,29,30
5
3
LRU
2 3
0 0
0 0
3
ULR
3 2
0 0
0 0
2
LU
0 2
0 0
4
RULR
3 0
0 0
0 4
2 0
7
LLRRRLU
5 2
3 6
0 0
7 0
4 0
0 0
0 0
```




```output1
0
1
1
3
1
```



## Note

<p>In the first test case, vertex $1$ has $2$ as its left child and $3$ as its right child. Vertices $2$ and $3$ do not have children and are therefore leaves. As '<span class="tex-font-style-tt">L</span>' is written on vertex $1$, Keksic will go to vertex $2$, therefore he has to do no operations.</p><p>In the second test case, vertex $1$ has $3$ as its left child and $2$ as its right child. Vertices $2$ and $3$ are leaves. As '<span class="tex-font-style-tt">U</span>' is written on vertex $1$, Keksic needs to change it to either '<span class="tex-font-style-tt">L</span>' or '<span class="tex-font-style-tt">R</span>' in order for him to reach a leaf.</p><p>In the third case, vertex $1$ has only a right child, which is vertex $2$. As '<span class="tex-font-style-tt">L</span>' is written on it, Keksic needs to change it to '<span class="tex-font-style-tt">R</span>', otherwise he would be stuck on vertex $1$.</p><p>In the fourth case, he can change $3$ characters so that letters on the vertices are "<span class="tex-font-style-tt">LURL</span>", which makes him reach vertex $2$.</p><p>In the fifth case, there are $3$ leaves, $3$, $6$ and $7$. To reach either leaf $6$ or leaf $7$, he needs to change $2$ characters. However, if he changes character on vertex $1$ to '<span class="tex-font-style-tt">R</span>', he will reach leaf $3$, therefore the answer is $1$.</p><center>  <img class="tex-graphics" src="file://VZD50jYI.png" style="max-width: 100.0%;max-height: 100.0%;" width="720px">   <span class="tex-font-size-small">The initial tree in test case 5.</span> </center>
