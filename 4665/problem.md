## Description

<div><p>Monocarp is playing a computer game (yet again). Guess what is he doing? That's right, killing monsters.</p><p>There are $n$ monsters in a row, numbered from $1$ to $n$. The $i$-th monster has two parameters: attack value equal to $a_i$ and defense value equal to $d_i$. In order to kill these monsters, Monocarp put a berserk spell on them, so they're attacking each other instead of Monocarp's character.</p><p>The fight consists of $n$ rounds. Every round, the following happens:</p><ul> <li> first, every alive monster $i$ deals $a_i$ damage to the <span class="tex-font-style-bf">closest</span> alive monster to the left (if it exists) and the <span class="tex-font-style-bf">closest</span> alive monster to the right (if it exists); </li><li> then, every alive monster $j$ which received more than $d_j$ damage <span class="tex-font-style-bf">during this round</span> dies. I. e. the $j$-th monster dies if and only if its defense value $d_j$ is <span class="tex-font-style-bf">strictly less</span> than the total damage it received <span class="tex-font-style-bf">this round</span>. </li></ul><p>For each round, calculate the number of monsters that will die during that round.</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of three lines:</p><ul> <li> the first line contains one integer $n$ ($1 \le n \le 3 \cdot 10^5$); </li><li> the second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$); </li><li> the third line contains $n$ integers $d_1, d_2, \dots, d_n$ ($1 \le d_i \le 10^9$). </li></ul><p>Additional constraint on the input: the sum of $n$ over all test cases does not exceed $3 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print $n$ integers. The $i$-th integer should be equal to the number of monsters that die during the $i$-th round.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of three lines:</p><ul> <li> the first line contains one integer $n$ ($1 \le n \le 3 \cdot 10^5$); </li><li> the second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$); </li><li> the third line contains $n$ integers $d_1, d_2, \dots, d_n$ ($1 \le d_i \le 10^9$). </li></ul><p>Additional constraint on the input: the sum of $n$ over all test cases does not exceed $3 \cdot 10^5$.</p>

## Output

<p>For each test case, print $n$ integers. The $i$-th integer should be equal to the number of monsters that die during the $i$-th round.</p>





```input1|2,3,4,8,9,10
3
5
3 4 7 5 10
4 9 1 18 1
2
2 1
1 3
4
1 1 2 4
3 3 4 2
```




```output1
3 1 0 0 0 
0 0 
1 1 1 0
```



## Note

<p>Explanation for the first test case of the example:</p><p>During the first round, the following happens:</p><ul> <li> the monster $1$ deals $3$ damage to the monster $2$; </li><li> the monster $2$ deals $4$ damage to the monster $1$ and the monster $3$; </li><li> the monster $3$ deals $7$ damage to the monster $2$ and the monster $4$; </li><li> the monster $4$ deals $5$ damage to the monster $3$ and the monster $5$; </li><li> the monster $5$ deals $10$ damage to the monster $4$; </li><li> the monster $1$ does not die, since it received $4$ damage and its defense is $4$; </li><li> the monster $2$ dies, since it received $10$ damage and its defense is $9$; </li><li> the monster $3$ dies, since it received $9$ damage and its defense is $1$; </li><li> the monster $4$ does not die, since it received $17$ damage and its defense is $18$; </li><li> the monster $5$ dies, since it received $5$ damage and its defense is $1$. </li></ul><p>After the first round, the monsters $1$ and $4$ stay alive.</p><p>During the second round, the following happens:</p><ul> <li> the monster $1$ deals $3$ damage to the monster $4$; </li><li> the monster $4$ deals $5$ damage to the monster $1$; </li><li> the monster $1$ dies, since it received $5$ damage and its defense is $4$; </li><li> the monster $4$ does not die, since it received $3$ damage and its defense is $18$. </li></ul><p>During the next three rounds, only the $4$-th monster is alive, so nothing happens.</p>
