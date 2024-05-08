## Description

<div><p>Alice and Bob are bored, so they decide to play a game with their wallets. Alice has $a$ coins in her wallet, while Bob has $b$ coins in his wallet.</p><p>Both players take turns playing, with Alice making the first move. In each turn, the player will perform the following steps <span class="tex-font-style-bf">in order</span>:</p><ol> <li> Choose to exchange wallets with their opponent, or to keep their current wallets. </li><li> Remove $1$ coin from the player's current wallet. The current wallet cannot have $0$ coins before performing this step. </li></ol><p>The player who cannot make a valid move on their turn loses. If both Alice and Bob play optimally, determine who will win the game.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first and only line of each test case contains two integers $a$ and $b$ ($1 \le a, b \le 10^9$)&nbsp;— the number of coins in Alice's and Bob's wallets, respectively.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">Alice</span>" if Alice will win the game, and "<span class="tex-font-style-tt">Bob</span>" if Bob will win the game.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first and only line of each test case contains two integers $a$ and $b$ ($1 \le a, b \le 10^9$)&nbsp;— the number of coins in Alice's and Bob's wallets, respectively.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">Alice</span>" if Alice will win the game, and "<span class="tex-font-style-tt">Bob</span>" if Bob will win the game.</p>





```input1|2,4,6,8,10
10
1 1
1 4
5 3
4 5
11 9
83 91
1032 9307
839204 7281
1000000000 1000000000
53110 2024
```




```output1
Bob
Alice
Bob
Alice
Bob
Bob
Alice
Alice
Bob
Bob
```



## Note

<p>In the first test case, an example of the game is shown below:</p><ul> <li> Alice chooses to not swap wallets with Bob in step 1 of her move. Now, $a=0$ and $b=1$. </li><li> Since Alice's wallet is empty, Bob must choose to not swap their wallets in step 1 of his move. Now, $a=0$ and $b=0$. </li><li> Since both Alice's and Bob's wallets are empty, Alice is unable to make a move. Hence, Bob wins. </li></ul><p>In the second test case, an example of the game is shown below:</p><ul> <li> Alice chooses to swap wallets with Bob in step 1 of her move. Now, $a=3$ and $b=1$. </li><li> Bob chooses to swap wallets with Alice in step 1 of his move. Now, $a=1$ and $b=2$. </li><li> Alice chooses to not swap wallets with Bob in step 1 of her move. Now, $a=0$ and $b=2$. </li><li> Since Alice's wallet is empty, Bob can only choose to not swap wallets with Alice in step 1 of his move. Now, $a=0$ and $b=1$. </li><li> Since Alice's wallet is empty, Alice can only choose to swap wallets with Bob in step 1 of her move. Now, $a=0$ and $b=0$. </li><li> Since both Alice's wallet and Bob's wallet are empty, Bob is unable to make a move. Hence, Alice wins. </li></ul>
