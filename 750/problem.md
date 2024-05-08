## Description

<div><p>You are given $n \times m$ grid. Some cells are filled and some are empty.</p><p>A <span class="tex-font-style-it">city</span> is a maximal (by inclusion) set of filled cells such that it is possible to get from any cell in the set to any other cell in the set by moving to adjacent (by side) cells, without moving into any cells not in the set. In other words, a city is a connected component of filled cells with edges between adjacent (by side) cells.</p><p>Initially, there are <span class="tex-font-style-bf">two cities</span> on the grid. You want to change some empty cells into filled cells so that both of the following are satisfied: </p><ul> <li> There is <span class="tex-font-style-bf">one city</span> on the resulting grid. </li><li> The shortest path between any two filled cells, achievable only by moving onto filled cells, is equal to the Manhattan distance between them. </li></ul><p>The <span class="tex-font-style-it">Manhattan distance</span> between two cells $(a, b)$ and $(c, d)$ is equal to $|a - c| + |b - d|$.</p><p>Find a way to add filled cells that satisfies these conditions and minimizes the total number of filled cells.</p></div><div class="input-specification"><p>Input consists of multiple test cases. The first line contains a single integer $t$, the number of test cases ($1 \le t \le 5000$).</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \le n, m \le 50$, $nm \geq 3$).</p><p>The next $n$ lines describe the grid. The $i$-th line contains a string $s_i$ of length $m$. $s_{i,j}$ is '<span class="tex-font-style-tt">#</span>' if the cell in position $(i, j)$ is filled, and '<span class="tex-font-style-tt">.</span>' if it is empty.</p><p>It is guaranteed that there are <span class="tex-font-style-bf">exactly two cities</span> in the initial grid.</p><p>It is guaranteed that the sum of $n\cdot m$ over all test cases does not exceed $25\,000$.</p></div><div class="output-specification"><p>For each test case, output $n$ lines, each containing a string of length $m$, describing the grid you create in the same format as the input.</p><p>If there are multiple possible answers with the minimum number of filled cells print any.</p></div>

## Input

<p>Input consists of multiple test cases. The first line contains a single integer $t$, the number of test cases ($1 \le t \le 5000$).</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \le n, m \le 50$, $nm \geq 3$).</p><p>The next $n$ lines describe the grid. The $i$-th line contains a string $s_i$ of length $m$. $s_{i,j}$ is '<span class="tex-font-style-tt">#</span>' if the cell in position $(i, j)$ is filled, and '<span class="tex-font-style-tt">.</span>' if it is empty.</p><p>It is guaranteed that there are <span class="tex-font-style-bf">exactly two cities</span> in the initial grid.</p><p>It is guaranteed that the sum of $n\cdot m$ over all test cases does not exceed $25\,000$.</p>

## Output

<p>For each test case, output $n$ lines, each containing a string of length $m$, describing the grid you create in the same format as the input.</p><p>If there are multiple possible answers with the minimum number of filled cells print any.</p>





```input1|2,3,7,8,9,10,11,19,20,21,22,23,24,25,32,33,34,35,36,43,44,45,46,47,48,56,57,58,59,60,61
11
1 3
#.#
2 2
.#
#.
4 4
..##
...#
#...
##..
6 6
.##...
##....
......
....##
.....#
...###
6 5
.#..#
.#..#
.#..#
.#.##
.#...
##...
5 5
#####
#...#
#.#.#
#...#
#####
4 4
.##.
##.#
#.##
.##.
5 5
..###
....#
.....
#....
#....
5 6
.##...
##....
#....#
....##
...##.
6 5
..##.
...##
....#
#....
##...
.##..
5 4
..##
..#.
..#.
#...
#...
```




```output1
###

.#
##

..##
..##
###.
##..

.##...
###...
..#...
..####
...###
...###

.####
.####
.####
.####
.#...
##...

#####
#####
#####
#####
#####

.##.
####
####
.##.

..###
..###
..#..
###..
#....

.##...
###...
######
...###
...##.

..##.
..###
..###
###..
###..
.##..

..##
..#.
..#.
###.
#...
```



## Note

<p>In the first test case, we can add a single filled cell between the two cities to connect them. We can verify that the second condition is satisfied.</p><p>In the second test case, we can also connect the cities with a single filled cell, while satisfying the second condition. </p><p>In the third test case, note that if we filled the 3 cells in the top left, the cities would be connected, but the second condition would not be satisfied for cells $(4, 2)$ and $(2, 4)$.</p>
