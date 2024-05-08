## Description

<div><p>You are given integers $n$ and $m$. Fill an $n$ by $m$ grid with the integers $1$ through $n\cdot m$, in such a way that for any two adjacent cells in the grid, the absolute difference of the values in those cells is not a prime number. Two cells in the grid are considered adjacent if they share a side.</p><center> <img class="tex-graphics" src="file://80KXKETC.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>It can be shown that under the given constraints, there is always a solution.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first and only line of each test case contains two integers $n$ and $m$ ($4 \le n, m \le 1000$)&nbsp;— the dimensions of the grid.</p><p>It is guaranteed that the sum of $n\cdot m$ over all test cases does not exceed $10^6$.</p></div><div class="output-specification"><p>For each test case, output $n$ lines of $m$ integers each, representing the final grid. Every number from $1$ to $n\cdot m$ should appear exactly once in the grid.</p><p>The extra spaces and blank lines in the sample output below are only present to make the output easier to read, and are <span class="tex-font-style-bf">not</span> required.</p><p>If there are multiple solutions, print any of them.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first and only line of each test case contains two integers $n$ and $m$ ($4 \le n, m \le 1000$)&nbsp;— the dimensions of the grid.</p><p>It is guaranteed that the sum of $n\cdot m$ over all test cases does not exceed $10^6$.</p>

## Output

<p>For each test case, output $n$ lines of $m$ integers each, representing the final grid. Every number from $1$ to $n\cdot m$ should appear exactly once in the grid.</p><p>The extra spaces and blank lines in the sample output below are only present to make the output easier to read, and are <span class="tex-font-style-bf">not</span> required.</p><p>If there are multiple solutions, print any of them.</p>





```input1|2,4
3
4 4
5 7
6 4
```




```output1
16  7  1  9
12  8  2  3
13  4 10 11
14  5  6 15

29 23 17  9  5  6  2
33 27 21 15 11  7  1
32 31 25 19 20 16 10
26 30 24 18 14  8  4
35 34 28 22 13 12  3

 2  3  7 11
 8  9  1 10
17 13  5  4
18 14  6 12
19 23 15 21
20 24 16 22
```



## Note

<p>The first sample case corresponds to the picture above. The only absolute differences between adjacent elements in this grid are $1$, $4$, $6$, $8$, and $9$, none of which are prime. </p>
