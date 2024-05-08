## Description

<div><p>You've got a job in a game studio that developed an online shooter, and your first big task is to help to balance weapons. The game has $n$ weapons: the $i$-th gun has an integer fire rate $f_i$ and an integer damage per bullet $d_i$. The $i$-th gun's total firepower is equal to $p_i = f_i \cdot d_i$.</p><p>You have to modify the values $d_i$ of some guns in such a way that the new values $d_i$ will still be integers, and the firepower of all guns will become balanced. Given an integer $k$, the guns are said to be <span class="tex-font-style-it">balanced</span> if $\max\limits_{1 \le i \le n}{p_i} - \min\limits_{1 \le i \le n}{p_i} \le k$.</p><p>Since gamers that play your game don't like big changes, you need to change the values $d_i$ for the minimum possible number of guns. What is the minimum number of guns for which you have to change these values to make the guns balanced?</p><p>Note that the new values $d_i$ must be integers greater than $0$.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two integers $n$ and $k$ ($2 \le n \le 3000$; $0 \le k \le 1500$)&nbsp;— the number of guns to balance, and the maximum allowed gap between the most and the least powerful weapons.</p><p>The second line contains $n$ integers $f_1, f_2, \dots, f_n$ ($1 \le f_i \le 2000$), where $f_i$ is the fire rate of the $i$-th gun.</p><p>The third line contains $n$ integers $d_1, d_2, \dots, d_n$ ($1 \le d_i \le 10^9$), where $d_i$ is the damage per bullet of the $i$-th gun.</p><p>It's guaranteed that the sum of $n$ over all test cases doesn't exceed $3000$.</p></div><div class="output-specification"><p>For each test case, print the minimum number of guns which damage $d_i$ you have to change in order to make the guns balanced.</p><p>Note that the new values $d_i$ must be integers greater than $0$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two integers $n$ and $k$ ($2 \le n \le 3000$; $0 \le k \le 1500$)&nbsp;— the number of guns to balance, and the maximum allowed gap between the most and the least powerful weapons.</p><p>The second line contains $n$ integers $f_1, f_2, \dots, f_n$ ($1 \le f_i \le 2000$), where $f_i$ is the fire rate of the $i$-th gun.</p><p>The third line contains $n$ integers $d_1, d_2, \dots, d_n$ ($1 \le d_i \le 10^9$), where $d_i$ is the damage per bullet of the $i$-th gun.</p><p>It's guaranteed that the sum of $n$ over all test cases doesn't exceed $3000$.</p>

## Output

<p>For each test case, print the minimum number of guns which damage $d_i$ you have to change in order to make the guns balanced.</p><p>Note that the new values $d_i$ must be integers greater than $0$.</p>





```input1|2,3,4,8,9,10,14,15,16
5
4 2
6 3 13 7
1 2 1 2
3 2
100 101 102
100 99 98
5 0
1 12 4 4 3
12 1 3 3 4
2 50
1000 10
1000000000 1
3 5
1 19 11
49 4 72
```




```output1
2
3
0
1
2
```



## Note

<p>In the first test case, you can set $d_1 = 2$ and $d_2 = 4$. You'll get an array $d = [2, 4, 1, 2]$, and the values of firepower will be $p = [12, 12, 13, 14]$. The guns are balanced, since $14 - 12 \le 2$.</p><p>In the second test case, you have to change the value $d_i$ for all three guns. For example, you can set $d = [5151, 5100, 5050]$.</p><p>In the third test case, all guns are already balanced, so you don't have to change anything.</p>
