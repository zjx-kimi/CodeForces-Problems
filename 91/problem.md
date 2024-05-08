## Description

<div><p><span class="tex-font-style-bf">The easy and hard versions of this problem differ only in the constraints on the number of test cases and $n$. In the hard version, the number of test cases does not exceed $10^4$, and the sum of values of $n$ over all test cases does not exceed $2 \cdot 10^5$. Furthermore, there are no additional constraints on $n$ in a single test case.</span></p><p>Recently, Alice and Bob were given marbles of $n$ different colors by their parents. Alice has received $a_1$ marbles of color $1$, $a_2$ marbles of color $2$,..., $a_n$ marbles of color $n$. Bob has received $b_1$ marbles of color $1$, $b_2$ marbles of color $2$, ..., $b_n$ marbles of color $n$. All $a_i$ and $b_i$ are between $1$ and $10^9$.</p><p>After some discussion, Alice and Bob came up with the following game: players take turns, starting with Alice. On their turn, a player chooses a color $i$ such that <span class="tex-font-style-bf">both</span> players have at least one marble of that color. The player then discards <span class="tex-font-style-it">one marble</span> of color $i$, and their opponent discards <span class="tex-font-style-it">all marbles</span> of color $i$. The game ends when there is no color $i$ such that both players have at least one marble of that color.</p><p>The score in the game is the difference between the number of remaining marbles that Alice has and the number of remaining marbles that Bob has at the end of the game. In other words, the score in the game is equal to $(A-B)$, where $A$ is the number of marbles Alice has and $B$ is the number of marbles Bob has at the end of the game. Alice wants to maximize the score, while Bob wants to minimize it.</p><p>Calculate the score at the end of the game if both players play optimally.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of three lines:</p><ul> <li> the first line contains a single integer $n$ ($2 \le n \le 2 \cdot 10^5$) — the number of colors; </li><li> the second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$), where $a_i$ is the number of marbles of the $i$-th color that Alice has; </li><li> the third line contains $n$ integers $b_1, b_2, \dots, b_n$ ($1 \le b_i \le 10^9$), where $b_i$ is the number of marbles of the $i$-th color that Bob has. </li></ul><p>Additional constraint on the input: the sum of $n$ for all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer — the score at the end of the game if both Alice and Bob act optimally.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of three lines:</p><ul> <li> the first line contains a single integer $n$ ($2 \le n \le 2 \cdot 10^5$) — the number of colors; </li><li> the second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$), where $a_i$ is the number of marbles of the $i$-th color that Alice has; </li><li> the third line contains $n$ integers $b_1, b_2, \dots, b_n$ ($1 \le b_i \le 10^9$), where $b_i$ is the number of marbles of the $i$-th color that Bob has. </li></ul><p>Additional constraint on the input: the sum of $n$ for all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output a single integer — the score at the end of the game if both Alice and Bob act optimally.</p>





```input1|2,3,4,8,9,10,14,15,16
5
3
4 2 1
1 2 4
4
1 20 1 20
100 15 10 20
5
1000000000 1000000000 1000000000 1000000000 1000000000
1 1 1 1 1
3
5 6 5
2 1 7
6
3 2 4 2 5 5
9 4 7 9 2 5
```




```output1
1
-9
2999999997
8
-6
```



## Note

<p>In the first example, one way to achieve a score of $1$ is as follows: </p><ol> <li> Alice chooses color $1$, discards $1$ marble. Bob also discards $1$ marble; </li><li> Bob chooses color $3$, discards $1$ marble. Alice also discards $1$ marble; </li><li> Alice chooses color $2$, discards $1$ marble, and Bob discards $2$ marble. </li></ol><p>As a result, Alice has $a = [3, 1, 0]$ remaining, and Bob has $b = [0, 0, 3]$ remaining. The score is $3 + 1 - 3 = 1$.</p><p>It can be shown that neither Alice nor Bob can achieve a better score if both play optimally.</p><p>In the second example, Alice can first choose color $1$, then Bob will choose color $4$, after which Alice will choose color $2$, and Bob will choose color $3$. It can be shown that this is the optimal game.</p>
