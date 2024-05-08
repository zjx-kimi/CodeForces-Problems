## Description

<div><p>Masha and Olya have an important team olympiad coming up soon. In honor of this, Masha, for warm-up, suggested playing a game with Olya:</p><p>There is an array $a$ of size $n$. Masha goes first, and the players take turns. Each move is described by the following sequence of actions:</p><p>$\bullet$ If the size of the array is $1$, the game ends.</p><p>$\bullet$ The player who is currently playing chooses two <span class="tex-font-style-bf">different</span> indices $i$, $j$ ($1 \le i, j \le |a|$), and performs the following operation&nbsp;— removes $a_i$ and $a_j$ from the array and adds to the array a number equal to $\lfloor \frac{a_i + a_j}{2} \rfloor \cdot 2$. In other words, first divides the sum of the numbers $a_i$, $a_j$ by $2$ rounding down, and then multiplies the result by $2$.</p><p>Masha aims to maximize the final number, while Olya aims to minimize it.</p><p>Masha and Olya decided to play on each non-empty prefix of the initial array $a$, and asked for your help.</p><p>For each $k = 1, 2, \ldots, n$, answer the following question. Let only the first $k$ elements of the array $a$ be present in the game, with indices $1, 2, \ldots, k$ respectively. What number will remain at the end with optimal play by both players?</p></div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$)&nbsp;— the size of the array.</p><p>The second line contains $n$ integers $a_1,a_2, \ldots,a_n$ ($1 \leq a_i \leq 10^9$)&nbsp;— the array on which Masha and Olya play.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output $n$ integers. The $k$-th of these numbers should be equal to the number that will remain at the end with optimal play by both players, on the array consisting of the first $k$ elements of the array $a$.</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$)&nbsp;— the size of the array.</p><p>The second line contains $n$ integers $a_1,a_2, \ldots,a_n$ ($1 \leq a_i \leq 10^9$)&nbsp;— the array on which Masha and Olya play.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output $n$ integers. The $k$-th of these numbers should be equal to the number that will remain at the end with optimal play by both players, on the array consisting of the first $k$ elements of the array $a$.</p>





```input1|2,3,6,7
4
1
31
6
6 3 7 2 5 4
3
3 10 11
5
7 13 11 19 1
```




```output1
31 
6 8 16 18 22 26 
3 12 24 
7 20 30 48 50
```



## Note

<p>In the third test case, for a prefix of length $1$, the answer is $3$. For a prefix of length $2$, Masha has only one move, so the answer is $12$. For a prefix of length $3$, Masha has three possible moves: she chooses $3$ and $10$, then the final number is $22$, $3$ and $11$, then the final number is $24$, $10$ and $11$, then the final number is $22$, so Masha will choose $3$ and $11$ and get $24$.</p>
