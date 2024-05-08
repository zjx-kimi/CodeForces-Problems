## Description

<div><p>You are playing a deck-building game with your friend. There are $N$ cards, numbered from $1$ to $N$. Card $i$ has the value of $A_i$.</p><p>You want to build two decks; one for you and one for your friend. A card cannot be inside both decks, and it is allowed to not use all $N$ cards. It is also allowed for a deck to be empty, i.e. does not contain any cards.</p><p>The <span class="tex-font-style-bf">power</span> of a deck is represented as the bitwise XOR of the value of the cards in the deck. The power of an empty deck is $0$.</p><p>The game is <span class="tex-font-style-bf">balanced</span> if both decks have the same power.</p><p>Determine the number of ways to build two decks such that the game is balanced. Two ways are considered different if one of the decks contains at least one different card. Since the answer can be very large, calculate the answer modulo $998\,244\,353$.</p></div><div class="input-specification"><p>The first line consists of an integer $N$ ($2 \le N \le 100\,000$).</p><p>The following line consists of $N$ integers $A_i$ ($1 \le A_i \le 100\,000$).</p></div><div class="output-specification"><p>Output an integer representing the number of ways to build two decks such that the game is balanced. Output the answer modulo $998\,244\,353$.</p></div>

## Input

<p>The first line consists of an integer $N$ ($2 \le N \le 100\,000$).</p><p>The following line consists of $N$ integers $A_i$ ($1 \le A_i \le 100\,000$).</p>

## Output

<p>Output an integer representing the number of ways to build two decks such that the game is balanced. Output the answer modulo $998\,244\,353$.</p>





```input1
4
16 12 4 8
```




```input2
4
1 2 4 8
```




```input3
2
1 1
```




```input4
6
1 1 1 2 2 2
```




```output1
9
```




```output2
1
```




```output3
5
```




```output4
169
```



## Note

<p><span class="tex-font-style-it">Explanation for the sample input/output #1</span></p><p>Denote $S$ and $T$ as the set of cards in your deck and your friend's deck, respectively. There are $9$ ways to build the decks such that the game is balanced.</p><ul> <li> $S = \{\}$ and $T = \{\}$. Both decks have the power of $0$. </li><li> $S = \{2, 3, 4\}$ and $T = \{\}$. Both decks have the power of $0$. </li><li> $S = \{\}$ and $T = \{2, 3, 4\}$. Both decks have the power of $0$. </li><li> $S = \{2, 4\}$ and $T = \{3\}$. Both decks have the power of $4$. </li><li> $S = \{3\}$ and $T = \{2, 4\}$. Both decks have the power of $4$. </li><li> $S = \{2, 3\}$ and $T = \{4\}$. Both decks have the power of $8$. </li><li> $S = \{4\}$ and $T = \{2, 3\}$. Both decks have the power of $8$. </li><li> $S = \{3, 4\}$ and $T = \{2\}$. Both decks have the power of $12$. </li><li> $S = \{2\}$ and $T = \{3, 4\}$. Both decks have the power of $12$. </li></ul><p><span class="tex-font-style-it">Explanation for the sample input/output #2</span></p><p>The only way to make the game balanced is to have both decks empty.</p><p><span class="tex-font-style-it">Explanation for the sample input/output #3</span></p><p>There are $5$ ways to build the decks such that the game is balanced.</p><ul> <li> $S = \{\}$ and $T = \{\}$. Both decks have the power of $0$. </li><li> $S = \{1, 2\}$ and $T = \{\}$. Both decks have the power of $0$. </li><li> $S = \{\}$ and $T = \{1, 2\}$. Both decks have the power of $0$. </li><li> $S = \{1\}$ and $T = \{2\}$. Both decks have the power of $1$. </li><li> $S = \{2\}$ and $T = \{1\}$. Both decks have the power of $1$. </li></ul>
