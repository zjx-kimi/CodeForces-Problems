## Description

<div><p>To celebrate your birthday you have prepared a festive table! Now you want to seat as many guests as possible.</p><p>The table can be represented as a rectangle with height $h$ and width $w$, divided into $h \times w$ cells. Let $(i, j)$ denote the cell in the $i$-th row and the $j$-th column of the rectangle ($1 \le i \le h$; $1 \le j \le w$).</p><p>Into each cell of the table you can either put a plate or keep it empty.</p><p>As each guest has to be seated next to their plate, you can only put plates on the edge of the table&nbsp;— into the first or the last row of the rectangle, or into the first or the last column. Formally, for each cell $(i, j)$ you put a plate into, at least one of the following conditions must be satisfied: $i = 1$, $i = h$, $j = 1$, $j = w$.</p><p>To make the guests comfortable, no two plates must be put into cells that have a common side or corner. In other words, if cell $(i, j)$ contains a plate, you can't put plates into cells $(i - 1, j)$, $(i, j - 1)$, $(i + 1, j)$, $(i, j + 1)$, $(i - 1, j - 1)$, $(i - 1, j + 1)$, $(i + 1, j - 1)$, $(i + 1, j + 1)$.</p><p>Put as many plates on the table as possible without violating the rules above.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 100$)&nbsp;— the number of test cases.</p><p>Each of the following $t$ lines describes one test case and contains two integers $h$ and $w$ ($3 \le h, w \le 20$)&nbsp;— the height and the width of the table.</p></div><div class="output-specification"><p>For each test case, print $h$ lines containing $w$ characters each. Character $j$ in line $i$ must be equal to $1$ if you are putting a plate into cell $(i, j)$, and $0$ otherwise. If there are multiple answers, print any.</p><p>All plates must be put on the edge of the table. No two plates can be put into cells that have a common side or corner. The number of plates put on the table under these conditions must be as large as possible.</p><p>You are allowed to print additional empty lines.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 100$)&nbsp;— the number of test cases.</p><p>Each of the following $t$ lines describes one test case and contains two integers $h$ and $w$ ($3 \le h, w \le 20$)&nbsp;— the height and the width of the table.</p>

## Output

<p>For each test case, print $h$ lines containing $w$ characters each. Character $j$ in line $i$ must be equal to $1$ if you are putting a plate into cell $(i, j)$, and $0$ otherwise. If there are multiple answers, print any.</p><p>All plates must be put on the edge of the table. No two plates can be put into cells that have a common side or corner. The number of plates put on the table under these conditions must be as large as possible.</p><p>You are allowed to print additional empty lines.</p>





```input1
3
3 5
4 4
5 6
```




```output1
10101
00000
10101

0100
0001
1000
0010

010101
000000
100001
000000
101010
```



## Note

<p>For the first test case, example output contains the only way to put $6$ plates on the table.</p><p>For the second test case, there are many ways to put $4$ plates on the table, example output contains one of them.</p><p>Putting more than $6$ plates in the first test case or more than $4$ plates in the second test case is impossible.</p>
