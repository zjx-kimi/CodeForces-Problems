## Description

<div><p>There are $n$ people that will participate in voting. Each person has exactly one vote.</p><p>$i$-th person has a team $t_i$ ($1 \leq t_i \leq n$) where $t_i = t_j$ means $i$, $j$ are in the same team. By the rules each person should vote for the person from the different team. Note that it automatically means that each person can't vote for himself.</p><p>Each person knows the number of votes $c_i$ he wants to get. How many possible votings exists, such that each person will get the desired number of votes? Due to this number can be big, find it by modulo $998\,244\,353$.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($1 \leq n \leq 200$) — the number of people.</p><p>The second line contains $n$ integers $c_1, c_2, \ldots, c_n$ ($0 \leq c_i \leq n$) — desired number of votes. It is guaranteed, that $\sum\limits_{i=1}^{n} c_i = n$.</p><p>The third line contains $n$ integers $t_1, t_2, \ldots, t_n$ ($1 \leq t_i \leq n$) — team numbers.</p></div><div class="output-specification"><p>Print a single integer — the number of possible votings by modulo $998\,244\,353$.</p></div>

## Input

<p>The first line contains a single integer $n$ ($1 \leq n \leq 200$) — the number of people.</p><p>The second line contains $n$ integers $c_1, c_2, \ldots, c_n$ ($0 \leq c_i \leq n$) — desired number of votes. It is guaranteed, that $\sum\limits_{i=1}^{n} c_i = n$.</p><p>The third line contains $n$ integers $t_1, t_2, \ldots, t_n$ ($1 \leq t_i \leq n$) — team numbers.</p>

## Output

<p>Print a single integer — the number of possible votings by modulo $998\,244\,353$.</p>





```input1
3
1 1 1
1 2 3
```




```input2
5
2 0 1 0 2
1 2 3 4 5
```




```input3
5
1 2 2 0 0
3 5 4 3 4
```




```output1
2
```




```output2
10
```




```output3
5
```



## Note

<p>In the first test there are two possible votings: $(2, 3, 1)$, $(3, 1, 2)$.</p><p>In the third test there are five possible votings: $(3, 3, 2, 2, 1)$, $(2, 3, 2, 3, 1)$, $(3, 3, 1, 2, 2)$, $(3, 1, 2, 3, 2)$, $(2, 3, 1, 3, 2)$.</p>
