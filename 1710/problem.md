## Description

<div><p>There are $n$ cars on a coordinate axis $OX$. Each car is located at an integer point initially and no two cars are located at the same point. Also, each car is oriented either left or right, and they can move at any constant positive speed in that direction at any moment.</p><p>More formally, we can describe the $i$-th car with a letter and an integer: its orientation $ori_i$ and its location $x_i$. If $ori_i = L$, then $x_i$ is decreasing at a constant rate with respect to time. Similarly, if $ori_i = R$, then $x_i$ is increasing at a constant rate with respect to time. </p><p>We call two cars <span class="tex-font-style-bf">irrelevant</span> if they never end up in the same point regardless of their speed. In other words, they won't share the same coordinate at any moment.</p><p>We call two cars <span class="tex-font-style-bf">destined</span> if they always end up in the same point regardless of their speed. In other words, they must share the same coordinate at some moment.</p><p>Unfortunately, we lost all information about our cars, but we do remember $m$ relationships. There are two types of relationships:</p><p>$1$ $i$ $j$ —$i$-th car and $j$-th car are <span class="tex-font-style-bf">irrelevant</span>.</p><p>$2$ $i$ $j$ —$i$-th car and $j$-th car are <span class="tex-font-style-bf">destined</span>.</p><p>Restore the orientations and the locations of the cars satisfying the relationships, or report that it is impossible. If there are multiple solutions, you can output any.</p><p>Note that if two cars share the same coordinate, they will intersect, but at the same moment they will continue their movement in their directions.</p></div><div class="input-specification"><p>The first line contains two integers, $n$ and $m$ $(2 \leq n \leq 2 \cdot 10^5; 1 \leq m \leq min(2 \cdot 10^5, \frac{n(n-1)}{2})$ — the number of cars and the number of restrictions respectively.</p><p>Each of the next $m$ lines contains three integers, $type$, $i$, and $j$ $(1 \leq type \leq 2; 1 \leq i,j \leq n; i≠j)$.</p><p>If $type$ = $1$, $i$-th car and $j$-th car are <span class="tex-font-style-bf">irrelevant</span>. Otherwise, $i$-th car and $j$-th car are <span class="tex-font-style-bf">destined</span>.</p><p>It is guaranteed that for each pair of cars, there are at most $1$ relationship between.</p></div><div class="output-specification"><p>In the first line, print either "<span class="tex-font-style-tt">YES</span>" or "<span class="tex-font-style-tt">NO</span>" (in any case), whether it is possible to restore the orientations and the locations of the cars satisfying the relationships.</p><p>If the answer is "<span class="tex-font-style-tt">YES</span>", print $n$ lines each containing a symbol and an integer: $ori_i$ and $x_i$ $(ori_i \in \{L, R\}; -10^9 \leq x_i \leq 10^9)$ — representing the information of the $i$-th car.</p><p>If the orientation is left, then $ori_i$ = $L$. Otherwise $ori_i$ = $R$.</p><p>$x_i$ is the where the $i$-th car is located. Note that all $x_i$ should be <span class="tex-font-style-bf">distinct</span>. </p><p>We can prove that if there exists a solution, then there must be a solution satisfying the constraints on $x_i$.</p></div>

## Input

<p>The first line contains two integers, $n$ and $m$ $(2 \leq n \leq 2 \cdot 10^5; 1 \leq m \leq min(2 \cdot 10^5, \frac{n(n-1)}{2})$ — the number of cars and the number of restrictions respectively.</p><p>Each of the next $m$ lines contains three integers, $type$, $i$, and $j$ $(1 \leq type \leq 2; 1 \leq i,j \leq n; i≠j)$.</p><p>If $type$ = $1$, $i$-th car and $j$-th car are <span class="tex-font-style-bf">irrelevant</span>. Otherwise, $i$-th car and $j$-th car are <span class="tex-font-style-bf">destined</span>.</p><p>It is guaranteed that for each pair of cars, there are at most $1$ relationship between.</p>

## Output

<p>In the first line, print either "<span class="tex-font-style-tt">YES</span>" or "<span class="tex-font-style-tt">NO</span>" (in any case), whether it is possible to restore the orientations and the locations of the cars satisfying the relationships.</p><p>If the answer is "<span class="tex-font-style-tt">YES</span>", print $n$ lines each containing a symbol and an integer: $ori_i$ and $x_i$ $(ori_i \in \{L, R\}; -10^9 \leq x_i \leq 10^9)$ — representing the information of the $i$-th car.</p><p>If the orientation is left, then $ori_i$ = $L$. Otherwise $ori_i$ = $R$.</p><p>$x_i$ is the where the $i$-th car is located. Note that all $x_i$ should be <span class="tex-font-style-bf">distinct</span>. </p><p>We can prove that if there exists a solution, then there must be a solution satisfying the constraints on $x_i$.</p>





```input1
4 4
1 1 2
1 2 3
2 3 4
2 4 1
```




```input2
3 3
1 1 2
1 2 3
1 1 3
```




```output1
YES
R 0
L -3
R 5
L 6
```




```output2
NO
```


