## Description

<div><p>Andrea is playing the game <span class="tex-font-style-it">Tanto Cuore</span>.</p><center> <img class="tex-graphics" src="file://ZCvQz9fC.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p><span class="tex-font-style-paragraph"></span></p><p>He has a deck of $n$ cards with values $a_1, \ldots, a_n$ from top to bottom. Each card can be either locked or unlocked. Initially, only the topmost card is unlocked. </p><p>The game proceeds in turns. In each turn, Andrea chooses an unlocked card in the deck — the value written on the card is $v$ — and performs exactly one of the following two operations: </p><ol> <li> Unlock the first $v$ <span class="tex-font-style-bf">locked</span> cards in the deck from the top. If there are less than $v$ locked cards in the deck, then unlock all the locked cards. </li><li> Earn $v$ <span class="tex-font-style-underline">victory points</span>. </li></ol> In both cases, after performing the operation, he removes the card from the deck.<p>The game ends when all the cards remaining in the deck are locked, or there are no more cards in the deck.</p><p>What is the maximum number of victory points Andrea can earn?</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($1 \leq n \leq 10^5$) — the number of cards in the deck.</p><p>The second line contains $n$ integers $a_1, \ldots, a_n$ ($0 \leq a_1, \ldots, a_n \leq n$) — the values of the cards in the deck.</p></div><div class="output-specification"><p>Output a single integer — the maximum number of victory points Andrea can earn.</p></div>

## Input

<p>The first line contains a single integer $n$ ($1 \leq n \leq 10^5$) — the number of cards in the deck.</p><p>The second line contains $n$ integers $a_1, \ldots, a_n$ ($0 \leq a_1, \ldots, a_n \leq n$) — the values of the cards in the deck.</p>

## Output

<p>Output a single integer — the maximum number of victory points Andrea can earn.</p>





```input1
2
1 2
```




```input2
5
2 4 5 0 1
```




```input3
4
0 4 4 4
```




```output1
2
```




```output2
9
```




```output3
0
```



## Note

<p>In the first sample test, the deck starts as [unlocked, locked]. Then, Andrea uses the first card to unlock the second card. Then he uses the second card to earn $2$ victory points.</p><p>In the second sample test, Andrea can use the first card to unlock the second and the third card. Then he uses the second and the third card to earn $4+5=9$ victory points.</p><p>In the third sample test, Andrea can't unlock any cards or gain any victory points with the first card.</p>
