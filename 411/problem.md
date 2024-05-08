## Description

<div><p>The game of Berland poker is played as follows. There are $n+1$ people: $n$ players, numbered from $1$ to $n$, and the dealer. The dealer has a deck which contains cards of four different suits (the number of cards of each suit <span class="tex-font-style-bf">is not necessarily the same</span>); the number of cards in the deck is divisible by $n$. The dealer gives all cards to the players, so that <span class="tex-font-style-bf">every player receives the same number of cards, and the whole deck is used</span>.</p><p>After the cards are dealt, every player chooses one of four suits (independently) and discards all cards from their hand which do not belong to their chosen suit. The winner of the game is the player with the maximum number of cards left in their hand. The number of points the winner receives is $x - y$, where $x$ is the number of cards in the winner's hand, and $y$ is the maximum number of cards among all <span class="tex-font-style-bf">other</span> players; everyone else receives $0$ points. Note that it means that <span class="tex-font-style-bf">if there are multiple players with the maximum number of cards</span>, everyone receives $0$ points.</p><p>Since every player wants to maximize their odds to win, <span class="tex-font-style-bf">they will choose a suit with the maximum number of cards in their hand</span>.</p><p>Monocarp is the dealer. He has already given some cards to the players; the $i$-th player received $a_{i,j}$ cards of suit $j$. Note that <span class="tex-font-style-bf">the number of cards in players' hands don't have to be the same at this moment</span>. Monocarp has $b_1, b_2, b_3, b_4$ cards of suit $1, 2, 3, 4$ respectively left in his deck. He has to give them to the players so that, after all cards are dealt, every player has the same number of cards.</p><p>For each player, calculate the maximum number of points they can receive among all ways to deal the remaining cards according to the rules of the game.</p></div><div class="input-specification"><p>The first line of the input contains one integer $n$ ($2 \le n \le 5 \cdot 10^4$) — the number of players.</p><p>Then $n$ lines follow. The $i$-th of them contains four integers $a_{i,1}, a_{i,2}, a_{i,3}, a_{i,4}$ ($0 \le a_{i,j} \le 10^6$), where $a_{i,j}$ is the number of cards of the $j$-th suit that the $i$-th player currently has.</p><p>The last line contains $4$ integers $b_1, b_2, b_3, b_4$ ($0 \le b_j \le 10^6$), where $b_j$ is the number of cards of the $j$-th suit Monocarp has to deal yet.</p><p>Additional constraint on the input: it is possible to deal all of the remaining cards so that every player has the same number of cards.</p></div><div class="output-specification"><p>Print $n$ integers. The $i$-th of them should be the maximum number of points the $i$-th player can get among all possible ways to deal the remaining cards.</p></div>

## Input

<p>The first line of the input contains one integer $n$ ($2 \le n \le 5 \cdot 10^4$) — the number of players.</p><p>Then $n$ lines follow. The $i$-th of them contains four integers $a_{i,1}, a_{i,2}, a_{i,3}, a_{i,4}$ ($0 \le a_{i,j} \le 10^6$), where $a_{i,j}$ is the number of cards of the $j$-th suit that the $i$-th player currently has.</p><p>The last line contains $4$ integers $b_1, b_2, b_3, b_4$ ($0 \le b_j \le 10^6$), where $b_j$ is the number of cards of the $j$-th suit Monocarp has to deal yet.</p><p>Additional constraint on the input: it is possible to deal all of the remaining cards so that every player has the same number of cards.</p>

## Output

<p>Print $n$ integers. The $i$-th of them should be the maximum number of points the $i$-th player can get among all possible ways to deal the remaining cards.</p>





```input1
2
3 1 1 1
1 1 1 1
2 2 0 0
```




```input2
4
0 0 0 0
0 0 0 1
2 2 0 0
0 1 0 0
3 2 3 2
```




```input3
7
2 1 0 1
0 0 2 1
4 4 1 2
0 0 1 0
1 1 0 1
0 2 1 1
0 2 0 0
15 10 10 14
```




```output1
1 0
```




```output2
1 1 1 1
```




```output3
5 6 1 7 5 5 7
```


