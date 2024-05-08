## Description

<div><p>There are $n$ boxes placed in a line. The boxes are numbered from $1$ to $n$. Some boxes contain one ball inside of them, the rest are empty. At least one box contains a ball and at least one box is empty.</p><p>In one move, you <span class="tex-font-style-bf">have to</span> choose a box with a ball inside and an adjacent empty box and move the ball from one box into another. Boxes $i$ and $i+1$ for all $i$ from $1$ to $n-1$ are considered adjacent to each other. Boxes $1$ and $n$ are <span class="tex-font-style-bf">not adjacent</span>.</p><p>How many different arrangements of balls exist after <span class="tex-font-style-bf">exactly</span> $k$ moves are performed? Two arrangements are considered different if there is at least one such box that it contains a ball in one of them and doesn't contain a ball in the other one.</p><p>Since the answer might be pretty large, print its remainder modulo $10^9+7$.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $k$ ($2 \le n \le 1500$; $1 \le k \le 1500$)&nbsp;— the number of boxes and the number of moves.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($a_i \in \{0, 1\}$)&nbsp;— $0$ denotes an empty box and $1$ denotes a box with a ball inside. There is at least one $0$ and at least one $1$.</p></div><div class="output-specification"><p>Print a single integer&nbsp;— the number of different arrangements of balls that can exist after <span class="tex-font-style-bf">exactly</span> $k$ moves are performed, modulo $10^9+7$.</p></div>

## Input

<p>The first line contains two integers $n$ and $k$ ($2 \le n \le 1500$; $1 \le k \le 1500$)&nbsp;— the number of boxes and the number of moves.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($a_i \in \{0, 1\}$)&nbsp;— $0$ denotes an empty box and $1$ denotes a box with a ball inside. There is at least one $0$ and at least one $1$.</p>

## Output

<p>Print a single integer&nbsp;— the number of different arrangements of balls that can exist after <span class="tex-font-style-bf">exactly</span> $k$ moves are performed, modulo $10^9+7$.</p>





```input1
4 1
1 0 1 0
```




```input2
4 2
1 0 1 0
```




```input3
10 6
1 0 0 1 0 0 0 1 1 1
```




```output1
3
```




```output2
2
```




```output3
69
```



## Note

<p>In the first example, there are the following possible arrangements: </p><ul> <li> <span class="tex-font-style-tt">0 1 1 0</span>&nbsp;— obtained after moving the ball from box $1$ to box $2$; </li><li> <span class="tex-font-style-tt">1 0 0 1</span>&nbsp;— obtained after moving the ball from box $3$ to box $4$; </li><li> <span class="tex-font-style-tt">1 1 0 0</span>&nbsp;— obtained after moving the ball from box $3$ to box $2$. </li></ul><p>In the second example, there are the following possible arrangements: </p><ul> <li> <span class="tex-font-style-tt">1 0 1 0</span>&nbsp;— three ways to obtain that: just reverse the operation performed during the first move; </li><li> <span class="tex-font-style-tt">0 1 0 1</span>&nbsp;— obtained from either of the first two arrangements after the first move. </li></ul>
