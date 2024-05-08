## Description

<div><p>After watching a certain anime before going to sleep, Mark dreams of standing in an old classroom with a blackboard that has a sequence of $n$ positive integers $a_1, a_2,\dots,a_n$ on it.</p><p>Then, professor Koro comes in. He can perform the following operation:</p><ul> <li> select an integer $x$ that appears at least $2$ times on the board, </li><li> erase those $2$ appearances, and </li><li> write $x+1$ on the board. </li></ul><p>Professor Koro then asks Mark the question, "what is the maximum possible number that could appear on the board after some operations?"</p><p>Mark quickly solves this question, but he is still slower than professor Koro. Thus, professor Koro decides to give Mark additional challenges. He will update the initial sequence of integers $q$ times. Each time, he will choose positive integers $k$ and $l$, then change $a_k$ to $l$. After each update, he will ask Mark the same question again.</p><p>Help Mark answer these questions faster than Professor Koro!</p><p>Note that the updates are persistent. Changes made to the sequence $a$ will apply when processing future updates.</p></div><div class="input-specification"><p>The first line of the input contains two integers $n$ and $q$ ($2\leq n\leq 2\cdot 10^5$, $1\leq q\leq 2\cdot 10^5$) — the length of the sequence $a$ and the number of updates, respectively.</p><p>The second line contains $n$ integers $a_1,a_2,\dots,a_n$ ($1\leq a_i\leq 2\cdot 10^5$)</p><p>Then, $q$ lines follow, each consisting of two integers $k$ and $l$ ($1\leq k\leq n$, $1\leq l\leq 2\cdot 10^5$), telling to update $a_k$ to $l$.</p></div><div class="output-specification"><p>Print $q$ lines. The $i$-th line should consist of a single integer — the answer after the $i$-th update.</p></div>

## Input

<p>The first line of the input contains two integers $n$ and $q$ ($2\leq n\leq 2\cdot 10^5$, $1\leq q\leq 2\cdot 10^5$) — the length of the sequence $a$ and the number of updates, respectively.</p><p>The second line contains $n$ integers $a_1,a_2,\dots,a_n$ ($1\leq a_i\leq 2\cdot 10^5$)</p><p>Then, $q$ lines follow, each consisting of two integers $k$ and $l$ ($1\leq k\leq n$, $1\leq l\leq 2\cdot 10^5$), telling to update $a_k$ to $l$.</p>

## Output

<p>Print $q$ lines. The $i$-th line should consist of a single integer — the answer after the $i$-th update.</p>





```input1
5 4
2 2 2 4 5
2 3
5 3
4 1
1 4
```




```input2
2 1
200000 1
2 200000
```




```output1
6
5
4
5
```




```output2
200001
```



## Note

<p>In the first example test, the program must proceed through $4$ updates.</p><p>The sequence after the first update is $[2,3,2,4,5]$. One sequence of operations that achieves the number $6$ the following. </p><ul> <li> Initially, the blackboard has numbers $[2,3,2,4,5]$. </li><li> Erase two copies of $2$ and write $3$, yielding $[3,4,5,\color{red}{3}]$. </li><li> Erase two copies of $3$ and write $4$, yielding $[4,5,\color{red}{4}]$. </li><li> Erase two copies of $4$ and write $5$, yielding $[5,\color{red}{5}]$. </li><li> Erase two copies of $5$ and write $6$, yielding $[\color{red}{6}]$. </li></ul><p>Then, in the second update, the array is changed to $[2,3,2,4,3]$. This time, Mark cannot achieve $6$. However, one sequence that Mark can use to achieve $5$ is shown below. </p><ul> <li> Initially, the blackboard has $[2,3,2,4,3]$. </li><li> Erase two copies of $2$ and write $3$, yielding $[3,4,3,\color{red}{3}]$. </li><li> Erase two copies of $3$ and write $4$, yielding $[3,4,\color{red}{4}]$. </li><li> Erase two copies of $4$ and write $5$, yielding $[3,\color{red}{5}]$. </li></ul><p>In the third update, the array is changed to $[2,3,2,1,3]$. One way to achieve $4$ is shown below. </p><ul> <li> Initially, the blackboard has $[2,3,2,1,3]$. </li><li> Erase two copies of $3$ and write $4$, yielding $[2,2,1,\color{red}{4}]$. </li></ul>
