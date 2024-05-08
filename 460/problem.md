## Description

<div><p>Vlad remembered that he had a series of $n$ tiles and a number $k$. The tiles were numbered from left to right, and the $i$-th tile had colour $c_i$.</p><p>If you stand on the <span class="tex-font-style-bf">first</span> tile and start jumping any number of tiles <span class="tex-font-style-bf">right</span>, you can get a path of length $p$. The length of the path is the number of tiles you stood on.</p><p>Vlad wants to see if it is possible to get a path of length $p$ such that: </p><ul> <li> it ends at tile with index $n$; </li><li> $p$ is divisible by $k$ </li><li> the path is divided into blocks of length exactly $k$ each; </li><li> tiles in each block have the same colour, the colors in adjacent blocks are not necessarily different. </li></ul><p>For example, let $n = 14$, $k = 3$.</p><p>The colours of the tiles are contained in the array $c$ = [$\color{red}{1}, \color{violet}{2}, \color{red}{1}, \color{red}{1}, \color{gray}{7}, \color{orange}{5}, \color{green}{3}, \color{green}{3}, \color{red}{1}, \color{green}{3}, \color{blue}{4}, \color{blue}{4}, \color{violet}{2}, \color{blue}{4}$]. Then we can construct a path of length $6$ consisting of $2$ blocks:</p><p>$\color{red}{c_1} \rightarrow \color{red}{c_3} \rightarrow \color{red}{c_4} \rightarrow \color{blue}{c_{11}} \rightarrow \color{blue}{c_{12}} \rightarrow \color{blue}{c_{14}}$</p><p>All tiles from the $1$-st block will have colour $\color{red}{\textbf{1}}$, from the $2$-nd block will have colour $\color{blue}{\textbf{4}}$.</p><p>It is also possible to construct a path of length $9$ in this example, in which all tiles from the $1$-st block will have colour $\color{red}{\textbf{1}}$, from the $2$-nd block will have colour $\color{green}{\textbf{3}}$, and from the $3$-rd block will have colour $\color{blue}{\textbf{4}}$.</p></div><div class="input-specification"><p>The first line of input data contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le k \le n \le 2 \cdot 10^5$)—the number of tiles in the series and the length of the block.</p><p>The second line of each test case contains $n$ integers $c_1, c_2, c_3, \dots, c_n$ ($1 \le c_i \le n$) — the colours of the tiles.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output on a separate line: </p><ul> <li> <span class="tex-font-style-tt">YES</span> if you can get a path that satisfies these conditions; </li><li> <span class="tex-font-style-tt">NO</span> otherwise. </li></ul><p>You can output <span class="tex-font-style-tt">YES</span> and <span class="tex-font-style-tt">NO</span> in any case (for example, strings <span class="tex-font-style-tt">yEs</span>, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span> and <span class="tex-font-style-tt">YES</span> will be recognized as positive response).</p></div>

## Input

<p>The first line of input data contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le k \le n \le 2 \cdot 10^5$)—the number of tiles in the series and the length of the block.</p><p>The second line of each test case contains $n$ integers $c_1, c_2, c_3, \dots, c_n$ ($1 \le c_i \le n$) — the colours of the tiles.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output on a separate line: </p><ul> <li> <span class="tex-font-style-tt">YES</span> if you can get a path that satisfies these conditions; </li><li> <span class="tex-font-style-tt">NO</span> otherwise. </li></ul><p>You can output <span class="tex-font-style-tt">YES</span> and <span class="tex-font-style-tt">NO</span> in any case (for example, strings <span class="tex-font-style-tt">yEs</span>, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span> and <span class="tex-font-style-tt">YES</span> will be recognized as positive response).</p>





```input1|2,3,6,7,10,11,14,15,18,19
10
4 2
1 1 1 1
14 3
1 2 1 1 7 5 3 3 1 3 4 4 2 4
3 3
3 1 3
10 4
1 2 1 2 1 2 1 2 1 2
6 2
1 3 4 1 6 6
2 2
1 1
4 2
2 1 1 1
2 1
1 2
3 2
2 2 2
4 1
1 1 2 2
```




```output1
YES
YES
NO
NO
YES
YES
NO
YES
YES
YES
```



## Note

<p>In the first test case, you can jump from the first tile to the last tile;</p><p>The second test case is explained in the problem statement.</p>
