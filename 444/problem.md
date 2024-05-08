## Description

<div><p>Michael and Brian are stuck in a hotel with $n$ rooms, numbered from $1$ to $n$, and need to find each other. But this hotel's doors are all locked and the only way of getting around is by using the teleporters in each room. Room $i$ has a teleporter that will take you to room $a_i$ (it might be that $a_i = i$). But they don't know the values of $a_1,a_2, \dots, a_n$.</p><p>Instead, they can call up the front desk to ask queries. In one query, they give a room $u$, a positive integer $k$, and a set of rooms $S$. The hotel concierge answers whether a person starting in room $u$, and using the teleporters $k$ times, ends up in a room in $S$.</p><p>Brian is in room $1$. Michael wants to know the set $A$ of rooms so that if he starts in one of those rooms they can use the teleporters to meet up. He can ask at most $2000$ queries.</p><p>The values $a_1, a_2, \dots, a_n$ are fixed before the start of the interaction and do not depend on your queries. In other words, the interactor is not adaptive.</p></div><div class="input-specification"><p>The input contains a single integer $n$ ($2 \leq n \leq 500$).</p></div><div><h2>Interaction</h2><p>To ask a query, print a line in the format "<span class="tex-font-style-tt">? u k |S| S_1 S_2 ... S_|S|</span>" with $1 \leq u, S_1, \ldots, S_{|S|} \leq n$, all the $S_i$ distinct, and $1 \leq k \leq 10^9$.</p><p>As a response to the query you will get "<span class="tex-font-style-tt">1</span>" if the answer is yes, and "<span class="tex-font-style-tt">0</span>" if the answer is no.</p><p>To output an answer, you should print "<span class="tex-font-style-tt">! |A| A_1 A_2 ... A_|A|</span>" with $1 \leq A_1, \ldots, A_{|A|} \leq n$ all distinct. Printing the answer doesn't count as a query.</p><p>See the interaction example for more clarity.</p><p>If you ask too many queries or you ask a malformed query, you will get <span class="tex-font-style-tt">Wrong answer</span>.</p><p>After printing a query do not forget to output the end of line and flush the output. Otherwise, you will get <span class="tex-font-style-tt">Idleness limit exceeded</span>. To do this, use:</p><ul> <li> <span class="tex-font-style-tt">fflush(stdout)</span> or <span class="tex-font-style-tt">cout.flush()</span> in C++; </li><li> <span class="tex-font-style-tt">System.out.flush()</span> in Java; </li><li> <span class="tex-font-style-tt">flush(output)</span> in Pascal; </li><li> <span class="tex-font-style-tt">stdout.flush()</span> in Python; </li><li> see the documentation for other languages. </li></ul><p><span class="tex-font-style-bf">Hack format</span></p><p>For the hacks use the following format.</p><p>The first line should contain $n$ — the number of rooms.</p><p>The second line should contains $n$ integers $a_1, a_2, \dots, a_n$ — the teleporter in room $i$ leads to room $a_i$.</p></div>

## Input

<p>The input contains a single integer $n$ ($2 \leq n \leq 500$).</p>





```input1
5

0

1
```




```output1
? 3 5 2 2 3

? 2 5 2 2 3

! 3 1 3 4
```



## Note

<p>In the sample test, there are $n=5$ rooms and the (hidden) array describing the behavior of the teleporters is $[1, 2, 1, 3, 2]$.</p><ul> <li> The first query asks whether starting from room number $a=3$, and using the teleporters $5$ times, one ends up in one of the two rooms $S=\{2, 3\}$. This action results in ending up in the room $1$, so the answer is $0$. </li><li> The second query asks whether starting from room number $a=2$, and using the teleporters $5$ times, one ends up in one of the two rooms $S=\{2, 3\}$. This action results in ending up in the room $2$, so the answer is $1$. </li></ul>
