## Description

<div><p>Hag is a very talented person. He has always had an artist inside him but his father forced him to study mechanical engineering.</p><p>Yesterday he spent all of his time cutting a giant piece of wood trying to make it look like a goose. Anyway, his dad found out that he was doing arts rather than studying mechanics and other boring subjects. He confronted Hag with the fact that he is a spoiled son that does not care about his future, and if he continues to do arts he will cut his 25 Lira monthly allowance.</p><p>Hag is trying to prove to his dad that the wooden piece is a project for mechanics subject. He also told his dad that the wooden piece is a <span class="tex-font-style-bf">strictly convex</span> polygon with $n$ vertices.</p><p>Hag brought two pins and pinned the polygon with them in the $1$-st and $2$-nd vertices to the wall. His dad has $q$ queries to Hag of two types. </p><ul> <li> $1$ $f$ $t$: pull a pin from the vertex $f$, wait for the wooden polygon to rotate under the gravity force (if it will rotate) and stabilize. And then put the pin in vertex $t$. </li><li> $2$ $v$: answer what are the coordinates of the vertex $v$. </li></ul><p>Please help Hag to answer his father's queries.</p><p>You can assume that the wood that forms the polygon has uniform density and the polygon has a positive thickness, same in all points. After every query of the 1-st type Hag's dad tries to move the polygon a bit and watches it stabilize again.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $q$ ($3\leq n \leq 10\,000$, $1 \leq q \leq 200000$)&nbsp;— the number of vertices in the polygon and the number of queries.</p><p>The next $n$ lines describe the wooden polygon, the $i$-th line contains two integers $x_i$ and $y_i$ ($|x_i|, |y_i|\leq 10^8$)&nbsp;— the coordinates of the $i$-th vertex of the polygon. It is guaranteed that polygon is strictly convex and the vertices are given in the counter-clockwise order and all vertices are distinct.</p><p>The next $q$ lines describe the queries, one per line. Each query starts with its type $1$ or $2$. Each query of the first type continues with two integers $f$ and $t$ ($1 \le f, t \le n$)&nbsp;— the vertex the pin is taken from, and the vertex the pin is put to and the polygon finishes rotating. It is guaranteed that the vertex $f$ contains a pin. Each query of the second type continues with a single integer $v$ ($1 \le v \le n$)&nbsp;— the vertex the coordinates of which Hag should tell his father.</p><p>It is guaranteed that there is at least one query of the second type.</p></div><div class="output-specification"><p>The output should contain the answer to each query of second type&nbsp;— two numbers in a separate line. Your answer is considered correct, if its absolute or relative error does not exceed $10^{-4}$.</p><p>Formally, let your answer be $a$, and the jury's answer be $b$. Your answer is considered correct if $\frac{|a - b|}{\max{(1, |b|)}} \le 10^{-4}$</p></div>

## Input

<p>The first line contains two integers $n$ and $q$ ($3\leq n \leq 10\,000$, $1 \leq q \leq 200000$)&nbsp;— the number of vertices in the polygon and the number of queries.</p><p>The next $n$ lines describe the wooden polygon, the $i$-th line contains two integers $x_i$ and $y_i$ ($|x_i|, |y_i|\leq 10^8$)&nbsp;— the coordinates of the $i$-th vertex of the polygon. It is guaranteed that polygon is strictly convex and the vertices are given in the counter-clockwise order and all vertices are distinct.</p><p>The next $q$ lines describe the queries, one per line. Each query starts with its type $1$ or $2$. Each query of the first type continues with two integers $f$ and $t$ ($1 \le f, t \le n$)&nbsp;— the vertex the pin is taken from, and the vertex the pin is put to and the polygon finishes rotating. It is guaranteed that the vertex $f$ contains a pin. Each query of the second type continues with a single integer $v$ ($1 \le v \le n$)&nbsp;— the vertex the coordinates of which Hag should tell his father.</p><p>It is guaranteed that there is at least one query of the second type.</p>

## Output

<p>The output should contain the answer to each query of second type&nbsp;— two numbers in a separate line. Your answer is considered correct, if its absolute or relative error does not exceed $10^{-4}$.</p><p>Formally, let your answer be $a$, and the jury's answer be $b$. Your answer is considered correct if $\frac{|a - b|}{\max{(1, |b|)}} \le 10^{-4}$</p>





```input1
3 4
0 0
2 0
2 2
1 1 2
2 1
2 2
2 3

```




```input2
3 2
-1 1
0 0
1 1
1 1 2
2 1

```




```output1
3.4142135624 -1.4142135624
2.0000000000 0.0000000000
0.5857864376 -1.4142135624

```




```output2
1.0000000000 -1.0000000000

```



## Note

<p>In the first test note the initial and the final state of the wooden polygon. </p><center> <img class="tex-graphics" src="file://cmq47zhu.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>Red Triangle is the initial state and the green one is the triangle after rotation around $(2,0)$.</p><p>In the second sample note that the polygon rotates $180$ degrees counter-clockwise or clockwise direction (it does not matter), because Hag's father makes sure that the polygon is stable and his son does not trick him.</p>
