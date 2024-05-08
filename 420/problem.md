## Description

<div><p>Alice and Bob are playing a game. They have a permutation $p$ of size $n$ (a permutation of size $n$ is an array of size $n$ where each element from $1$ to $n$ occurs exactly once). They also have a chip, which can be placed on any element of the permutation.</p><p>Alice and Bob make alternating moves: Alice makes the first move, then Bob makes the second move, then Alice makes the third move, and so on. During the first move, Alice chooses any element of the permutation and places the chip on that element. During each of the next moves, the current player <span class="tex-font-style-bf">has to</span> move the chip to any element that is simultaneously to the left and strictly less than the current element (i. e. if the chip is on the $i$-th element, it can be moved to the $j$-th element if $j &lt; i$ and $p_j &lt; p_i$). If a player cannot make a move (it is impossible to move the chip according to the rules of the game), that player <span class="tex-font-style-bf">wins</span> the game.</p><p>Let's say that the $i$-th element of the permutation is <span class="tex-font-style-bf">lucky</span> if the following condition holds:</p><ul> <li> if Alice places the chip on the $i$-th element during her first move, she can win the game no matter how Bob plays (i. e. she has a winning strategy). </li></ul><p>You have to calculate the number of lucky elements in the permutation.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 3 \cdot 10^5$)&nbsp;– the number of elements in the permutation.</p><p>The second line contains $n$ integers $p_1, p_2, \dots, p_n$ ($1 \le p_i \le n$). All $p_i$ are distinct. </p><p>The sum of $n$ over all test cases doesn't exceed $3 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print a single integer&nbsp;— the number of lucky elements in the permutation.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 3 \cdot 10^5$)&nbsp;– the number of elements in the permutation.</p><p>The second line contains $n$ integers $p_1, p_2, \dots, p_n$ ($1 \le p_i \le n$). All $p_i$ are distinct. </p><p>The sum of $n$ over all test cases doesn't exceed $3 \cdot 10^5$.</p>

## Output

<p>For each test case, print a single integer&nbsp;— the number of lucky elements in the permutation.</p>





```input1|2,3,6,7
4
3
2 1 3
2
2 1
3
1 2 3
4
2 1 4 3
```




```output1
1
0
1
2
```



## Note

<p>In the first test case of the example, the $3$-rd element of the permutation is lucky.</p><p>In the second test case of the example, there are no lucky elements.</p><p>In the third test case of the example, the $2$-nd element of the permutation is lucky.</p><p>In the fourth test case of the example, the $3$-rd and the $4$-th element of the permutation are lucky.</p>
