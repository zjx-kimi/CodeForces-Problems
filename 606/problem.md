## Description

<div><p>There is a group of $n$ people. Some of them might be liars, who <span class="tex-font-style-bf">always</span> tell lies. Other people <span class="tex-font-style-bf">always</span> tell the truth. The $i$-th person says "There are at least $l_i$ liars amongst us". Determine if what people are saying is contradictory, or if it is possible. If it is possible, output the number of liars in the group. If there are multiple possible answers, output any one of them.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$) — the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 100$).</p><p>The second line of each test case contains $n$ integers $l_i$ ($0 \leq l_i \leq n$) — the number said by the $i$-th person.</p><p>It's guaranteed that the sum of all $n$ does not exceed $10^4$.</p></div><div class="output-specification"><p>For each test case output a single integer. If what people are saying is contradictory, output $-1$. Otherwise, output the number of liars in the group. If there are multiple possible answers, output any one of them.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$) — the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 100$).</p><p>The second line of each test case contains $n$ integers $l_i$ ($0 \leq l_i \leq n$) — the number said by the $i$-th person.</p><p>It's guaranteed that the sum of all $n$ does not exceed $10^4$.</p>

## Output

<p>For each test case output a single integer. If what people are saying is contradictory, output $-1$. Otherwise, output the number of liars in the group. If there are multiple possible answers, output any one of them.</p>





```input1|2,3,6,7,10,11,14,15
7
2
1 2
2
2 2
2
0 0
1
1
1
0
5
5 5 3 3 5
6
5 3 6 6 3 5
```




```output1
1
-1
0
-1
0
3
4
```



## Note

<p>In the first example, the only possible answer is that the second person is a liar, so the answer is $1$ liar.</p><p>In the second example, it can be proven that we can't choose the liars so that all the requirements are satisfied.</p><p>In the third example, everybody tells the truth, so the answer is $0$ liars.</p>
