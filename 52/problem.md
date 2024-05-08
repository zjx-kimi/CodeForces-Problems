## Description

<div><p><span class="tex-font-style-bf">This is the easy version of the problem. The only difference between the two versions is the constraint on $c_i$ and $z$. You can make hacks only if both versions of the problem are solved.</span></p><p>There are three arrays $a$, $b$ and $c$. $a$ and $b$ have length $n$ and $c$ has length $n-1$. Let $W(a,b,c)$ denote the liters of wine created from the following process.</p><p>Create $n$ water towers. The $i$-th water tower initially has $a_i$ liters of water and has a wizard with power $b_i$ in front of it. Furthermore, for each $1 \le i \le n - 1$, there is a valve connecting water tower $i$ to $i + 1$ with capacity $c_i$.</p><p>For each $i$ from $1$ to $n$ in this order, the following happens: </p><ol> <li> The wizard in front of water tower $i$ removes at most $b_i$ liters of water from the tower and turns the removed water into wine. </li><li> If $i \neq n$, at most $c_i$ liters of the remaining water left in water tower $i$ flows through the valve into water tower $i + 1$. </li></ol><p>There are $q$ updates. In each update, you will be given integers $p$, $x$, $y$ and $z$ and you will update $a_p := x$, $b_p := y$ and $c_p := z$. After each update, find the value of $W(a,b,c)$. Note that previous updates to arrays $a$, $b$ and $c$ persist throughout future updates.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $q$ ($2 \le n \le 5\cdot 10^5$, $1 \le q \le 5\cdot 10^5$)&nbsp;— the number of water towers and the number of updates.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i \le 10^9$)&nbsp;— the number of liters of water in water tower $i$.</p><p>The third line contains $n$ integers $b_1, b_2, \ldots, b_n$ ($0 \le b_i \le 10^9$)&nbsp;— the power of the wizard in front of water tower $i$.</p><p>The fourth line contains $n - 1$ integers $c_1, c_2, \ldots, c_{n - 1}$ ($c_i \color{red}{=} 10^{18}$)&nbsp;— the capacity of the pipe connecting water tower $i$ to $i + 1$.</p><p>Each of the next $q$ lines contains four integers $p$, $x$, $y$ and $z$ ($1 \le p \le n$, $0 \le x, y \le 10^9$, $z \color{red}{=} 10^{18}$)&nbsp;— the updates done to arrays $a$, $b$ and $c$.</p><p>Note that $c_n$ does not exist, so the value of $z$ does not matter when $p = n$.</p></div><div class="output-specification"><p>Print $q$ lines, each line containing a single integer representing $W(a, b, c)$ after each update.</p></div>

## Input

<p>The first line contains two integers $n$ and $q$ ($2 \le n \le 5\cdot 10^5$, $1 \le q \le 5\cdot 10^5$)&nbsp;— the number of water towers and the number of updates.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i \le 10^9$)&nbsp;— the number of liters of water in water tower $i$.</p><p>The third line contains $n$ integers $b_1, b_2, \ldots, b_n$ ($0 \le b_i \le 10^9$)&nbsp;— the power of the wizard in front of water tower $i$.</p><p>The fourth line contains $n - 1$ integers $c_1, c_2, \ldots, c_{n - 1}$ ($c_i \color{red}{=} 10^{18}$)&nbsp;— the capacity of the pipe connecting water tower $i$ to $i + 1$.</p><p>Each of the next $q$ lines contains four integers $p$, $x$, $y$ and $z$ ($1 \le p \le n$, $0 \le x, y \le 10^9$, $z \color{red}{=} 10^{18}$)&nbsp;— the updates done to arrays $a$, $b$ and $c$.</p><p>Note that $c_n$ does not exist, so the value of $z$ does not matter when $p = n$.</p>

## Output

<p>Print $q$ lines, each line containing a single integer representing $W(a, b, c)$ after each update.</p>





```input1|
4 3
3 3 3 3
1 4 2 8
1000000000000000000 1000000000000000000 1000000000000000000
4 3 8 1000000000000000000
2 5 1 1000000000000000000
3 0 0 1000000000000000000
```




```input2|
5 5
10 3 8 9 2
3 4 10 8 1
1000000000000000000 1000000000000000000 1000000000000000000 1000000000000000000
5 4 9 1000000000000000000
1 1 1 1000000000000000000
2 7 4 1000000000000000000
4 1 1 1000000000000000000
1 8 3 1000000000000000000
```




```output1
12
12
10
```




```output2
34
25
29
21
27
```



## Note

<p>The first update does not make any modifications to the arrays. </p><ul> <li> When $i = 1$, there are $3$ liters of water in tower 1 and $1$ liter of water is turned into wine. The remaining $2$ liters of water flow into tower 2. </li><li> When $i = 2$, there are $5$ liters of water in tower 2 and $4$ liters of water is turned into wine. The remaining $1$ liter of water flows into tower 3. </li><li> When $i = 3$, there are $4$ liters of water in tower 3 and $2$ liters of water is turned into wine. The remaining $2$ liters of water flows into tower 4. </li><li> When $i = 4$, there are $5$ liters of water in tower 4. All $5$ liters of water are turned into wine. </li></ul><p>Hence, $W(a,b,c)=1 + 4 + 2 + 5 = 12$ after the first update.</p><p>The second update modifies the arrays to $a = [3, 5, 3, 3]$, $b = [1, 1, 2, 8]$, and $c = [10^{18}, 10^{18}, 10^{18}]$.</p><ul> <li> When $i = 1$, there are $3$ liters of water in tower 1 and $1$ liter of water is turned into wine. The remaining $2$ liters of water flow into tower 2. </li><li> When $i = 2$, there are $7$ liters of water in tower 2 and $1$ liter of water is turned into wine. The remaining $6$ liters of water flow into tower 3. </li><li> When $i = 3$, there are $9$ liters of water in tower 3 and $2$ liters of water is turned into wine. The remaining $7$ liters of water flow into tower 4. </li><li> When $i = 4$, there are $10$ liters of water in tower 4. Only $8$ liters of water is turned into wine. </li></ul><p>Hence, $W(a,b,c)=1 + 1 + 2 + 8 = 12$ after the second update.</p><p>The third update modifies the arrays to $a = [3, 5, 0, 3]$, $b = [1, 1, 0, 8]$, and $c = [10^{18}, 10^{18}, 10^{18}]$.</p><ul> <li> When $i = 1$, there are $3$ liters of water in tower 1 and $1$ liter of water is turned into wine. The remaining $2$ liters of water flow into tower 2. </li><li> When $i = 2$, there are $7$ liters of water in tower 2 and $1$ liter of water is turned into wine. The remaining $6$ liters of water flow into tower 3. </li><li> When $i = 3$, there are $6$ liters of water in tower 3 and $0$ liters of water is turned into wine. The remaining $6$ liters of water flow into tower 4. </li><li> When $i = 4$, there are $9$ liters of water in tower 4. Only $8$ liters of water is turned into wine. </li></ul><p>Hence, $W(a,b,c)=1 + 1 + 0 + 8 = 10$ after the third update.</p>
