## Description

<div><p>There are $N$ bubbles in a coordinate plane. Bubbles are so tiny that it can be assumed that each bubble is a point $(X_i, Y_i)$. </p><p>$Q$ Bubble Cup finalists plan to play with the bubbles. Each finalist would link to use infinitely long Bubble Cup stick to pop some bubbles. The $i$-th finalist would like to place the stick in the direction of vector $(dxi, dyi)$, and plays the following game until $K_i$ bubbles are popped. The game starts with finalist placing the stick in the direction of vector $(dx_i, dy_i)$, and sweeping it from the infinity to the left until it hits some bubble, which is immediately popped. It is guaranteed that only one bubble will be hit in this step. After that the finalist starts rotating the stick in the counter clockwise direction with the center of rotation in point where the previous bubble was popped. When the next bubble is hit, it is immediately popped and becomes the new center of rotation. The process continues until $K_i$ bubbles have been popped. It is guaranteed that the stick won't hit two bubbles simultaneously in this process. </p><p>For each finalist find which bubble would be popped the last. Note that each game starts with the configuration of all $N$ bubbles, so the games don't depend on the previous games. </p></div><div class="input-specification"><p>The first line contains one integer $N$ — the number of bubbles. ($1 \leq N \leq 10^5$)</p><p>Each of the next $N$ lines contains two integers. The $i$-th line contains integers $X_i$ and $Y_i$ — the coordinates of the $i$-th bubble. ($-10^9 \leq X_i, Y_i \leq 10^9$, $(X_i, Y_i) \neq (X_j, Y_j)$ for $i \neq j$)</p><p>The next line contains one integer $Q$ — the number of finalists willing to play with the bubbles. ($1 \leq Q \leq 10^5$)</p><p>Each of the next Q lines contains 3 integers. The $i$-th line contains integers $dx_i$, $dy_i$ and $K_i$. ($-10^9 \leq dx_i, dy_i \leq 10^9$, $1 \leq K_i \leq N$)</p></div><div class="output-specification"><p>For each of the $Q$ finalists, print the index of the bubble which would be popped last, in the separate line. </p></div>

## Input

<p>The first line contains one integer $N$ — the number of bubbles. ($1 \leq N \leq 10^5$)</p><p>Each of the next $N$ lines contains two integers. The $i$-th line contains integers $X_i$ and $Y_i$ — the coordinates of the $i$-th bubble. ($-10^9 \leq X_i, Y_i \leq 10^9$, $(X_i, Y_i) \neq (X_j, Y_j)$ for $i \neq j$)</p><p>The next line contains one integer $Q$ — the number of finalists willing to play with the bubbles. ($1 \leq Q \leq 10^5$)</p><p>Each of the next Q lines contains 3 integers. The $i$-th line contains integers $dx_i$, $dy_i$ and $K_i$. ($-10^9 \leq dx_i, dy_i \leq 10^9$, $1 \leq K_i \leq N$)</p>

## Output

<p>For each of the $Q$ finalists, print the index of the bubble which would be popped last, in the separate line. </p>





```input1
4
0 0
1 0
0 1
1 1
2
1 -1 3
-1 1 4
```




```input2
4
1 1
2 2
7 1
1 7
3
2 2 1
1 -5 4
-6 5 3
```




```output1
4
2
```




```output2
3
2
3
```



## Note

<p>There are two finalists willing to play with the bubbles. If the first finalist plays with the bubbles, then the bubbles at coordinates (0, 0), (1, 0) and (1, 1) would be popped in that order. Their indexes are 1, 2 and 4, so the answer is 4. If the second finalist plays with the bubbles, then the bubbles at coordinates (1, 1), (0, 1), (0, 0) and (1, 0) would be popped in that order, so the answer is 2.</p><p>Visualization: <a href="https://petljamediastorage.blob.core.windows.net/uploads/example1.gif">link</a>. </p>
