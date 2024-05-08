## Description

<div><p>Pak Chanek is the chief of a village named Khuntien. On one night filled with lights, Pak Chanek has a sudden and important announcement that needs to be notified to all of the $n$ residents in Khuntien.</p><p>First, Pak Chanek shares the announcement directly to one or more residents with a cost of $p$ for each person. After that, the residents can share the announcement to other residents using a magical helmet-shaped device. However, there is a cost for using the helmet-shaped device. For each $i$, if the $i$-th resident has got the announcement at least once (either directly from Pak Chanek or from another resident), he/she can share the announcement to at most $a_i$ other residents with a cost of $b_i$ <span class="tex-font-style-bf">for each share</span>.</p><p>If Pak Chanek can also control how the residents share the announcement to other residents, what is the minimum cost for Pak Chanek to notify all $n$ residents of Khuntien about the announcement?</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. The following lines contain the description of each test case.</p><p>The first line contains two integers $n$ and $p$ ($1 \leq n \leq 10^5$; $1 \leq p \leq 10^5$) — the number of residents and the cost for Pak Chanek to share the announcement directly to one resident.</p><p>The second line contains $n$ integers $a_1,a_2,a_3,\ldots,a_n$ ($1\leq a_i\leq10^5$) — the maximum number of residents that each resident can share the announcement to.</p><p>The third line contains $n$ integers $b_1,b_2,b_3,\ldots,b_n$ ($1\leq b_i\leq10^5$) — the cost for each resident to share the announcement to one other resident.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output a line containing an integer representing the minimum cost to notify all $n$ residents of Khuntien about the announcement.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. The following lines contain the description of each test case.</p><p>The first line contains two integers $n$ and $p$ ($1 \leq n \leq 10^5$; $1 \leq p \leq 10^5$) — the number of residents and the cost for Pak Chanek to share the announcement directly to one resident.</p><p>The second line contains $n$ integers $a_1,a_2,a_3,\ldots,a_n$ ($1\leq a_i\leq10^5$) — the maximum number of residents that each resident can share the announcement to.</p><p>The third line contains $n$ integers $b_1,b_2,b_3,\ldots,b_n$ ($1\leq b_i\leq10^5$) — the cost for each resident to share the announcement to one other resident.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output a line containing an integer representing the minimum cost to notify all $n$ residents of Khuntien about the announcement.</p>





```input1|2,3,4,8,9,10
3
6 3
2 3 2 1 1 3
4 3 2 6 3 6
1 100000
100000
1
4 94
1 4 2 3
103 96 86 57
```




```output1
16
100000
265
```



## Note

<p>In the first test case, the following is a possible optimal strategy: </p><ol> <li> Pak Chanek shares the announcement directly to the $3$-rd, $5$-th, and $6$-th resident. This requires a cost of $p+p+p=3+3+3=9$. </li><li> The $3$-rd resident shares the announcement to the $1$-st and $2$-nd resident. This requires a cost of $b_3+b_3=2+2=4$. </li><li> The $2$-nd resident shares the announcement to the $4$-th resident. This requires a cost of $b_2=3$. </li></ol><p>The total cost is $9+4+3=16$. It can be shown that there is no other strategy with a smaller cost.</p>
