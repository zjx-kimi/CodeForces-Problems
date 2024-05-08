## Description

<div><p>Monsters have invaded the town again! Asuka invites her good friend, Jellyfish, to drive EVA with her.</p><p>There are $n$ cities in the town. All the monsters are in city $n$. Jellyfish and Asuka are currently in city $1$ and need to move to city $n$ to defeat the monsters.</p><p>There are $m$ roads. The $i$-th road allows one to travel from city $a_i$ to city $b_i$. All the roads are <span class="tex-font-style-bf">directed</span>. That is, one cannot travel from city $b_i$ to $a_i$ using the $i$-th road. Interestingly, all roads satisfy $a_i&lt;b_i$.</p><p>Driving EVA requires two people to work together. However, Asuka and Jellyfish have not done any training together before.</p><p>Suppose that EVA is currently in city $u$. Jellyfish and Asuka will both choose an undestroyed road that starts at city $u$. Suppose Jellyfish and Asuka choose roads that end at cities $v_1$ and $v_2$ respectively. If $v_1 = v_2$, EVA moves to city $v_1$ successfully. Otherwise, EVA stays in city $u$ and both roads that they have chosen will be destroyed.</p><p>It is possible that EVA is currently in city $u$ ($u \neq n$) and there are no undestroyed roads that start at city $u$. In that case, the mission will be a failure. Otherwise, if they reach city $n$ in the end, the mission is considered a success.</p><p>Every time they choose the roads, Jellyfish knows that Asuka will choose a road randomly. Now, Jellyfish wants to know, if she chooses the roads optimally, what is the maximum probability of the mission being successful.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 2000$). The description of the test cases follows.</p><p>The first line of each test case contains two integers, $n$ and $m$ ($2 \leq n \leq 5000$, $0 \leq m \leq \min(\frac{n(n-1)}{2}, 2 \cdot 10^5)$)&nbsp;— the number of the cities and the number of the roads.</p><p>In the following $m$ lines of each test case, each line contains two integers $a$ and $b$ ($1 \leq a &lt; b \leq n$)&nbsp;— representing a road from city $a$ to city $b$.</p><p>It is guaranteed that for each test case, each road appears at most once.</p><p>It is guaranteed that the sum of $n$ over all test cases will not exceed $5000$ and that the sum of $m$ over all test cases will not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>Output the maximum probability of the mission being successful if Jellyfish chooses the roads optimally.</p><p>Your answer will be accepted if the absolute or relative error does not exceed $10^{-9}$. Formally, let your answer be $a$, and the jury's answer be $b$. Your answer is considered correct if $\frac{|a-b|}{\max(1,|b|)} \leq 10^{-9}$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 2000$). The description of the test cases follows.</p><p>The first line of each test case contains two integers, $n$ and $m$ ($2 \leq n \leq 5000$, $0 \leq m \leq \min(\frac{n(n-1)}{2}, 2 \cdot 10^5)$)&nbsp;— the number of the cities and the number of the roads.</p><p>In the following $m$ lines of each test case, each line contains two integers $a$ and $b$ ($1 \leq a &lt; b \leq n$)&nbsp;— representing a road from city $a$ to city $b$.</p><p>It is guaranteed that for each test case, each road appears at most once.</p><p>It is guaranteed that the sum of $n$ over all test cases will not exceed $5000$ and that the sum of $m$ over all test cases will not exceed $2 \cdot 10^5$.</p>

## Output

<p>Output the maximum probability of the mission being successful if Jellyfish chooses the roads optimally.</p><p>Your answer will be accepted if the absolute or relative error does not exceed $10^{-9}$. Formally, let your answer be $a$, and the jury's answer be $b$. Your answer is considered correct if $\frac{|a-b|}{\max(1,|b|)} \leq 10^{-9}$.</p>





```input1|2,3,4,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34
3
3 2
1 2
1 3
7 8
1 2
1 3
1 4
1 5
2 6
3 6
4 6
6 7
10 20
1 2
1 3
1 4
1 5
1 6
2 6
2 7
2 8
2 9
3 4
3 7
3 8
3 10
4 6
4 8
4 10
6 10
7 8
7 9
7 10
```




```output1
0.500000000000
0.625000000000
0.491666666667
```



## Note

<p>In the first test case, Jellyfish will choose $v_1=3$, and Asuka will choose $v_2=2$ with a possibility of $0.5$ and $v_2=3$ with a possibility of $0.5$. The mission is considered a success with a possibility of $0.5$.</p>
