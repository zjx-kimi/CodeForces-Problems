## Description

<div><p>After working at a factory (Lihmuf Sorting), Lihmuf wants to play a game with his good friend, Pak Chanek. There are $N$ boxes numbered from $1$ to $N$. The $i$-th box contains $i$ balls. Pak Chanek and Lihmuf will play a game using those boxes.</p><p>There will be $N$ turns numbered from $1$ to $N$. On each turn, Pak Chanek chooses one box and takes all balls from that box, then Lihmuf does the same thing for one box he chooses (it is possible that the two chosen boxes are the same).</p><p>Given an integer $M$. Before the game begins, Lihmuf must choose an integer $K$ satisfying $1 \leq K \leq M$. It is known that on the $j$-th turn, Pak Chanek will choose the $j$-th box, while Lihmuf will choose the $y$-th box, with $y=((j \times K - 1) \bmod N) + 1$. Help Lihmuf choose the correct value of $K$ so that he will get as many balls as possible! If there are more than one possible values of $K$ that result in the maximum total balls, find the minimum such value of $K$.</p><p>Keep in mind that each box can be chosen more than once, but after a box is chosen for the first time, the box becomes empty.</p></div><div class="input-specification"><p>The only line contains two integers $N$ and $M$ ($1 \leq N \leq 10^9$; $1 \leq M \leq 2000$) — the number of boxes and the maximum limit for the value of $K$.</p></div><div class="output-specification"><p>An integer representing the value of $K$ that will make Lihmuf get as many balls as possible. If there are more than one possible value of $K$ that result in the maximum total balls, find the minimum such value of $K$.</p></div>

## Input

<p>The only line contains two integers $N$ and $M$ ($1 \leq N \leq 10^9$; $1 \leq M \leq 2000$) — the number of boxes and the maximum limit for the value of $K$.</p>

## Output

<p>An integer representing the value of $K$ that will make Lihmuf get as many balls as possible. If there are more than one possible value of $K$ that result in the maximum total balls, find the minimum such value of $K$.</p>





```input1
3 1
```




```input2
5 4
```




```output1
1
```




```output2
3
```



## Note

<p>In the first example, if Lihmuf chooses $K=1$, the game will go as follows: </p><ol> <li> Pak Chanek chooses the $1$-st box and gets $1$ ball, then Lihmuf chooses the $1$-st box and gets $0$ balls. </li><li> Pak Chanek chooses the $2$-nd box and gets $2$ balls, then Lihmuf chooses the $2$-nd box and gets $0$ balls. </li><li> Pak Chanek chooses the $3$-rd box and gets $3$ balls, then Lihmuf chooses the $3$-rd box and gets $0$ balls. </li></ol><p>In total, Lihmuf gets $0+0+0=0$ balls.</p><p>The maximum total balls that can be earned by Lihmuf is $0$ because he can only choose $K=1$. Therefore, $K=1$ is the minimum possible value of $K$ that results in the maximum total balls.</p><p>In the second example, if Lihmuf chooses $K=3$, the game will go as follows: </p><ol> <li> Pak Chanek chooses the $1$-st box and gets $1$ ball, then Lihmuf chooses the $3$-rd box and gets $3$ balls. </li><li> Pak Chanek chooses the $2$-nd box and gets $2$ balls, then Lihmuf chooses the $1$-st box and gets $0$ balls. </li><li> Pak Chanek chooses the $3$-rd box and gets $0$ balls, then Lihmuf chooses the $4$-th box and gets $4$ balls. </li><li> Pak Chanek chooses the $4$-th box and gets $0$ balls, then Lihmuf chooses the $2$-nd box and gets $0$ balls. </li><li> Pak Chanek chooses the $5$-th box and gets $5$ balls, then Lihmuf chooses the $5$-th box and gets $0$ balls. </li></ol><p>In total, Lihmuf gets $3+0+4+0+0=7$ balls.</p><p>It can be obtained that $7$ is the maximum total balls that can be earned by Lihmuf. The possible values of $K$ that result in $7$ total balls are $3$ and $4$. Therefore, $K=3$ is the minimum possible value of $K$ that results in the maximum total balls.</p>
