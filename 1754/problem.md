## Description

<div><p>You are given a tree consisting of $n$ vertices. Some of the vertices (at least two) are black, all the other vertices are white.</p><p>You place a chip on one of the vertices of the tree, and then perform the following operations:</p><ul> <li> let the current vertex where the chip is located is $x$. You choose a black vertex $y$, and then move the chip along the first edge on the simple path from $x$ to $y$. </li></ul><p>You are not allowed to choose the same black vertex $y$ in two operations in a row (i. e., for every two consecutive operations, the chosen black vertex should be different).</p><p>You end your operations when the chip moves to the black vertex (if it is initially placed in a black vertex, you don't perform the operations at all), or when the number of performed operations exceeds $100^{500}$.</p><p>For every vertex $i$, you have to determine if there exists a (possibly empty) sequence of operations that moves the chip to some black vertex, if the chip is initially placed on the vertex $i$.</p></div><div class="input-specification"><p>The first line contains one integer $n$ ($3 \le n \le 3 \cdot 10^5$) — the number of vertices in the tree.</p><p>The second line contains $n$ integers $c_1, c_2, \dots, c_n$ ($0 \le c_i \le 1$), where $c_i = 0$ means that the $i$-th vertex is white, and $c_i = 1$ means that the $i$-th vertex is black. At least two values of $c_i$ are equal to $1$.</p><p>Then $n-1$ lines follow, each of them contains two integers $u_i$ and $v_i$ ($1 \le u_i, v_i \le n$; $u_i \ne v_i$) — the endpoints of some edge. These edges form a tree.</p></div><div class="output-specification"><p>Print $n$ integers. The $i$-th integer should be equal to $1$ if there exists a (possibly empty) sequence of operations that moves the chip to some black vertex if it is placed on the vertex $i$, and $0$ if no such sequence of operations exists.</p></div>

## Input

<p>The first line contains one integer $n$ ($3 \le n \le 3 \cdot 10^5$) — the number of vertices in the tree.</p><p>The second line contains $n$ integers $c_1, c_2, \dots, c_n$ ($0 \le c_i \le 1$), where $c_i = 0$ means that the $i$-th vertex is white, and $c_i = 1$ means that the $i$-th vertex is black. At least two values of $c_i$ are equal to $1$.</p><p>Then $n-1$ lines follow, each of them contains two integers $u_i$ and $v_i$ ($1 \le u_i, v_i \le n$; $u_i \ne v_i$) — the endpoints of some edge. These edges form a tree.</p>

## Output

<p>Print $n$ integers. The $i$-th integer should be equal to $1$ if there exists a (possibly empty) sequence of operations that moves the chip to some black vertex if it is placed on the vertex $i$, and $0$ if no such sequence of operations exists.</p>





```input1
8
0 1 0 0 0 0 1 0
8 6
2 5
7 8
6 5
4 5
6 1
7 3
```




```output1
0 1 1 1 1 0 1 1
```


