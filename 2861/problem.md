## Description

<div><p>All techniques in the ninja world consist of hand seals. At the moment Naruto is learning a new technique, which consists of $n\cdot m$ different seals, denoted by distinct numbers. All of them were written in an $n\times m$ table.</p><p>The table is lost now. Naruto managed to remember elements of each row from left to right, and elements of each column from top to bottom, but he doesn't remember the order of rows and columns. Please restore the table consistent with this data so that Naruto will be able to learn the new technique.</p></div><div class="input-specification"><p>The first line of the input contains the only integer $t$ ($1\leq t\leq 100\,000$) denoting the number of test cases. Their descriptions follow.</p><p>The first line of each test case description consists of two space-separated integers $n$ and $m$ ($1 \leq n, m \leq 500$) standing for the number of rows and columns in the table, respectively. All hand seals are encoded by the positive integers from $1$ to $n\cdot m$.</p><p>The following $n$ lines contain $m$ space separated integers each, denoting elements of an arbitrary row in the table left to right.</p><p>The following $m$ lines contain $n$ space separated integers each, denoting elements of an arbitrary column in the table top to bottom.</p><p>Sum of $nm$ over all test cases does not exceed $250\,000$. It is guaranteed that each row occurs in the input exactly once, as well as each column. It is also guaranteed that each number from $1$ to $nm$ occurs exactly once in all rows, as well as in all columns. Finally, it is guaranteed that a table consistent with the input exists.</p></div><div class="output-specification"><p>For each test case, output $n$ lines with $m$ space-separated integers each, denoting the restored table. One can show that the answer is always unique.</p></div>

## Input

<p>The first line of the input contains the only integer $t$ ($1\leq t\leq 100\,000$) denoting the number of test cases. Their descriptions follow.</p><p>The first line of each test case description consists of two space-separated integers $n$ and $m$ ($1 \leq n, m \leq 500$) standing for the number of rows and columns in the table, respectively. All hand seals are encoded by the positive integers from $1$ to $n\cdot m$.</p><p>The following $n$ lines contain $m$ space separated integers each, denoting elements of an arbitrary row in the table left to right.</p><p>The following $m$ lines contain $n$ space separated integers each, denoting elements of an arbitrary column in the table top to bottom.</p><p>Sum of $nm$ over all test cases does not exceed $250\,000$. It is guaranteed that each row occurs in the input exactly once, as well as each column. It is also guaranteed that each number from $1$ to $nm$ occurs exactly once in all rows, as well as in all columns. Finally, it is guaranteed that a table consistent with the input exists.</p>

## Output

<p>For each test case, output $n$ lines with $m$ space-separated integers each, denoting the restored table. One can show that the answer is always unique.</p>





```input1
2
2 3
6 5 4
1 2 3
1 6
2 5
3 4
3 1
2
3
1
3 1 2
```




```output1
1 2 3 
6 5 4 
3 
1 
2
```



## Note

<p>Consider the first test case. The matrix is $2 \times 3$. You are given the rows and columns in arbitrary order.</p><p>One of the rows is $[6, 5, 4]$. One of the rows is $[1, 2, 3]$.</p><p>One of the columns is $[1, 6]$. One of the columns is $[2, 5]$. One of the columns is $[3, 4]$.</p><p>You are to reconstruct the matrix. The answer is given in the output.</p>