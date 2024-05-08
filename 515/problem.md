## Description

<div><p>There are $n$ <span class="tex-font-style-bf">pairwise-distinct</span> points and a line $x+y=k$ on a two-dimensional plane. The $i$-th point is at $(x_i,y_i)$. All points have non-negative coordinates and are strictly below the line. Alternatively, $0 \leq x_i,y_i, x_i+y_i &lt; k$.</p><p>Tenzing wants to erase all the points. He can perform the following two operations:</p><ol> <li> Draw triangle: Tenzing will choose two non-negative integers $a$, $b$ that satisfy $a+b&lt;k$, then all points inside the triangle formed by lines $x=a$, $y=b$ and $x+y=k$ will be erased. It can be shown that this triangle is an isosceles right triangle. Let the side lengths of the triangle be $l$, $l$ and $\sqrt 2 l$ respectively. Then, the cost of this operation is $l \cdot A$.<p>The blue area of the following picture describes the triangle with $a=1,b=1$ with cost $=1\cdot A$.</p><center> <img class="tex-graphics" src="file://9ERoW8kf.png" style="max-width: 100.0%;max-height: 100.0%;"> </center></li><li> Erase a specific point: Tenzing will choose an integer $i$ that satisfies $1 \leq i \leq n$ and erase the point $i$. The cost of this operation is $c_i$.</li></ol><p>Help Tenzing find the minimum cost to erase all of the points.</p></div><div class="input-specification"><p>The first line of the input contains three integers $n$, $k$ and $A$ ($1\leq n,k\leq 2\cdot 10^5$, $1\leq A\leq 10^4$)&nbsp;— the number of points, the coefficient describing the hypotenuse of the triangle and the coefficient describing the cost of drawing a triangle.</p><p>The following $n$ lines of the input the $i$-th line contains three integers $x_i,y_i,c_i$ ($0\leq x_i,y_i,x_i+y_i&lt; k$, $1\leq c_i\leq 10^4$)&nbsp;— the coordinate of the $i$-th points and the cost of erasing it using the second operation. It is guaranteed that the coordinates are pairwise distinct.</p></div><div class="output-specification"><p>Output a single integer&nbsp;—the minimum cost needed to erase all of the points.</p></div>

## Input

<p>The first line of the input contains three integers $n$, $k$ and $A$ ($1\leq n,k\leq 2\cdot 10^5$, $1\leq A\leq 10^4$)&nbsp;— the number of points, the coefficient describing the hypotenuse of the triangle and the coefficient describing the cost of drawing a triangle.</p><p>The following $n$ lines of the input the $i$-th line contains three integers $x_i,y_i,c_i$ ($0\leq x_i,y_i,x_i+y_i&lt; k$, $1\leq c_i\leq 10^4$)&nbsp;— the coordinate of the $i$-th points and the cost of erasing it using the second operation. It is guaranteed that the coordinates are pairwise distinct.</p>

## Output

<p>Output a single integer&nbsp;—the minimum cost needed to erase all of the points.</p>





```input1
4 6 1
1 2 1
2 1 1
1 1 1
3 2 6
```




```input2
6 7 1
4 2 1
3 3 1
5 1 4
3 2 5
4 1 1
0 6 4
```




```input3
10 4 100
0 0 1
0 1 1
0 2 50
0 3 200
1 0 1
1 1 1
1 2 1
2 0 200
2 1 200
3 0 200
```




```output1
4
```




```output2
4
```




```output3
355
```



## Note

<p>The picture of the first example:</p><p>Tenzing do the following operations:</p><ol><li> draw a triangle with $a=3,b=2$, the cost $=1\cdot A=1$. </li><li> erase the first point, the cost $=1$. </li><li> erase the second point, the cost $=1$. </li><li> erase the third point, the cost $=1$.</li></ol><center> <img class="tex-graphics" src="file://6tP3qDB2.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>The picture of the second example: </p><center> <img class="tex-graphics" src="file://MnYF46l7.png" style="max-width: 100.0%;max-height: 100.0%;"> </center>
