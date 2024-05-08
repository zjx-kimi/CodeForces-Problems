## Description

<div><p>Monocarp and Bicarp are playing a card game. Each card has two parameters: an attack value and a defence value. A card $s$ beats another card $t$ if the attack of $s$ is strictly greater than the defence of $t$.</p><p>Monocarp has $n$ cards, the $i$-th of them has an attack value of $\mathit{ax}_i$ and a defence value of $\mathit{ay}_i$. Bicarp has $m$ cards, the $j$-th of them has an attack value of $\mathit{bx}_j$ and a defence value of $\mathit{by}_j$.</p><p>On the first move, Monocarp chooses one of his cards and plays it. Bicarp has to respond with his own card that beats that card. After that, Monocarp has to respond with a card that beats Bicarp's card. After that, it's Bicarp's turn, and so forth.</p><p><span class="tex-font-style-bf">After a card is beaten, it returns to the hand of the player who played it.</span> It implies that each player always has the same set of cards to play as at the start of the game. The game ends when the current player has no cards that beat the card which their opponent just played, and the current player loses.</p><p>If the game lasts for $100^{500}$ moves, it's declared a draw.</p><p>Both Monocarp and Bicarp play optimally. That is, if a player has a winning strategy regardless of his opponent's moves, he plays for a win. Otherwise, if he has a drawing strategy, he plays for a draw.</p><p>You are asked to calculate three values: </p><ul> <li> the number of Monocarp's starting moves that result in a win for Monocarp; </li><li> the number of Monocarp's starting moves that result in a draw; </li><li> the number of Monocarp's starting moves that result in a win for Bicarp. </li></ul></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains an integer $n$ ($1 \le n \le 3 \cdot 10^5$)&nbsp;— the number of cards Monocarp has.</p><p>The second line contains $n$ integers $\mathit{ax}_1, \mathit{ax}_2, \dots, \mathit{ax}_n$ ($1 \le \mathit{ax}_i \le 10^6$)&nbsp;— the attack values of Monocarp's cards.</p><p>The third line contains $n$ integers $\mathit{ay}_1, \mathit{ay}_2, \dots, \mathit{ay}_n$ ($1 \le \mathit{ay}_i \le 10^6$)&nbsp;— the defence values of Monocarp's cards.</p><p>The fourth line contains a single integer $m$ ($1 \le m \le 3 \cdot 10^5$)&nbsp;— the number of cards Bicarp has.</p><p>The fifth line contains $m$ integers $\mathit{bx}_1, \mathit{bx}_2, \dots, \mathit{bx}_m$ ($1 \le \mathit{bx}_j \le 10^6$)&nbsp;— the attack values of Bicarp's cards.</p><p>The sixth line contains $m$ integers $\mathit{by}_1, \mathit{by}_2, \dots, \mathit{by}_m$ ($1 \le \mathit{by}_j \le 10^6$)&nbsp;— the defence values of Bicarp's cards.</p><p>Additional constraints on the input: the sum of $n$ over all test cases doesn't exceed $3 \cdot 10^5$, the sum of $m$ over all test cases doesn't exceed $3 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print three integers: </p><ul> <li> the number of Monocarp's starting moves that result in a win for Monocarp; </li><li> the number of Monocarp's starting moves that result in a draw; </li><li> the number of Monocarp's starting moves that result in a win for Bicarp. </li></ul></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains an integer $n$ ($1 \le n \le 3 \cdot 10^5$)&nbsp;— the number of cards Monocarp has.</p><p>The second line contains $n$ integers $\mathit{ax}_1, \mathit{ax}_2, \dots, \mathit{ax}_n$ ($1 \le \mathit{ax}_i \le 10^6$)&nbsp;— the attack values of Monocarp's cards.</p><p>The third line contains $n$ integers $\mathit{ay}_1, \mathit{ay}_2, \dots, \mathit{ay}_n$ ($1 \le \mathit{ay}_i \le 10^6$)&nbsp;— the defence values of Monocarp's cards.</p><p>The fourth line contains a single integer $m$ ($1 \le m \le 3 \cdot 10^5$)&nbsp;— the number of cards Bicarp has.</p><p>The fifth line contains $m$ integers $\mathit{bx}_1, \mathit{bx}_2, \dots, \mathit{bx}_m$ ($1 \le \mathit{bx}_j \le 10^6$)&nbsp;— the attack values of Bicarp's cards.</p><p>The sixth line contains $m$ integers $\mathit{by}_1, \mathit{by}_2, \dots, \mathit{by}_m$ ($1 \le \mathit{by}_j \le 10^6$)&nbsp;— the defence values of Bicarp's cards.</p><p>Additional constraints on the input: the sum of $n$ over all test cases doesn't exceed $3 \cdot 10^5$, the sum of $m$ over all test cases doesn't exceed $3 \cdot 10^5$.</p>

## Output

<p>For each test case, print three integers: </p><ul> <li> the number of Monocarp's starting moves that result in a win for Monocarp; </li><li> the number of Monocarp's starting moves that result in a draw; </li><li> the number of Monocarp's starting moves that result in a win for Bicarp. </li></ul>





```input1|2,3,4,5,6,7,14,15,16,17,18,19
3
3
8 7 4
7 1 10
2
8 4
5 10
9
8 8 5 5 5 4 4 1 4
2 7 5 2 8 9 7 1 9
10
9 8 7 6 5 5 4 3 2 1
7 1 6 7 5 8 8 4 9 6
1
10
5
1
10
5
```




```output1
1 1 1
2 4 3
0 1 0
```


