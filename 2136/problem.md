## Description

<div><p>Consider a sequence of integers $a_1, a_2, \ldots, a_n$. In one move, you can select any element of the sequence and delete it. After an element is deleted, all elements to the right are shifted to the left by $1$ position, so there are no empty spaces in the sequence. So after you make a move, the sequence's length decreases by $1$. The indices of the elements after the move are recalculated.</p><p>E. g. let the sequence be $a=[3, 2, 2, 1, 5]$. Let's select the element $a_3=2$ in a move. Then after the move the sequence will be equal to $a=[3, 2, 1, 5]$, so the $3$-rd element of the new sequence will be $a_3=1$ and the $4$-th element will be $a_4=5$.</p><p>You are given a sequence $a_1, a_2, \ldots, a_n$ and a number $k$. You need to find the minimum number of moves you have to make so that in the resulting sequence there will be <span class="tex-font-style-bf">at least</span> $k$ elements that are equal to their indices, i. e. the resulting sequence $b_1, b_2, \ldots, b_m$ will contain at least $k$ indices $i$ such that $b_i = i$.</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 100$) — the number of test cases. Then $t$ test cases follow.</p><p>Each test case consists of two consecutive lines. The first line contains two integers $n$ and $k$ ($1 \le k \le n \le 2000$). The second line contains a sequence of integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le n$). The numbers in the sequence are not necessarily different.</p><p>It is guaranteed that the sum of $n$ over all test cases doesn't exceed $2000$.</p></div><div class="output-specification"><p>For each test case output in a single line:</p><ul> <li> $-1$ if there's no desired move sequence; </li><li> otherwise, the integer $x$ ($0 \le x \le n$) — the minimum number of the moves to be made so that the resulting sequence will contain at least $k$ elements that are equal to their indices. </li></ul></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 100$) — the number of test cases. Then $t$ test cases follow.</p><p>Each test case consists of two consecutive lines. The first line contains two integers $n$ and $k$ ($1 \le k \le n \le 2000$). The second line contains a sequence of integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le n$). The numbers in the sequence are not necessarily different.</p><p>It is guaranteed that the sum of $n$ over all test cases doesn't exceed $2000$.</p>

## Output

<p>For each test case output in a single line:</p><ul> <li> $-1$ if there's no desired move sequence; </li><li> otherwise, the integer $x$ ($0 \le x \le n$) — the minimum number of the moves to be made so that the resulting sequence will contain at least $k$ elements that are equal to their indices. </li></ul>





```input1
4
7 6
1 1 2 3 4 5 6
5 2
5 1 3 2 3
5 2
5 5 5 5 4
8 4
1 2 3 3 2 2 5 5
```




```output1
1
2
-1
2
```



## Note

<p>In the first test case the sequence doesn't satisfy the desired condition, but it can be provided by deleting the first element, hence the sequence will be $[1, 2, 3, 4, 5, 6]$ and $6$ elements will be equal to their indices.</p><p>In the second test case there are two ways to get the desired result in $2$ moves: the first one is to delete the $1$-st and the $3$-rd elements so that the sequence will be $[1, 2, 3]$ and have $3$ elements equal to their indices; the second way is to delete the $2$-nd and the $3$-rd elements to get the sequence $[5, 2, 3]$ with $2$ desired elements.</p>
