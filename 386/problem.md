## Description

<div><p>Dhruvil and amenotiomoi are sitting in different countries and chatting online. Initially, amenotiomoi has an empty board of size $n \times n$, and Dhruvil has a sequence of integers $1, 2, \ldots, n^2$, each number occurring exactly once. The numbers may be placed in the cells of the board, each cell is either empty or contains exactly one number.</p><p>The current state of the board is called <span class="tex-font-style-bf">good</span>, if there is a way of placing the remaining numbers in empty cells so that all numbers except $1$ have a neighbor with a smaller value. Two cells are neighbors if they share an edge.</p><p>The rows are numbered from $1$ to $n$ from top to bottom, the columns are numbered from $1$ to $n$ from left to right. The cell at the intersection of the $x$-th row and the $y$-th column is denoted as $(x, y)$.</p><p>To chat, amenotiomoi asks $q$ queries to Dhruvil. Each time he provides Dhruvil with an empty cell $(x, y)$. Dhruvil has to place one of the remaining numbers in this cell so that the board is still good. Among all ways to do this, he chooses the largest possible number he can place and sends this number to amenotiomoi as the answer to the query.</p><p>Since amenotiomoi knows the correct answer every time, he tells Dhruvil $(x \oplus k,y \oplus k)$ instead of $(x, y)$, where $k$ is the answer for the previous query. If amenotiomoi is sending the first query, he considers $k = 0$. Each time Dhruvil has to decode the query and send the answer to amenotiomoi. Here $\oplus$ denotes the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#XOR">bitwise XOR operation</a>.</p><p>Help Dhruvil reply to all amenotiomoi's queries.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $q$ ($1 \le n \le 10^3$, $1 \le q \le n^2$).</p><p>The $i$-th of the following $q$ lines contains two integers $x_i'$ and $y_i'$. The corresponding cell is $(x_i, y_i)$, where $x_i'=x_i \oplus k$ and $y_i' = y_i \oplus k$, where $k$ is the correct answer for the previous query. If $i = 1$, then $k = 0$ is used. It is guaranteed that $1 \le x_i, y_i \le n$ and that $(x_i, y_i)$ is an empty cell at the moment of $i$-th query.</p><p>It is guaranteed that the sum of $n^2$ over all test cases does not exceed $10^6$.</p></div><div class="output-specification"><p>For each test case, output one line, containing the answers to all queries, separated by spaces.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $q$ ($1 \le n \le 10^3$, $1 \le q \le n^2$).</p><p>The $i$-th of the following $q$ lines contains two integers $x_i'$ and $y_i'$. The corresponding cell is $(x_i, y_i)$, where $x_i'=x_i \oplus k$ and $y_i' = y_i \oplus k$, where $k$ is the correct answer for the previous query. If $i = 1$, then $k = 0$ is used. It is guaranteed that $1 \le x_i, y_i \le n$ and that $(x_i, y_i)$ is an empty cell at the moment of $i$-th query.</p><p>It is guaranteed that the sum of $n^2$ over all test cases does not exceed $10^6$.</p>

## Output

<p>For each test case, output one line, containing the answers to all queries, separated by spaces.</p>





```input1|2,3,4,5,6,17,18
3
2 4
1 1
6 6
3 0
1 2
3 9
2 1
8 11
4 4
4 4
2 0
4 4
11 10
1 3
3 2
1 1
1 1
```




```output1
4 2 3 1 
9 7 6 3 5 8 2 1 4 
1
```



## Note

<p>In the first test case, the first query is $(1, 1)$, Dhruvil puts $4$ in that cell.</p><p>The second query is $(6, 6)$, Dhruvil decode it as $(2, 2)$ using the previous answer ($2 \oplus 4 = 6$). If Dhruvil places $3$ to the cell $(2, 2)$, the board stops being good. So, Dhruvil places $2$ in this cell.</p><p>The third query is $(3, 0)$, Dhruvil decodes it as $(1, 2)$ using the previous answer ($1 \oplus 2 = 3$, $2 \oplus 2 = 0$). Dhruvil can place $3$ in this cell.</p><p>The fourth query is $(1, 2)$, Dhruvil decodes it as $(2, 1)$ using the previous answer ($2 \oplus 3 = 1$, $1 \oplus 3 = 2$). Now, only $1$ remains in the sequence, and after Dhruvil places $1$ in this cell, the board becomes full and remains good.</p><p>Here you can see the entire history of the board:</p><center> <img class="tex-graphics" src="file://PZ1oQ8HZ.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>In the second test case, the final state of the board is:</p><center> <table class="tex-tabular"><tbody><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$8$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$7$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$5$</td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$9$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$3$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$4$</td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$1$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$2$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$6$</td></tr></tbody></table> </center>
