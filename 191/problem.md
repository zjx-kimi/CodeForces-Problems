## Description

<div><p>Filip has a row of cells, some of which are blocked, and some are empty. He wants all empty cells to have water in them. He has two actions at his disposal:</p><ul> <li> $1$&nbsp;— place water in an empty cell. </li><li> $2$&nbsp;— remove water from a cell and place it in any other empty cell. </li></ul><p>If at some moment cell $i$ ($2 \le i \le n-1$) is empty and both cells $i-1$ and $i+1$ contains water, then it becomes filled with water.</p><p>Find the minimum number of times he needs to perform action $1$ in order to fill all empty cells with water. </p><p>Note that you don't need to minimize the use of action $2$. Note that blocked cells neither contain water nor can Filip place water in them.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 100$)&nbsp;— the number of cells. </p><p>The next line contains a string $s$ of length $n$. The $i$-th character of $s$ is '<span class="tex-font-style-tt">.</span>' if the cell $i$ is empty and '<span class="tex-font-style-tt">#</span>' if cell $i$ is blocked.</p></div><div class="output-specification"><p>For each test case, output a single number&nbsp;— the minimal amount of actions $1$ needed to fill all empty cells with water.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 100$)&nbsp;— the number of cells. </p><p>The next line contains a string $s$ of length $n$. The $i$-th character of $s$ is '<span class="tex-font-style-tt">.</span>' if the cell $i$ is empty and '<span class="tex-font-style-tt">#</span>' if cell $i$ is blocked.</p>

## Output

<p>For each test case, output a single number&nbsp;— the minimal amount of actions $1$ needed to fill all empty cells with water.</p>





```input1|2,3,6,7,10,11
5
3
...
7
##....#
7
..#.#..
4
####
10
#...#..#.#
```




```output1
2
2
5
0
2
```



## Note

<p><span class="tex-font-style-bf">Test Case 1</span></p><p>In the first test case, Filip can put water in cells $1$ and $3$. As cell $2$ is between $2$ cells with water, it gets filled with water too.</p><p><span class="tex-font-style-bf">Test Case 2</span></p><p>In the second case, he can put water sources in cells $3$ and $5$. That results in cell $4$ getting filled with water. Then he will remove water from cell $5$ and place it into cell $6$. As cell $5$'s neighbors, cell $4$ and cell $6$, have water in them, cell $5$ also gets filled with water. You can see the illustration of this case below.</p><center>  <img class="tex-graphics" src="file://knWQedwF.png" style="max-width: 100.0%;max-height: 100.0%;" width="720px">   <span class="tex-font-size-small">Operations in the second test case. White cells are empty, grey ones are blocked, and blue ones are water.</span> </center><p><span class="tex-font-style-bf">Test Case 3</span></p><p>In the third case, he can put water in all the empty cells. That requires $5$ actions of type $1$.</p><p><span class="tex-font-style-bf">Test Case 4</span></p><p>In the fourth case, there are no empty cells. Therefore, he does not have to put any water in them.</p><p><span class="tex-font-style-bf">Test Case 5</span></p><p>In the fifth test case, there exists a sequence of actions that requires only $2$ type $1$ actions.</p>
