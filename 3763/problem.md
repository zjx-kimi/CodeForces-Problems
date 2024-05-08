## Description

<div><p>Bob Bubblestrong just got a new job as security guard. Bob is now responsible for safety of a collection of warehouses, each containing the most valuable Bubble Cup assets - the high-quality bubbles. His task is to detect thieves inside the warehouses and call the police.</p><p>Looking from the sky, each warehouse has a shape of a convex polygon. Walls of no two warehouses intersect, and of course, none of the warehouses is built inside of another warehouse.</p><p>Little did the Bubble Cup bosses know how lazy Bob is and that he enjoys watching soap operas (he heard they are full of bubbles) from the coziness of his office. Instead of going from one warehouse to another to check if warehouses are secured, the plan Bob has is to monitor all the warehouses from the comfort of his office using the special X-ray goggles. The goggles have an infinite range, so a thief in any of the warehouses could easily be spotted.</p><p>However, the goggles promptly broke and the X-rays are now strong only enough to let Bob see through a single wall. Now, Bob would really appreciate if you could help him find out what is the total area inside of the warehouses monitored by the broken goggles, so that he could know how much area of the warehouses he needs to monitor in person.</p></div><div class="input-specification"><p>The first line contains one integer $N$ ($1$ $\leq$ $N$ $\leq$ $10^4$) – the number of warehouses.</p><p>The next $N$ lines describe the warehouses.</p><p>The first number of the line is integer $c_i$ ($3$ $\leq$ $c_i$ $\leq$ $10^4$) – the number corners in the $i^{th}$ warehouse, followed by $c_i$ pairs of integers. The $j^{th}$ pair is $(x_j, y_j)$ – the coordinates of the $j^{th}$ corner ($|x_j|$, $|y_j|$ $\leq$ $3 * 10^4$). The corners are listed in the clockwise order. The total number of corners in all the warehouses is at most $5 * 10^4$.</p><p>Bob's office is positioned at the point with coordinates $(0, 0)$. The office is not contained within any of the warehouses.</p></div><div class="output-specification"><p>Print a single line containing a single decimal number accurate to at least four decimal places – the total area of the warehouses Bob can monitor using the broken X-ray goggles.</p></div>

## Input

<p>The first line contains one integer $N$ ($1$ $\leq$ $N$ $\leq$ $10^4$) – the number of warehouses.</p><p>The next $N$ lines describe the warehouses.</p><p>The first number of the line is integer $c_i$ ($3$ $\leq$ $c_i$ $\leq$ $10^4$) – the number corners in the $i^{th}$ warehouse, followed by $c_i$ pairs of integers. The $j^{th}$ pair is $(x_j, y_j)$ – the coordinates of the $j^{th}$ corner ($|x_j|$, $|y_j|$ $\leq$ $3 * 10^4$). The corners are listed in the clockwise order. The total number of corners in all the warehouses is at most $5 * 10^4$.</p><p>Bob's office is positioned at the point with coordinates $(0, 0)$. The office is not contained within any of the warehouses.</p>

## Output

<p>Print a single line containing a single decimal number accurate to at least four decimal places – the total area of the warehouses Bob can monitor using the broken X-ray goggles.</p>





```input1
5
4 1 1 1 3 3 3 3 1
4 4 3 6 2 6 0 4 0
6 -5 3 -4 4 -3 4 -2 3 -3 2 -4 2
3 0 -1 1 -3 -1 -3
4 1 -4 1 -6 -1 -6 -1 -4
```




```output1
13.333333333333
```



## Note

<center> <img class="tex-graphics" src="file://NUNMnSKE.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>Areas monitored by the X-ray goggles are colored green and areas not monitored by the goggles are colored red.</p><p>The warehouses $ABCD$, $IJK$ and $LMNOPQ$ are completely monitored using the googles.</p><p>The warehouse $EFGH$ is partially monitored using the goggles: part $EFW$ is not monitored because to monitor each point inside it, the X-rays must go through two walls of warehouse $ABCD$.</p><p>The warehouse $RUTS$ is not monitored from the Bob's office, because there are two walls of the warehouse $IJK$ between Bob's office and each point in $RUTS$.</p><p>The total area monitored by the goggles is $P$ = $P_{ABCD}$ + $P_{FGHW}$ + $P_{IJK}$ + $P_{LMNOPQ}$ = $4$ + $3.333333333333$ + $2$ + $4$ = $13.333333333333$.</p>
