## Description

<div><p><span class="tex-font-style-bf">The only difference between the two versions of this problem is the constraint on $q$. You can make hacks only if both versions of the problem are solved.</span></p><p>Thomas is sailing around an island surrounded by the ocean. The ocean and island can be represented by a grid with $n$ rows and $m$ columns. The rows are numbered from $1$ to $n$ from top to bottom, and the columns are numbered from $1$ to $m$ from left to right. The position of a cell at row $r$ and column $c$ can be represented as $(r, c)$. Below is an example of a valid grid.</p><center> <img class="tex-graphics" src="file://ziwgrp1p.png" style="max-width: 100.0%;max-height: 100.0%;" width="302px"> <span class="tex-font-size-small">Example of a valid grid</span> </center><p>There are three types of cells: island, ocean and underwater volcano. Cells representing the island are marked with a '<span class="tex-font-style-tt">#</span>', cells representing the ocean are marked with a '<span class="tex-font-style-tt">.</span>', and cells representing an underwater volcano are marked with a '<span class="tex-font-style-tt">v</span>'. It is guaranteed that there is at least one island cell and at least one underwater volcano cell. It is also guaranteed that the set of all island cells forms a single connected component$^{\dagger}$ and the set of all ocean cells and underwater volcano cells forms a single connected component. Additionally, it is guaranteed that there are no island cells at the edge of the grid (that is, at row $1$, at row $n$, at column $1$, and at column $m$).</p><p>Define a <span class="tex-font-style-it">round trip</span> starting from cell $(x, y)$ as a path Thomas takes which satisfies the following conditions:</p><ul> <li> The path starts and ends at $(x, y)$. </li><li> If Thomas is at cell $(i, j)$, he can go to cells $(i+1, j)$, $(i-1, j)$, $(i, j-1)$, and $(i, j+1)$ as long as the destination cell <span class="tex-font-style-bf">is an ocean cell or an underwater volcano cell</span> and is still inside the grid. Note that it is allowed for Thomas to visit the same cell multiple times in the same round trip. </li><li> The path must go around the island and fully encircle it. Some path $p$ fully encircles the island if it is impossible to go from an island cell to a cell on the grid border by only traveling <span class="tex-font-style-bf">to adjacent on a side or diagonal</span> cells without visiting a cell on path $p$. In the image below, the path starting from $(2, 2)$, going to $(1, 3)$, and going back to $(2, 2)$ the other way does <span class="tex-font-style-bf">not</span> fully encircle the island and is not considered a round trip. </li></ul><center> <img class="tex-graphics" src="file://bk5MfSVD.png" style="max-width: 100.0%;max-height: 100.0%;" width="302px"> <span class="tex-font-size-small">Example of a path that does <span class="tex-font-style-bf">not</span> fully encircle the island</span> </center><p>The <span class="tex-font-style-it">safety</span> of a round trip is the minimum Manhattan distance$^{\ddagger}$ from a cell on the round trip to an underwater volcano (note that the presence of island cells does not impact this distance).</p><p>You have $q$ queries. A query can be represented as $(x, y)$ and for every query, you want to find the maximum safety of a round trip starting from $(x, y)$. It is guaranteed that $(x, y)$ is an ocean cell or an underwater volcano cell.</p><p>$^{\dagger}$A set of cells forms a single connected component if from any cell of this set it is possible to reach any other cell of this set by moving only through the cells of this set, each time going to a cell <span class="tex-font-style-bf">with a common side</span>.</p><p>$^{\ddagger}$Manhattan distance between cells $(r_1, c_1)$ and $(r_2, c_2)$ is equal to $|r_1 - r_2| + |c_1 - c_2|$.</p></div><div class="input-specification"><p>The first line contains three integers $n$, $m$, and $q$ ($3 \leq n, m \leq 10^5$, $9 \leq n \cdot m \leq 3 \cdot 10^5$, $1 \leq q \leq 3 \cdot 10^5$) — the number of rows and columns of the grid and the number of queries. </p><p>Each of the following $n$ lines contains $m$ characters describing the cells of the grid. The character '<span class="tex-font-style-tt">#</span>' denotes an island cell, '<span class="tex-font-style-tt">.</span>' denotes an ocean cell, and '<span class="tex-font-style-tt">v</span>' denotes an underwater volcano cell.</p><p>It is guaranteed that there is at least one island cell and at least one underwater volcano cell. It is guaranteed that the set of all island cells forms a single connected component and the set of all ocean cells and underwater volcano cells forms a single connected component. Also, it is guaranteed that there are no island cells at the edge of the grid (that is, at the row $1$, at the row $n$, at the column $1$, and at the column $m$).</p><p>The following $q$ lines describe the queries. Each of these lines contains two integers $x$ and $y$ ($1 \leq x \leq n$, $1 \leq y \leq m$) denoting a round trip starting from $(x, y)$.</p><p>It is guaranteed that $(x, y)$ is an ocean cell or an underwater volcano cell.</p></div><div class="output-specification"><p>For each query, output a single integer — the maximum safety of a round trip starting from the specified position.</p></div>

