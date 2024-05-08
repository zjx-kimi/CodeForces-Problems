## Description

<div><p>There are $n$ coins on the table forming a circle, and each coin is either facing up or facing down. Alice and Bob take turns to play the following game, and Alice goes first.</p><p>In each operation, the player chooses a facing-up coin, removes the coin, and flips the two coins that are adjacent to it. If (before the operation) there are only two coins left, then one will be removed and the other won't be flipped (as it would be flipped twice). If (before the operation) there is only one coin left, no coins will be flipped. If (before the operation) there are no facing-up coins, the player loses.</p><p>Decide who will win the game if they both play optimally. It can be proved that the game will end in a finite number of operations, and one of them will win.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1\le t\le 100$). The description of the test cases follows.</p><p>The first line of each test case contains only one positive integer $n$ ($1 \leq n \leq 100$), representing the number of the coins.</p><p>A string $s$ of length $n$ follows on the second line of each test case, containing only "<span class="tex-font-style-tt">U</span>" and "<span class="tex-font-style-tt">D</span>", representing that each coin is facing up or facing down.</p></div><div class="output-specification"><p>For each test case, print "<span class="tex-font-style-tt">YES</span>" if Alice will win the game, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1\le t\le 100$). The description of the test cases follows.</p><p>The first line of each test case contains only one positive integer $n$ ($1 \leq n \leq 100$), representing the number of the coins.</p><p>A string $s$ of length $n$ follows on the second line of each test case, containing only "<span class="tex-font-style-tt">U</span>" and "<span class="tex-font-style-tt">D</span>", representing that each coin is facing up or facing down.</p>

## Output

<p>For each test case, print "<span class="tex-font-style-tt">YES</span>" if Alice will win the game, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p>





```input1|2,3,6,7
3
5
UUDUD
5
UDDUD
2
UU
```




```output1
YES
NO
NO
```



## Note

<p>In the first test case, the game may go as follows.</p><ul> <li> Alice chooses the first coin and $s$ becomes "<span class="tex-font-style-tt">DDUU</span>". </li><li> Bob chooses the last coin and $s$ becomes "<span class="tex-font-style-tt">UDD</span>". </li><li> Alice chooses the first coin and $s$ becomes "<span class="tex-font-style-tt">UU</span>". </li><li> Bob chooses the first coin and $s$ becomes "<span class="tex-font-style-tt">U</span>". </li><li> Alice chooses the only coin and $s$ becomes empty. </li><li> Bob can't choose any coin now, and he loses the game. </li></ul><p>It can be proved that Bob will always lose if they both play optimally.</p>
