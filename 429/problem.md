## Description

<div><p>There are $n$ benches near the Main Walkway in Summer Infomatics School. These benches are numbered by integers from $1$ to $n$ in order they follow. Also there are $m$ cookie sellers near the Walkway. The $i$-th ($1 \le i \le m$) cookie sellers is located near the $s_i$-th bench.</p><p>Petya is standing in the beginning of the Walkway. He will pass near all benches starting from the $1$-st bench and ending with the $n$-th bench. Petya passes the distance between two consecutive benches in $1$ minute. He has a knapsack with an infinite amount of cookies. Petya is going to eat cookies from his knapsack and buy them from cookie sellers during the walk.</p><p>Petya eats cookies only near the benches according to the following rule: he will eat the cookie near the $i$-th ($1 \le i \le n$) bench if and only if <span class="tex-font-style-bf">at least one</span> of the following conditions holds:</p><ul> <li> There is a cookie seller near the $i$-th bench. Then Petya will buy a cookie from cookie seller and eat it immediately. </li><li> Petya has not yet eaten a cookie. Then Petya will take a cookie from his knapsack and eat it immediately. </li><li> At least $d$ minutes passed since Petya ate the previous cookie. In other words, Petya has not eaten a cookie near the benches $i-1, i-2, \ldots, \max(i-d+1, 1)$. Then Petya will take a cookie from his knapsack and eat it immediately. </li></ul><p>You may assume that Petya eats cookies instantly. Petya will not eat two or more cookies near the same bench.</p><p>You want to <span class="tex-font-style-bf">minimize</span> the number of cookies Petya will eat during his walk. In order to do this, you will ask the administration of the Summer Informatics School to remove <span class="tex-font-style-bf">exactly one</span> cookie seller from the Walkway before Petya starts his walk.</p><p>Please determine the minimum possible number of cookies Petya can eat after removing exactly one cookie seller. Also determine the number of cookie sellers, such that if you remove one of them, Petya will eat the minimum possible number of cookies.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^3$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains three integers $n$, $m$ and $d$ ($2 \le d \le n \le 10^9$, $2 \le m \le \min(10^{5}, n)$)&nbsp;— the number of benches, the number of cookie sellers and the value of parameter $d$ from the statement, respectively.</p><p>The second line of each test case contains $m$ integers $s_1, s_2, \ldots, s_m$ ($1 \le s_i \le n$)&nbsp;— the locations of the cookie sellers. It is guaranteed that $s_{i} &lt; s_{i+1}$ for all $1 \leq i \leq m - 1$.</p><p>It is guaranteed that the sum of $m$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case print two integers&nbsp;— the minimum number of cookies that Petya can eat if exactly one cookie seller is removed, and the number of cookie sellers such that if one of them is removed, Petya will eat the minimum possible number of cookies.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^3$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains three integers $n$, $m$ and $d$ ($2 \le d \le n \le 10^9$, $2 \le m \le \min(10^{5}, n)$)&nbsp;— the number of benches, the number of cookie sellers and the value of parameter $d$ from the statement, respectively.</p><p>The second line of each test case contains $m$ integers $s_1, s_2, \ldots, s_m$ ($1 \le s_i \le n$)&nbsp;— the locations of the cookie sellers. It is guaranteed that $s_{i} &lt; s_{i+1}$ for all $1 \leq i \leq m - 1$.</p><p>It is guaranteed that the sum of $m$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case print two integers&nbsp;— the minimum number of cookies that Petya can eat if exactly one cookie seller is removed, and the number of cookie sellers such that if one of them is removed, Petya will eat the minimum possible number of cookies.</p>





```input1|2,3,6,7,10,11,14,15
8
6 2 2
2 5
8 3 2
3 5 8
10 4 9
2 8 9 10
30 5 8
6 8 15 24 29
30 5 8
6 8 12 20 27
8 8 3
1 2 3 4 5 6 7 8
2 2 2
1 2
1000000000 3 20000000
57008429 66778899 837653445
```




```output1
3 1
4 1
4 4
6 4
5 2
7 7
1 1
51 1
```



## Note

<p>In the first test case $n=6$, $m=2$, $d=2$ and $s=[2, 5]$. If no cookie seller is removed, then Petya will eat $4$ cookies during his walk (note that you have to remove exactly one cookie seller; this case is explained only to show how Petya decides whether to eat a cookie): </p><ul> <li> Petya will eat a cookie near the $1$-st bench since he has not yet eaten a cookie. </li><li> Petya will eat a cookie near the $2$-nd bench since there is a cookie seller near this bench. </li><li> Petya will not eat a cookie near the $3$-rd bench since only $1&lt;d$ minute passed since he ate a cookie. </li><li> Petya will eat a cookie near the $4$-th bench since $2\ge d$ minutes passed since he ate a cookie. </li><li> Petya will eat a cookie near the $5$-th bench since there is a cookie seller near this bench. </li><li> Petya will not eat a cookie near the $6$-th bench since only $1&lt;d$ minute passed since he ate a cookie. </li></ul><p>If the $1$-st cookie seller is removed, Petya will eat $3$ cookies (near the benches $1$, $3$ and $5$). If the $2$-nd cookie seller is removed, Petya will eat $4$ cookies (near the benches $1$, $2$, $4$ and $6$).</p><p>Thus, the minimum number of cookies Petya will eat is $3$; there is only one cookie seller such that removing it results in minimizing the number of cookies Petya will eat.</p><p>In the second test case </p><ul> <li> the removal of the $1$-st or the $2$-nd cookie seller results in Petya eating $5$ cookies near the benches $1$, $3$, $5$, $7$, $8$; </li><li> the removal of the $3$-rd cookie seller results in Petya eating $4$ cookies near the benches $1$, $3$, $5$, $7$. </li></ul><p>Note that the second integer you should output is the <span class="tex-font-style-bf">number of (that is, amount)</span> cookie sellers, not the index of a cookie seller to remove. Thus, the answer to the second test case is <span class="tex-font-style-tt">4 1</span> because there is only <span class="tex-font-style-bf">one</span> cookie seller such that removing it results in Petya eating four cookies, which is the minimum possible.</p><p>In the third test case Petya will eat $4$ cookies no matter what cookie seller is removed.</p><p>Note that Petya is not interested in minimizing the number of cookies he will eat, so he eats cookies whenever it is possible under the rule from the statement.</p>