## Input

<p>The first line contains three integers $n$, $m$, and $q$ ($3 \leq n, m \leq 10^5$, $9 \leq n \cdot m \leq 3 \cdot 10^5$, $1 \leq q \leq 3 \cdot 10^5$) — the number of rows and columns of the grid and the number of queries. </p><p>Each of the following $n$ lines contains $m$ characters describing the cells of the grid. The character '<span class="tex-font-style-tt">#</span>' denotes an island cell, '<span class="tex-font-style-tt">.</span>' denotes an ocean cell, and '<span class="tex-font-style-tt">v</span>' denotes an underwater volcano cell.</p><p>It is guaranteed that there is at least one island cell and at least one underwater volcano cell. It is guaranteed that the set of all island cells forms a single connected component and the set of all ocean cells and underwater volcano cells forms a single connected component. Also, it is guaranteed that there are no island cells at the edge of the grid (that is, at the row $1$, at the row $n$, at the column $1$, and at the column $m$).</p><p>The following $q$ lines describe the queries. Each of these lines contains two integers $x$ and $y$ ($1 \leq x \leq n$, $1 \leq y \leq m$) denoting a round trip starting from $(x, y)$.</p><p>It is guaranteed that $(x, y)$ is an ocean cell or an underwater volcano cell.</p>

## Output

<p>For each query, output a single integer — the maximum safety of a round trip starting from the specified position.</p>





```input1
9 9 3
.........
.........
....###..
...v#....
..###....
...##...v
...##....
.........
v........
1 1
9 1
5 7
```




```input2
3 3 5
..v
.#.
...
1 2
1 3
2 3
2 1
3 2
```




```input3
14 13 5
.............
.............
.............
...vvvvvvv...
...v.....v...
...v.###.v...
...v.#.#.v...
...v..v..v...
...v..v..v...
....v...v....
.....vvv.....
.............
.............
.............
1 1
7 7
5 6
4 10
13 6
```




```input4
10 11 4
...........
..#######..
..#..#..#..
..#.....#..
..#..v..#..
..#.###.#..
..#.#.#.#..
..#...#.#..
..#####.#..
...........
7 6
3 7
6 8
1 1
```




```output1
3
0
3
```




```output2
0
0
0
0
0
```




```output3
3
0
1
0
2
```




```output4
1
2
3
4
```



## Note

<p>For the first example, the image below shows an optimal round trip starting from $(1, 1)$. The round trip has a safety of $3$ as the minimum Manhattan distance from a cell on the round trip to an underwater volcano is $3$.</p><center> <img class="tex-graphics" src="file://1YcImZkI.png" style="max-width: 100.0%;max-height: 100.0%;" width="302px"> <span class="tex-font-size-small">Example of an optimal round trip</span> </center><p>For the fourth example, remember that it is allowed for Thomas to visit the same cell multiple times in the same round trip. For example, doing so is necessary for the round trip starting from $(7, 6)$.</p>
