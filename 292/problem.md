## Description

<div><p>There are $n$ cards stacked in a deck. Initially, $a_{i}$ is written on the $i$-th card from the top. The value written on a card does not change.</p><p>You will play a game. Initially your score is $0$. In each turn, you can do <span class="tex-font-style-bf">one</span> of the following operations: </p><ul> <li> Choose an odd$^{\dagger}$ positive integer $i$, which is not greater than the number of cards left in the deck. Remove the $i$-th card from the top of the deck <span class="tex-font-style-bf">and add the number written on the card to your score</span>. The remaining cards will be reindexed starting from the top. </li><li> Choose an even$^{\ddagger}$ positive integer $i$, which is not greater than the number of cards left in the deck. Remove the $i$-th card from the top of the deck. The remaining cards will be reindexed starting from the top. </li><li> End the game. You can end the game whenever you want, you <span class="tex-font-style-bf">do not</span> have to remove all cards from the initial deck. </li></ul><p>What is the maximum score you can get when the game ends?</p><p>$^{\dagger}$ An integer $i$ is odd, if there exists an integer $k$ such that $i = 2k + 1$.</p><p>$^{\ddagger}$ An integer $i$ is even, if there exists an integer $k$ such that $i = 2k$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^{4}$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^{5}$).</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($-10^{9} \le a_i \le 10^{9}$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^{5}$.</p></div><div class="output-specification"><p>For each test case, print a single integer&nbsp;— the maximum score you can get when the game ends.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^{4}$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^{5}$).</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($-10^{9} \le a_i \le 10^{9}$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^{5}$.</p>

## Output

<p>For each test case, print a single integer&nbsp;— the maximum score you can get when the game ends.</p>





```input1|2,3,6,7
4
4
-4 1 -3 5
4
1 -2 3 -4
3
-1 3 -5
1
-1
```




```output1
5
4
2
0
```



## Note

<p>In the first test case, one can get the score of $5$ as follows: </p><ol> <li> In the first turn, choose $i=2$. Your score remains $0$ and the numbers written on the cards from the top will become $[-4, -3, 5]$. </li><li> In the second turn, choose $i=3$. Your score will become $5$ and the numbers written on the cards from the top will become $[-4, -3]$. </li><li> In the third turn, end the game with the score of $5$. </li></ol><p>In the second test case, one can get the score of $4$ as follows: </p><ol> <li> In the first turn, choose $i=3$. Your score will become $3$ and the numbers written on the cards from the top will become $[1, -2, -4]$. </li><li> In the second turn, choose $i=1$. Your score will become $4$ and the numbers written on the cards from the top will become $[-2, -4]$. </li><li> In the third turn, end the game with the score of $4$. </li></ol><p>In the third test case, one can get the score of $2$ as follows: </p><ol> <li> In the first turn, choose $i=1$. Your score will become $-1$ and the numbers written on the cards from the top will become $[3, -5]$. </li><li> In the second turn, choose $i=1$. Your score will become $2$ and the numbers written on the cards from the top will become $[-5]$. </li><li> In the third turn, end the game with the score of $2$. </li></ol>
