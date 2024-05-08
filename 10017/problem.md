## Description

<div><p>Turtle Alice is currently designing a fortune cookie box, and she would like to incorporate the theory of LuoShu into it.</p><p>The box can be seen as an $n \times m$ grid ($n, m \ge 5$), where the rows are numbered $1, 2, \dots, n$ and columns are numbered $1, 2, \dots, m$. Each cell can either be <span class="tex-font-style-bf">empty</span> or have a single fortune cookie of one of the following shapes: <span class="tex-font-style-bf">circle</span> or <span class="tex-font-style-bf">square</span>. The cell at the intersection of the $a$-th row and the $b$-th column is denoted as $(a, b)$.</p><p>Initially, the entire grid is empty. Then, Alice performs $q$ operations on the fortune cookie box. The $i$-th operation ($1 \le i \le q$) is as follows: specify a currently empty cell $(r_i,c_i)$ and a shape (circle or square), then put a fortune cookie of the specified shape on cell $(r_i,c_i)$. Note that after the $i$-th operation, the cell $(r_i,c_i)$ is no longer empty.</p><p>Before all operations <span class="tex-font-style-bf">and</span> after each of the $q$ operations, Alice wonders what the number of ways to place fortune cookies in <span class="tex-font-style-bf">all remaining empty cells</span> is, such that the following condition is satisfied:</p><p>No three consecutive cells (in horizontal, vertical, and both diagonal directions) contain cookies of the same shape. Formally:</p><ul> <li> There does not exist any $(i,j)$ satisfying $1 \le i \le n, 1 \le j \le m-2$, such that there are cookies of the same shape in cells $(i,j), (i,j+1), (i,j+2)$. </li><li> There does not exist any $(i,j)$ satisfying $1 \le i \le n-2, 1 \le j \le m$, such that there are cookies of the same shape in cells $(i,j), (i+1,j), (i+2,j)$. </li><li> There does not exist any $(i,j)$ satisfying $1 \le i \le n-2, 1 \le j \le m-2$, such that there are cookies of the same shape in cells $(i,j), (i+1,j+1), (i+2,j+2)$. </li><li> There does not exist any $(i,j)$ satisfying $1 \le i \le n-2, 1 \le j \le m-2$, such that there are cookies of the same shape in cells $(i,j+2), (i+1,j+1), (i+2,j)$. </li></ul><p>You should output all answers modulo $998\,244\,353$. Also note that it is possible that after some operations, the condition is already not satisfied with the already placed candies, in this case you should output $0$.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^3$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains three integers $n$, $m$, $q$ ($5 \le n, m \le 10^9, 0 \le q \le \min(n \times m, 10^5)$).</p><p>The $i$-th of the next $q$ lines contains two integers $r_i$, $c_i$ and a single string $\text{shape}_i$ ($1 \le r_i \le n, 1 \le c_i \le m$, $\text{shape}_i=$ <span class="tex-font-style-tt">"circle"</span> or <span class="tex-font-style-tt">"square"</span>), representing the operations. It is guaranteed that the cell on the $r_i$-th row and the $c_i$-th column is initially empty. That means, each $(r_i,c_i)$ will appear at most once in the updates.</p><p>The sum of $q$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output $q+1$ lines. The first line of each test case should contain the answer before any operations. The $i$-th line ($2 \le i \le q+1$) should contain the answer after the first $i-1$ operations. All answers should be taken modulo $998\,244\,353$.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^3$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains three integers $n$, $m$, $q$ ($5 \le n, m \le 10^9, 0 \le q \le \min(n \times m, 10^5)$).</p><p>The $i$-th of the next $q$ lines contains two integers $r_i$, $c_i$ and a single string $\text{shape}_i$ ($1 \le r_i \le n, 1 \le c_i \le m$, $\text{shape}_i=$ <span class="tex-font-style-tt">"circle"</span> or <span class="tex-font-style-tt">"square"</span>), representing the operations. It is guaranteed that the cell on the $r_i$-th row and the $c_i$-th column is initially empty. That means, each $(r_i,c_i)$ will appear at most once in the updates.</p><p>The sum of $q$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output $q+1$ lines. The first line of each test case should contain the answer before any operations. The $i$-th line ($2 \le i \le q+1$) should contain the answer after the first $i-1$ operations. All answers should be taken modulo $998\,244\,353$.</p>





```input1|2,3,4,5,6
2
6 7 4
3 3 circle
3 6 square
5 3 circle
5 4 square
5 5 3
1 1 circle
1 2 circle
1 3 circle
```




```output1
8
4
3
1
0
8
4
1
0
```



## Note

<p>In the second sample, after placing a circle-shaped fortune cookie to cells $(1,1)$, $(1,2)$ and $(1,3)$, the condition is already not satisfied. Therefore, you should output $0$.</p>
