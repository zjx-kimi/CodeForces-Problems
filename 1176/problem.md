## Description

<div><p>One day, Vogons wanted to build a new hyperspace highway through a distant system with $n$ planets. The $i$-th planet is on the orbit $a_i$, there could be multiple planets on the same orbit. It's a pity that all the planets are on the way and need to be destructed.</p><p>Vogons have two machines to do that.</p><ul> <li> The first machine in one operation can destroy any planet at cost of $1$ Triganic Pu. </li><li> The second machine in one operation can destroy all planets on a single orbit in this system at the cost of $c$ Triganic Pus. </li></ul><p>Vogons can use each machine as many times as they want.</p><p>Vogons are very greedy, so they want to destroy all planets with minimum amount of money spent. Can you help them to know the minimum cost of this project?</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 100$) — the number of test cases. Then the test cases follow.</p><p>Each test case consists of two lines.</p><p>The first line contains two integers $n$ and $c$ ($1 \le n, c \le 100$) — the number of planets and the cost of the second machine usage.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 100$), where $a_i$ is the orbit of the $i$-th planet.</p></div><div class="output-specification"><p>For each test case print a single integer — the minimum cost of destroying all planets.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 100$) — the number of test cases. Then the test cases follow.</p><p>Each test case consists of two lines.</p><p>The first line contains two integers $n$ and $c$ ($1 \le n, c \le 100$) — the number of planets and the cost of the second machine usage.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 100$), where $a_i$ is the orbit of the $i$-th planet.</p>

## Output

<p>For each test case print a single integer — the minimum cost of destroying all planets.</p>





```input1|2,3,6,7
4
10 1
2 1 4 5 2 4 5 5 1 2
5 2
3 2 1 2 2
2 2
1 1
2 2
1 2
```




```input2|2,3
1
1 100
1
```




```output1
4
4
2
2
```




```output2
1
```



## Note

<p>In the first test case, the cost of using both machines is the same, so you can always use the second one and destroy all planets in orbit $1$, all planets in orbit $2$, all planets in orbit $4$, all planets in orbit $5$.</p><p>In the second test case, it is advantageous to use the second machine for $2$ Triganic Pus to destroy all the planets in orbit $2$, then destroy the remaining two planets using the first machine.</p><p>In the third test case, you can use the first machine twice or the second machine once.</p><p>In the fourth test case, it is advantageous to use the first machine twice.</p>
