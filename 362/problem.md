## Description

<div><p>During the summer vacation after Zhongkao examination, Tom and Daniel are planning to go traveling.</p><p>There are $n$ cities in their country, numbered from $1$ to $n$. And the traffic system in the country is very special. For each city $i$ ($1 \le i \le n$), there is</p><ul> <li> a road between city $i$ and $2i$, if $2i\le n$; </li><li> a road between city $i$ and $2i+1$, if $2i+1\le n$. </li></ul><p>Making a travel plan, Daniel chooses some integer value between $1$ and $m$ for each city, for the $i$-th city we denote it by $a_i$.</p><p>Let $s_{i,j}$ be the maximum value of cities in the simple$^\dagger$ path between cities $i$ and $j$. The <span class="tex-font-style-it">score</span> of the travel plan is $\sum_{i=1}^n\sum_{j=i}^n s_{i,j}$. </p><p>Tom wants to know the sum of scores of all possible travel plans. Daniel asks you to help him find it. You just need to tell him the answer modulo $998\,244\,353$.</p><p>$^\dagger$ A simple path between cities $x$ and $y$ is a path between them that passes through each city at most once.</p></div><div class="input-specification"><p>The first line of input contains a single integer $t$ ($1\le t\le 200$) — the number of test cases. The description of test cases follows.</p><p>The only line of each test case contains two integers $n$ and $m$ ($1\leq n\leq 10^{18}$, $1\leq m\leq 10^5$) — the number of the cities and the maximum value of a city.</p><p>It is guaranteed that the sum of $m$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case output one integer — the sum of scores of all possible travel plans, modulo $998\,244\,353$.</p></div>

## Input

<p>The first line of input contains a single integer $t$ ($1\le t\le 200$) — the number of test cases. The description of test cases follows.</p><p>The only line of each test case contains two integers $n$ and $m$ ($1\leq n\leq 10^{18}$, $1\leq m\leq 10^5$) — the number of the cities and the maximum value of a city.</p><p>It is guaranteed that the sum of $m$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case output one integer — the sum of scores of all possible travel plans, modulo $998\,244\,353$.</p>





```input1|2,4,6
5
3 1
2 2
10 9
43 20
154 147
```




```output1
6
19
583217643
68816635
714002110
```



## Note

<p>In the first test case, there is only one possible travel plan:</p><center> <img class="tex-graphics" src="file://BFH4ukWt.png" style="max-width: 100.0%;max-height: 100.0%;" width="227px"> </center><p>Path $1\rightarrow 1$: $s_{1,1}=a_1=1$.</p><p>Path $1\rightarrow 2$: $s_{1,2}=\max(1,1)=1$.</p><p>Path $1\rightarrow 3$: $s_{1,3}=\max(1,1)=1$.</p><p>Path $2\rightarrow 2$: $s_{2,2}=a_2=1$.</p><p>Path $2\rightarrow 1\rightarrow 3$: $s_{2,3}=\max(1,1,1)=1$.</p><p>Path $3\rightarrow 3$: $s_{3,3}=a_3=1$.</p><p>The score is $1+1+1+1+1+1=6$.</p><p>In the second test case, there are four possible travel plans:</p><center> <img class="tex-graphics" src="file://GqBRSfXm.png" style="max-width: 100.0%;max-height: 100.0%;" width="529px"> </center><p>Score of plan $1$: $1+1+1=3$.</p><p>Score of plan $2$: $1+2+2=5$.</p><p>Score of plan $3$: $2+2+1=5$.</p><p>Score of plan $4$: $2+2+2=6$.</p><p>Therefore, the sum of score is $3+5+5+6=19$.</p>
