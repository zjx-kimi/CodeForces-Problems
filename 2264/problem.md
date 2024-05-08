## Description

<div><p><span class="tex-font-style-bf">The only difference between the easy and hard versions is that the given string $s$ in the easy version is initially a palindrome, this condition is not always true for the hard version.</span></p><p>A palindrome is a string that reads the same left to right and right to left. For example, "<span class="tex-font-style-tt">101101</span>" is a palindrome, while "<span class="tex-font-style-tt">0101</span>" is not.</p><p>Alice and Bob are playing a game on a string $s$ <span class="tex-font-style-bf">(which is initially a palindrome in this version)</span> of length $n$ consisting of the characters '<span class="tex-font-style-tt">0</span>' and '<span class="tex-font-style-tt">1</span>'. Both players take alternate turns with Alice going first.</p><p>In each turn, the player can perform one of the following operations: </p><ol> <li> Choose any $i$ ($1 \le i \le n$), where $s[i] =$ '<span class="tex-font-style-tt">0</span>' and change $s[i]$ to '<span class="tex-font-style-tt">1</span>'. Pay 1 dollar. </li><li> Reverse the whole string, pay 0 dollars. This operation is only allowed if the string is currently <span class="tex-font-style-bf">not</span> a palindrome, and the last operation was not reverse. That is, if Alice reverses the string, then Bob can't reverse in the next move, and vice versa. </li></ol><p>Reversing a string means reordering its letters from the last to the first. For example, "<span class="tex-font-style-tt">01001</span>" becomes "<span class="tex-font-style-tt">10010</span>" after reversing.</p><p>The game ends when every character of string becomes '<span class="tex-font-style-tt">1</span>'. The player who spends minimum dollars till this point wins the game and it is a draw if both spend equal dollars. If both players play optimally, output whether Alice wins, Bob wins, or if it is a draw.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^3$). Then $t$ test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^3$).</p><p>The second line of each test case contains the string $s$ of length $n$, consisting of the characters '<span class="tex-font-style-tt">0</span>' and '<span class="tex-font-style-tt">1</span>'. It is guaranteed that the string $s$ is a palindrome and contains at least one '<span class="tex-font-style-tt">0</span>'. </p><p>Note that there is no limit on the sum of $n$ over test cases.</p></div><div class="output-specification"><p>For each test case print a single word in a new line: </p><ul> <li> "<span class="tex-font-style-tt">ALICE</span>", if Alice will win the game, </li><li> "<span class="tex-font-style-tt">BOB</span>", if Bob will win the game, </li><li> "<span class="tex-font-style-tt">DRAW</span>", if the game ends in a draw. </li></ul></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^3$). Then $t$ test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^3$).</p><p>The second line of each test case contains the string $s$ of length $n$, consisting of the characters '<span class="tex-font-style-tt">0</span>' and '<span class="tex-font-style-tt">1</span>'. It is guaranteed that the string $s$ is a palindrome and contains at least one '<span class="tex-font-style-tt">0</span>'. </p><p>Note that there is no limit on the sum of $n$ over test cases.</p>

## Output

<p>For each test case print a single word in a new line: </p><ul> <li> "<span class="tex-font-style-tt">ALICE</span>", if Alice will win the game, </li><li> "<span class="tex-font-style-tt">BOB</span>", if Bob will win the game, </li><li> "<span class="tex-font-style-tt">DRAW</span>", if the game ends in a draw. </li></ul>





```input1
2
4
1001
1
0
```




```output1
BOB
BOB
```



## Note

<p>In the first test case of the example, </p><ul> <li> in the $1$-st move Alice has to perform the $1$-st operation, since the string is currently a palindrome. </li><li> in the $2$-nd move Bob reverses the string. </li><li> in the $3$-rd move Alice again has to perform the $1$-st operation. All characters of the string are '<span class="tex-font-style-tt">1</span>', game over. </li></ul> Alice spends $2$ dollars while Bob spends $0$ dollars. Hence, Bob always wins.
