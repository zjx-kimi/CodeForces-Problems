## Description

<div><p><span class="tex-font-style-it">Divan</span>'s new cottage is finally complete! However, after a thorough inspection, it turned out that the workers had installed the insulation incorrectly, and now the temperature in the house directly depends on the temperature outside. More precisely, if the temperature in the house is $P$ in the morning, and the street temperature is $T$, then by the next morning the temperature in the house changes according to the following rule: </p><ul> <li> $P_{new} = P + 1$, if $P &lt; T$, </li><li> $P_{new} = P - 1$, if $P &gt; T$, </li><li> $P_{new} = P$, if $P = T$. </li></ul> Here $P_{new}$ is the temperature in the house next morning.<p><span class="tex-font-style-it">Divan</span> is a very busy businessman, so sometimes he is not at home for long periods and does not know what the temperature is there now, so he hired you to find it. You will work for $n$ days. In the beginning of the $i$-th day, the temperature outside $T_i$ is first given to you. After that, on the $i$-th day, you will receive $k_i$ queries. Each query asks the following: "if the temperature in the house was $x_i$ at the morning of the <span class="tex-font-style-bf">first</span> day, what would be the temperature in the house next morning (after day $i$)?"</p><p>Please answer all the businessman's queries.</p></div><div class="input-specification"><p>The first line of the input contains the number $n$ ($1 \leq n \leq 2 \cdot 10^5$) — the number of days.</p><p>The following is a description of $n$ days in the following format.</p><p>The first line of the description contains an integer $T_i$ ($0 \leq T_i \leq 10^9$) — the temperature on that day.</p><p>The second line contains a non-negative integer $k_i$ ($0 \le k_i \le 2 \cdot 10^5$) — the number of queries that day.</p><p>The third line contains $k$ integers $x'_i$ ($0 \leq x'_{i} \leq 10^9$) — the encrypted version of Divan's queries.</p><p>Let $lastans = 0$ initially. Divan's actual queries are given by $x_i = (x'_i + lastans) \bmod (10^9 + 1)$, where $a \bmod b$ is the reminder when $a$ is divided by $b$. After answering the query, set $lastans$ to the answer.</p><p>It is guaranteed that the total number of queries (the sum of all $k_i$) does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each query, output a single integer — the temperature in the house after day $i$.</p></div>

## Input

<p>The first line of the input contains the number $n$ ($1 \leq n \leq 2 \cdot 10^5$) — the number of days.</p><p>The following is a description of $n$ days in the following format.</p><p>The first line of the description contains an integer $T_i$ ($0 \leq T_i \leq 10^9$) — the temperature on that day.</p><p>The second line contains a non-negative integer $k_i$ ($0 \le k_i \le 2 \cdot 10^5$) — the number of queries that day.</p><p>The third line contains $k$ integers $x'_i$ ($0 \leq x'_{i} \leq 10^9$) — the encrypted version of Divan's queries.</p><p>Let $lastans = 0$ initially. Divan's actual queries are given by $x_i = (x'_i + lastans) \bmod (10^9 + 1)$, where $a \bmod b$ is the reminder when $a$ is divided by $b$. After answering the query, set $lastans$ to the answer.</p><p>It is guaranteed that the total number of queries (the sum of all $k_i$) does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each query, output a single integer — the temperature in the house after day $i$.</p>





```input1
3
50
3
1 2 3
50
3
4 5 6
0
3
7 8 9
```




```input2
4
728
3
859 1045 182
104
1
689
346
6
634 356 912 214 1 1
755
3
241 765 473
```




```input3
2
500000000
3
1000000000 999999999 888888888
250000000
5
777777777 666666666 555555555 444444444 333333333
```




```output1
2
5
9
15
22
30
38
47
53
```




```output2
858
1902
2083
2770
3401
3754
4663
4874
4872
4870
5107
5868
6337
```




```output3
999999999
999999996
888888882
666666656
333333321
888888874
333333317
666666648
```



## Note

<p>Let's look at the first four queries from the example input.</p><p>The temperature is $50$ on the first day, $50$ on the second day, and $0$ on the third day.</p><p>Note that $lastans = 0$ initially.</p><ul><li> The initial temperature of the first query of the first day is $(1 \, + \, lastans) \bmod (10^9 + 1) = 1$. After the first day, the temperature rises by $1$, because $1 &lt; 50$. So the answer to the query is $2$. Then, we set $lastans = 2$.</li><li> The initial temperature of the second query of the first day is $(2 \, + \, lastans) \bmod (10^9 + 1) = 4$. After the first day, the temperature rises by $1$, because $4 &lt; 50$. So the answer to the query is $5$. Then, we set $lastans = 5$.</li><li> The initial temperature of the third query of the first day is $(3 \, + \, lastans) \bmod (10^9 + 1) = 8$. After the first day, the temperature rises by $1$. So the answer to the query is $9$. Then, we set $lastans = 9$.</li><li> The initial temperature of the first query of the second day is $(4 \, + \, lastans) \bmod (10^9 + 1) = 13$. After the first day, the temperature rises by $1$. After the second day, the temperature rises by $1$. So the answer to the query is $15$. Then, we set $lastans = 15$.</li></ul>
