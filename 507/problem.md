## Description

<div><p>Timofey has an apple tree growing in his garden; it is a rooted tree of $n$ vertices with the root in vertex $1$ (the vertices are numbered from $1$ to $n$). A tree is a connected graph without loops and multiple edges.</p><p>This tree is very unusual&nbsp;— it grows with its root upwards. However, it's quite normal for programmer's trees.</p><p>The apple tree is quite young, so only two apples will grow on it. Apples will grow in certain vertices (these vertices may be the same). After the apples grow, Timofey starts shaking the apple tree until the apples fall. Each time Timofey shakes the apple tree, the following happens to each of the apples:</p><p>Let the apple now be at vertex $u$.</p><ul> <li> If a vertex $u$ has a child, the apple moves to it (if there are several such vertices, the apple can move to any of them). </li><li> Otherwise, the apple falls from the tree. </li></ul><p>It can be shown that after a finite time, both apples will fall from the tree.</p><p>Timofey has $q$ assumptions in which vertices apples can grow. He assumes that apples can grow in vertices $x$ and $y$, and wants to know the number of pairs of vertices ($a$, $b$) from which apples can fall from the tree, where $a$&nbsp;— the vertex from which an apple from vertex $x$ will fall, $b$&nbsp;— the vertex from which an apple from vertex $y$ will fall. Help him do this.</p></div><div class="input-specification"><p>The first line contains integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains integer $n$ ($2 \leq n \leq 2 \cdot 10^5$)&nbsp;— the number of vertices in the tree.</p><p>Then there are $n - 1$ lines describing the tree. In line $i$ there are two integers $u_i$ and $v_i$ ($1 \leq u_i, v_i \leq n$, $u_i \ne v_i$)&nbsp;— edge in tree.</p><p>The next line contains a single integer $q$ ($1 \leq q \leq 2 \cdot 10^5$)&nbsp;— the number of Timofey's assumptions.</p><p>Each of the next $q$ lines contains two integers $x_i$ and $y_i$ ($1 \leq x_i, y_i \leq n$)&nbsp;— the supposed vertices on which the apples will grow for the assumption $i$.</p><p>It is guaranteed that the sum of $n$ does not exceed $2 \cdot 10^5$. Similarly, It is guaranteed that the sum of $q$ does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each Timofey's assumption output the number of ordered pairs of vertices from which apples can fall from the tree if the assumption is true on a separate line.</p></div>

## Input

<p>The first line contains integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains integer $n$ ($2 \leq n \leq 2 \cdot 10^5$)&nbsp;— the number of vertices in the tree.</p><p>Then there are $n - 1$ lines describing the tree. In line $i$ there are two integers $u_i$ and $v_i$ ($1 \leq u_i, v_i \leq n$, $u_i \ne v_i$)&nbsp;— edge in tree.</p><p>The next line contains a single integer $q$ ($1 \leq q \leq 2 \cdot 10^5$)&nbsp;— the number of Timofey's assumptions.</p><p>Each of the next $q$ lines contains two integers $x_i$ and $y_i$ ($1 \leq x_i, y_i \leq n$)&nbsp;— the supposed vertices on which the apples will grow for the assumption $i$.</p><p>It is guaranteed that the sum of $n$ does not exceed $2 \cdot 10^5$. Similarly, It is guaranteed that the sum of $q$ does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each Timofey's assumption output the number of ordered pairs of vertices from which apples can fall from the tree if the assumption is true on a separate line.</p>





```input1|2,3,4,5,6,7,8,9,10,11
2
5
1 2
3 4
5 3
3 2
4
3 4
5 1
4 4
1 3
3
1 2
1 3
3
1 1
2 3
3 1
```




```input2|2,3,4,5,6,7,8,9
2
5
5 1
1 2
2 3
4 3
2
5 5
5 1
5
3 2
5 3
2 1
4 2
3
4 3
2 1
4 2
```




```output1
2
2
1
4
4
1
2
```




```output2
1
2
1
4
2
```



## Note

<p>In the first example: </p><ul> <li> For the first assumption, there are two possible pairs of vertices from which apples can fall from the tree: $(4, 4), (5, 4)$. </li><li> For the second assumption there are also two pairs: $(5, 4), (5, 5)$. </li><li> For the third assumption there is only one pair: $(4, 4)$. </li><li> For the fourth assumption, there are $4$ pairs: $(4, 4), (4, 5), (5, 4), (5, 5)$. </li></ul><center> <img class="tex-graphics" src="file://VTpChCsR.png" style="max-width: 100.0%;max-height: 100.0%;">   <span class="tex-font-size-small">Tree from the first example.</span> </center><p>For the second example, there are $4$ of possible pairs of vertices from which apples can fall: $(2, 3), (2, 2), (3, 2), (3, 3)$. For the second assumption, there is only one possible pair: $(2, 3)$. For the third assumption, there are two pairs: $(3, 2), (3, 3)$.</p>
