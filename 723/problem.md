## Description

<div><p>Raj has a single physical network line that connects his office to the Internet. This line bandwidth is $b$ bytes per millisecond.</p><p>There are $n$ users who would like to use this network line to transmit some data. The $i$-th of them will use the line from millisecond $s_i$ to millisecond $f_i$ inclusive. His initial data rate will be set to $d_i$. That means he will use data rate equal to $d_i$ for millisecond $s_i$, and then it will change according to the procedure described below.</p><p>The flow control will happen as follows. Suppose there are $m$ users trying to transmit some data via the given network line during millisecond $x$. Denote as $t_i$ the data rate that the $i$-th of these $m$ users has at the beginning of this millisecond. All $t_i$ are non-negative integer values. </p><ol> <li> If $m = 0$, i.&nbsp;e. there are no users trying to transmit data during this millisecond, nothing happens. </li><li> If the sum of all $t_i$ is less than or equal to $b$, each active user successfully completes his transmission (the $i$-th active user transmits $t_i$ bytes). After that, the data rate of each active user grows by $1$, i.&nbsp;e. each $t_i$ is increased by $1$. </li><li> If the sum of all $t_i$ is greater than $b$, the congestion occurs and no data transmissions succeed this millisecond at all. If that happens, each $t_i$ decreases twice, i.&nbsp;e. each $t_i$ is replaced with $\lfloor \frac{t_i}{2} \rfloor$. </li></ol><p>Raj knows all the values $n$, $b$, $s_i$, $f_i$, and $d_i$, he wants to calculate the total number of bytes transmitted by all the users in the aggregate.</p></div><div class="input-specification"><p>The first line of the input contains two integers $n$ and $b$ ($1 \leq n \leq 2 \cdot 10^5$, $1 \leq b \leq 10^9$), the number of users who will use the line and the line bandwidth, respectively.</p><p>Each of the following $n$ lines contains three integers $s_i$, $f_i$ and $d_i$ ($1 \leq s_i \leq f_i \leq 10^9$, $1 \leq d_i \leq 10^9$), denoting that the $i$-th user will try to transmit data during each millisecond between $s_i$ and $f_i$ inclusive, and the initial data rate of the $i$-th user.</p></div><div class="output-specification"><p>Print one integer&nbsp;— the total number of bytes all users will successfully transmit.</p></div>

## Input

<p>The first line of the input contains two integers $n$ and $b$ ($1 \leq n \leq 2 \cdot 10^5$, $1 \leq b \leq 10^9$), the number of users who will use the line and the line bandwidth, respectively.</p><p>Each of the following $n$ lines contains three integers $s_i$, $f_i$ and $d_i$ ($1 \leq s_i \leq f_i \leq 10^9$, $1 \leq d_i \leq 10^9$), denoting that the $i$-th user will try to transmit data during each millisecond between $s_i$ and $f_i$ inclusive, and the initial data rate of the $i$-th user.</p>

## Output

<p>Print one integer&nbsp;— the total number of bytes all users will successfully transmit.</p>





```input1
1 3
1 5 2
```




```input2
1 10
7 11 1000
```




```input3
2 6
1 12 1
8 20 3
```




```input4
3 10
1 100 1
30 60 20
40 80 6
```




```output1
10
```




```output2
0
```




```output3
64
```




```output4
534
```



## Note

<p>Consider the first example.</p><ul> <li> Millisecond $1$: User $1$ transmits $2$ bytes. </li><li> Millisecond $2$: User $1$ transmits $3$ bytes. </li><li> Millisecond $3$: Congestion occurs, and no user transmits data. </li><li> Millisecond $4$: User $1$ transmits $2$ bytes. </li><li> Millisecond $5$: User $1$ transmits $3$ bytes. </li></ul><p>In the second example, at each millisecond from the $7$-th to the $11$-th inclusive, congestion occurs, and the only user decreases their rate twice. However, they don't decrease the speed enough before disconnecting.</p><p>Consider the third example.</p><ul> <li> Millisecond $1$: User $1$ transmits $1$ bytes. </li><li> Millisecond $2$: User $1$ transmits $2$ bytes. </li><li> Millisecond $3$: User $1$ transmits $3$ bytes. </li><li> Millisecond $4$: User $1$ transmits $4$ bytes. </li><li> Millisecond $5$: User $1$ transmits $5$ bytes. </li><li> Millisecond $6$: User $1$ transmits $6$ bytes. </li><li> Millisecond $7$: Congestion occurs, and no user transmits data. </li><li> Millisecond $8$: User $1$ transmits $3$ bytes. User $2$ transmits $3$ bytes. </li><li> Millisecond $9$: Congestion occurs, and no user transmits data. </li><li> Millisecond $10$: User $1$ transmits $2$ bytes. User $2$ transmits $2$ bytes. </li><li> Millisecond $11$: User $1$ transmits $3$ bytes. User $2$ transmits $3$ bytes. </li><li> Millisecond $12$: Congestion occurs, and no user transmits data. </li><li> Millisecond $13$: User $2$ transmits $2$ bytes. </li><li> Millisecond $14$: User $2$ transmits $3$ bytes. </li><li> Millisecond $15$: User $2$ transmits $4$ bytes. </li><li> Millisecond $16$: User $2$ transmits $5$ bytes. </li><li> Millisecond $17$: User $2$ transmits $6$ bytes. </li><li> Millisecond $18$: Congestion occurs, and no user transmits data. </li><li> Millisecond $19$: User $2$ transmits $3$ bytes. </li><li> Millisecond $20$: User $2$ transmits $4$ bytes. </li></ul>
