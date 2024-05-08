## Description

<div><p>Sasha gave Anna a list $a$ of $n$ integers for Valentine's Day. Anna doesn't need this list, so she suggests destroying it by playing a game.</p><p>Players take turns. Sasha is a gentleman, so he gives Anna the right to make the first move.</p><ul><li> On her turn, <span class="tex-font-style-bf">Anna must</span> choose an element $a_i$ from the list and <span class="tex-font-style-it">reverse</span> the sequence of its digits. For example, if Anna chose the element with a value of $42$, it would become $24$; if Anna chose the element with a value of $1580$, it would become $851$. Note that leading zeros are removed. After such a turn, the number of elements in the list does not change.</li><li> On his turn, <span class="tex-font-style-bf">Sasha must</span> extract <span class="tex-font-style-bf">two</span> elements $a_i$ and $a_j$ ($i \ne j$) from the list, <span class="tex-font-style-it">concatenate</span> them in any order and insert the result back into the list. For example, if Sasha chose the elements equal to $2007$ and $19$, he would remove these two elements from the list and add the integer $200719$ or $192007$. After such a turn, the number of elements in the list decreases by $1$.</li></ul><p>Players can't skip turns. The game ends when Sasha can't make a move, i.e. <span class="tex-font-style-bf">after</span> Anna's move there is <span class="tex-font-style-bf">exactly</span> one number left in the list. If this integer is <span class="tex-font-style-bf">not less than</span> $10^m$ (i.e., $\ge 10^m$), Sasha wins. Otherwise, Anna wins.</p><p>It can be shown that the game will always end. Determine who will win if both players play optimally.</p></div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Then follows the description of the test cases.</p><p>The first line of each test case contains integers $n$, $m$ ($1 \le n \le 2 \cdot 10^5$, $0 \le m \le 2 \cdot 10^6$)&nbsp;— the number of integers in the list and the parameter determining when Sasha wins.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the list that Sasha gave to Anna.</p><p>It is guaranteed that the sum of $n$ for all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output: </p><ul> <li> "<span class="tex-font-style-tt">Sasha</span>", if Sasha wins with optimal play; </li><li> "<span class="tex-font-style-tt">Anna</span>", if Anna wins with optimal play. </li></ul></div>

## Input

<p>The first line contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Then follows the description of the test cases.</p><p>The first line of each test case contains integers $n$, $m$ ($1 \le n \le 2 \cdot 10^5$, $0 \le m \le 2 \cdot 10^6$)&nbsp;— the number of integers in the list and the parameter determining when Sasha wins.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the list that Sasha gave to Anna.</p><p>It is guaranteed that the sum of $n$ for all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output: </p><ul> <li> "<span class="tex-font-style-tt">Sasha</span>", if Sasha wins with optimal play; </li><li> "<span class="tex-font-style-tt">Anna</span>", if Anna wins with optimal play. </li></ul>





```input1|2,3,6,7,10,11,14,15,18,19
9
2 2
14 2
3 5
9 56 1
4 10
1 2007 800 1580
4 5
5000 123 30 4
10 10
6 4 6 2 3 1 10 9 10 7
1 1
6
1 1
10
8 9
1 2 9 10 10 2 10 2
4 5
10 10 10 10
```




```output1
Sasha
Anna
Anna
Sasha
Sasha
Anna
Anna
Anna
Sasha
```



## Note

<p>Consider the first test case.</p><p>Anna can reverse the integer $2$, then Sasha can concatenate the integers $2$ and $14$, obtaining the integer $214$, which is greater than $10^2 = 100$. If Anna had reversed the integer $14$, Sasha would have concatenated the integers $41$ and $2$, obtaining the integer $412$, which is greater than $10^2 = 100$. Anna has no other possible moves, so she loses.</p>
