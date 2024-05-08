## Description

<div><p>Once the mischievous and wayward shooter named Shel found himself on a rectangular field of size $n \times m$, divided into unit squares. Each cell either contains a target or not.</p><p>Shel only had a lucky shotgun with him, with which he can shoot in one of the four directions: right-down, left-down, left-up, or right-up. When fired, the shotgun hits all targets in the chosen direction, the Manhattan distance to which does not exceed a fixed constant $k$. The Manhattan distance between two points $(x_1, y_1)$ and $(x_2, y_2)$ is equal to $|x_1 - x_2| + |y_1 - y_2|$.</p><center> <img class="tex-graphics" src="file://CMk7BzuV.png" style="max-width: 100.0%;max-height: 100.0%;">   <span class="tex-font-size-small">Possible hit areas for $k = 3$.</span> </center><p>Shel's goal is to hit as many targets as possible. Please help him find this value.</p></div><div class="input-specification"><p>Each test consists of several test cases. The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases. Then follows the description of the test cases.</p><p>The first line of each test case contains field dimensions $n$, $m$, and the constant for the shotgun's power $k$ ($1 \le n, m, k \le 10^5, 1 \le n \cdot m \le 10^5$).</p><p>Each of the next $n$ lines contains $m$ characters — the description of the next field row, where the character '<span class="tex-font-style-tt">.</span>' means the cell is empty, and the character '<span class="tex-font-style-tt">#</span>' indicates the presence of a target. </p><p>It is guaranteed that the sum of $n \cdot m$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer on a separate line, which is equal to the maximum possible number of hit targets with one shot.</p></div>

## Input

<p>Each test consists of several test cases. The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases. Then follows the description of the test cases.</p><p>The first line of each test case contains field dimensions $n$, $m$, and the constant for the shotgun's power $k$ ($1 \le n, m, k \le 10^5, 1 \le n \cdot m \le 10^5$).</p><p>Each of the next $n$ lines contains $m$ characters — the description of the next field row, where the character '<span class="tex-font-style-tt">.</span>' means the cell is empty, and the character '<span class="tex-font-style-tt">#</span>' indicates the presence of a target. </p><p>It is guaranteed that the sum of $n \cdot m$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output a single integer on a separate line, which is equal to the maximum possible number of hit targets with one shot.</p>





```input1|2,3,4,5,9,10,11,12,13
4
3 3 1
.#.
###
.#.
2 5 3
###..
...##
4 4 2
..##
###.
#..#
####
2 1 3
#
#
```




```output1
3
4
5
2
```



## Note

<p>Possible optimal shots for the examples in the statement:</p><center> <img class="tex-graphics" src="file://vqn6Cx4S.png" style="max-width: 100.0%;max-height: 100.0%;"> </center>
