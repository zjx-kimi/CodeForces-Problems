## Description

<div><p>The fox Yae climbed the <span class="tex-font-style-it">tree</span> of the Sacred Sakura. A tree is a connected undirected graph that does not contain cycles.</p><p>The fox uses her magical powers to move around the tree. Yae can jump from vertex $v$ to another vertex $u$ if and only if the distance between these vertices does not exceed $2$. In other words, in one jump Yae can jump from vertex $v$ to vertex $u$ if vertices $v$ and $u$ are connected by an edge, or if there exists such vertex $w$ that vertices $v$ and $w$ are connected by an edge, and also vertices $u$ and $w$ are connected by an edge.</p><p>After Yae was able to get the sakura petal, she wondered if there was a <span class="tex-font-style-bf">cyclic</span> route in the tree $v_1, v_2, \ldots, v_n$ such that:</p><ul> <li> the fox can jump from vertex $v_i$ to vertex $v_{i + 1}$, </li><li> the fox can jump from vertex $v_n$ to vertex $v_1$, </li><li> all $v_i$ are pairwise distinct. </li></ul><p>Help the fox determine if the required traversal exists.</p></div><div class="input-specification"><p>The first line contains one integer $n$ ($2 \le n \le 2 \cdot 10^5$)&nbsp;—the number of vertices of the tree.</p><p>Each of the following $n - 1$ lines contains two integers $u$ and $v$ ($1 \le u, v \le n$, $u \ne v$)&nbsp;— vertices connected by an edge. It is guaranteed that these edges form a tree.</p></div><div class="output-specification"><p>On the first line, print "<span class="tex-font-style-tt">Yes</span>" (without quotes) if the required route of the tree exists, or "<span class="tex-font-style-tt">No</span>" (without quotes) otherwise.</p><p>If the required tree traversal exists, on the second line print $n$ integers of different integers $v_1, v_2, \ldots, v_n$ ($1 \le v_i \le n$)&nbsp;— the vertices of the tree in traversal order.</p><p>If there are several correct traversals, output any of them.</p></div>

## Input

<p>The first line contains one integer $n$ ($2 \le n \le 2 \cdot 10^5$)&nbsp;—the number of vertices of the tree.</p><p>Each of the following $n - 1$ lines contains two integers $u$ and $v$ ($1 \le u, v \le n$, $u \ne v$)&nbsp;— vertices connected by an edge. It is guaranteed that these edges form a tree.</p>

## Output

<p>On the first line, print "<span class="tex-font-style-tt">Yes</span>" (without quotes) if the required route of the tree exists, or "<span class="tex-font-style-tt">No</span>" (without quotes) otherwise.</p><p>If the required tree traversal exists, on the second line print $n$ integers of different integers $v_1, v_2, \ldots, v_n$ ($1 \le v_i \le n$)&nbsp;— the vertices of the tree in traversal order.</p><p>If there are several correct traversals, output any of them.</p>





```input1
5
1 2
1 3
3 4
3 5
```




```input2
3
1 2
1 3
```




```input3
15
1 2
1 3
2 4
2 5
3 6
3 7
4 8
4 9
5 10
5 11
6 12
6 13
7 14
7 15
```




```output1
Yes
4 5 1 2 3
```




```output2
Yes
1 2 3
```




```output3
No
```



## Note

<p>The tree from the first example is shown below. The bold arrows indicate the fox's route.</p><center> <img class="tex-graphics" src="file://LhpCUasS.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>In the second example, any sequence of three different vertices is a correct route, because the fox can jump from any vertex to any vertex.</p><p>The tree from the third example is shown below. It can be shown that there is no required route for it.</p><center> <img class="tex-graphics" src="file://ZLeAElrg.png" style="max-width: 100.0%;max-height: 100.0%;"> </center>
