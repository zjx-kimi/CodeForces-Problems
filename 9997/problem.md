## Description

<div><p>Two players are playing an online card game. The game is played using a 32-card deck. Each card has a suit and a rank. There are four suits: clubs, diamonds, hearts, and spades. We will encode them with characters '<span class="tex-font-style-tt">C</span>', '<span class="tex-font-style-tt">D</span>', '<span class="tex-font-style-tt">H</span>', and '<span class="tex-font-style-tt">S</span>', respectively. And there are 8 ranks, in increasing order: '<span class="tex-font-style-tt">2</span>', '<span class="tex-font-style-tt">3</span>', '<span class="tex-font-style-tt">4</span>', '<span class="tex-font-style-tt">5</span>', '<span class="tex-font-style-tt">6</span>', '<span class="tex-font-style-tt">7</span>', '<span class="tex-font-style-tt">8</span>', '<span class="tex-font-style-tt">9</span>'.</p><p>Each card is denoted by two letters: its rank and its suit. For example, the 8 of Hearts is denoted as <span class="tex-font-style-tt">8H</span>.</p><p>At the beginning of the game, one suit is chosen as the <span class="tex-font-style-bf">trump suit</span>.</p><p>In each round, players make moves like this: the first player places one of his cards on the table, and the second player must beat this card with one of their cards. After that, both cards are moved to the discard pile.</p><p>A card can beat another card if both cards have the same suit and the first card has a higher rank than the second. For example, <span class="tex-font-style-tt">8S</span> can beat <span class="tex-font-style-tt">4S</span>. Additionally, a trump card can beat any non-trump card, regardless of the rank of the cards, for example, if the trump suit is clubs ('<span class="tex-font-style-tt">C</span>'), then <span class="tex-font-style-tt">3C</span> can beat <span class="tex-font-style-tt">9D</span>. Note that trump cards can be beaten only by the trump cards of higher rank.</p><p>There were $n$ rounds played in the game, so the discard pile now contains $2n$ cards. You want to reconstruct the rounds played in the game, but the cards in the discard pile are shuffled. Find any possible sequence of $n$ rounds that might have been played in the game.</p></div><div class="input-specification"><p>The first line contains integer $t$ ($1 \le t \le 100$) — the number of test cases. Then $t$ test cases follow.</p><p>The first line of a test case contains the integer number $n$ ($1\le n\le 16$).</p><p>The second line of a test case contains one character, the trump suit. It is one of "<span class="tex-font-style-tt">CDHS</span>".</p><p>The third line of a test case contains the description of $2n$ cards. Each card is described by a two-character string, the first character is the rank of the card, which is one of "<span class="tex-font-style-tt">23456789</span>", and the second one is the suit of the card, which is one of "<span class="tex-font-style-tt">CDHS</span>". All cards are different.</p></div><div class="output-specification"><p>For each test case print the answer to it:</p><ul><li> Print $n$ lines. In each line, print the description of two cards, in the same format as in the input: the first card that was played by the first player, and then the card that was used by the second player to beat it.</li><li> If there is no solution, print a single line "<span class="tex-font-style-tt">IMPOSSIBLE</span>".</li></ul><p>If there are multiple solutions, print any of them.</p></div>

## Input

<p>The first line contains integer $t$ ($1 \le t \le 100$) — the number of test cases. Then $t$ test cases follow.</p><p>The first line of a test case contains the integer number $n$ ($1\le n\le 16$).</p><p>The second line of a test case contains one character, the trump suit. It is one of "<span class="tex-font-style-tt">CDHS</span>".</p><p>The third line of a test case contains the description of $2n$ cards. Each card is described by a two-character string, the first character is the rank of the card, which is one of "<span class="tex-font-style-tt">23456789</span>", and the second one is the suit of the card, which is one of "<span class="tex-font-style-tt">CDHS</span>". All cards are different.</p>

## Output

<p>For each test case print the answer to it:</p><ul><li> Print $n$ lines. In each line, print the description of two cards, in the same format as in the input: the first card that was played by the first player, and then the card that was used by the second player to beat it.</li><li> If there is no solution, print a single line "<span class="tex-font-style-tt">IMPOSSIBLE</span>".</li></ul><p>If there are multiple solutions, print any of them.</p>





```input1|2,3,4,8,9,10,14,15,16,20,21,22
8
3
S
3C 9S 4C 6D 3S 7S
2
C
3S 5D 9S 6H
1
H
6C 5D
1
S
7S 3S
1
H
9S 9H
1
S
9S 9H
1
C
9D 8H
2
C
9C 9S 6H 8C
```




```output1
3C 4C
6D 9S
3S 7S
IMPOSSIBLE
IMPOSSIBLE
3S 7S
9S 9H
9H 9S
IMPOSSIBLE
6H 9C
9S 8C
```


