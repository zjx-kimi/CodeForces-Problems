## Description

<div><p><span class="tex-font-style-bf">This is a hard version of the problem. It differs from the easy one only by constraints on $n$ and $t$</span>.</p><p>There is a deck of $n$ cards, each of which is characterized by its power. There are two types of cards:</p><ul> <li> a hero card, the power of such a card is always equal to $0$; </li><li> a bonus card, the power of such a card is always positive. </li></ul><p>You can do the following with the deck:</p><ul> <li> take a card from the top of the deck; </li><li> if this card is a bonus card, you can put it <span class="tex-font-style-bf">on top</span> of your bonus deck or discard; </li><li> if this card is a hero card, then the power of <span class="tex-font-style-bf">the top</span> card from your bonus deck is added to his power (if it is not empty), after that the hero is added to your army, and the used bonus discards. </li></ul><p>Your task is to use such actions to gather an army with the maximum possible total power.</p></div><div class="input-specification"><p>The first line of input data contains single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases in the test.</p><p>The first line of each test case contains one integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of cards in the deck.</p><p>The second line of each test case contains $n$ integers $s_1, s_2, \dots, s_n$ ($0 \le s_i \le 10^9$)&nbsp;— card powers in top-down order.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>Output $t$ numbers, each of which is the answer to the corresponding test case — the maximum possible total power of the army that can be achieved.</p></div>

## Input

<p>The first line of input data contains single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases in the test.</p><p>The first line of each test case contains one integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of cards in the deck.</p><p>The second line of each test case contains $n$ integers $s_1, s_2, \dots, s_n$ ($0 \le s_i \le 10^9$)&nbsp;— card powers in top-down order.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>Output $t$ numbers, each of which is the answer to the corresponding test case — the maximum possible total power of the army that can be achieved.</p>





```input1|2,3,6,7,10,11
5
5
3 3 3 0 0
6
0 3 3 0 0 3
7
1 2 3 0 4 5 0
7
1 2 5 0 4 3 0
5
3 1 0 0 4
```




```output1
6
6
8
9
4
```



## Note

<p>In the first sample, you can take bonuses $1$ and $2$. Both hero cards will receive $3$ power. If you take all the bonuses, one of them will remain unused.</p><p>In the second sample, the hero's card on top of the deck cannot be powered up, and the rest can be powered up with $2$ and $3$ bonuses and get $6$ total power.</p><p>In the fourth sample, you can take bonuses $1$, $2$, $3$, $5$ and skip the bonus $6$, then the hero $4$ will be enhanced with a bonus $3$ by $5$, and the hero $7$ with a bonus $5$ by $4$. $4+5=9$.</p>
