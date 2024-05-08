## Description

<div><p>The Berland Army is preparing for a large military parade. It is already decided that the soldiers participating in it will be divided into $k$ rows, and all rows will contain <span class="tex-font-style-it">the same</span> number of soldiers.</p><p>Of course, not every arrangement of soldiers into $k$ rows is suitable. Heights of all soldiers in the same row should not differ by more than $1$. The height of each soldier is an integer between $1$ and $n$.</p><p>For each possible height, you know the number of soldiers having this height. To conduct a parade, you have to choose the soldiers participating in it, and then arrange <span class="tex-font-style-it">all of the chosen soldiers</span> into $k$ rows so that both of the following conditions are met:</p><ul> <li> each row has the same number of soldiers, </li><li> no row contains a pair of soldiers such that their heights differ by $2$ or more. </li></ul><p>Calculate the maximum number of soldiers who can participate in the parade.</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 10000$) — the number of test cases. Then the test cases follow. </p><p>Each test case begins with a line containing two integers $n$ and $k$ ($1 \le n \le 30000$, $1 \le k \le 10^{12}$) — the number of different heights of soldiers and the number of rows of soldiers in the parade, respectively.</p><p>The second (and final) line of each test case contains $n$ integers $c_1$, $c_2$, ..., $c_n$ ($0 \le c_i \le 10^{12}$), where $c_i$ is the number of soldiers having height $i$ in the Berland Army.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $30000$.</p></div><div class="output-specification"><p>For each test case, print one integer — the maximum number of soldiers that can participate in the parade.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 10000$) — the number of test cases. Then the test cases follow. </p><p>Each test case begins with a line containing two integers $n$ and $k$ ($1 \le n \le 30000$, $1 \le k \le 10^{12}$) — the number of different heights of soldiers and the number of rows of soldiers in the parade, respectively.</p><p>The second (and final) line of each test case contains $n$ integers $c_1$, $c_2$, ..., $c_n$ ($0 \le c_i \le 10^{12}$), where $c_i$ is the number of soldiers having height $i$ in the Berland Army.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $30000$.</p>

## Output

<p>For each test case, print one integer — the maximum number of soldiers that can participate in the parade.</p>





```input1
5
3 4
7 1 13
1 1
100
1 3
100
2 1
1000000000000 1000000000000
4 1
10 2 11 1
```




```output1
16
100
99
2000000000000
13
```



## Note

<p>Explanations for the example test cases:</p><ol> <li> the heights of soldiers in the rows can be: $[3, 3, 3, 3]$, $[1, 2, 1, 1]$, $[1, 1, 1, 1]$, $[3, 3, 3, 3]$ (each list represents a row); </li><li> all soldiers can march in the same row; </li><li> $33$ soldiers with height $1$ in each of $3$ rows; </li><li> all soldiers can march in the same row; </li><li> all soldiers with height $2$ and $3$ can march in the same row. </li></ol>
