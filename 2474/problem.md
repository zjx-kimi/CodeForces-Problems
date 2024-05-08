## Description

<div><p>Recently, cryptocurrencies have become increasingly popular. Ann decided that it was about time she started mining the Dogecoin cryptocurrency. Ann's computer is not very powerful, so Ann mines exactly $1$ Dogecoin per day. On the Internet, there are forecasts of the cost of $1$ dogecoin for the next $n$ days. Every day, Ann can sell any amount of dogecoin that she currently has. Note that if Ann mined Dogecoin on the $i$-th day, then she can sell it on the same day.</p><p>Ann has not yet decided when to start mining. She has prepared $q$ possible plans and for each of them wants to know the maximum profit that she can get. Each of the plans is described by two numbers $l$ and $r$ — the first and last days of mining. Note that Ann should not have any Dogecoin left after the $r$-th day.</p></div><div class="input-specification"><p>The first line contains one integer $n$ ($1 \le n \le 2 \cdot 10^5$).</p><p>The second line contains $n$ integers $c_1, c_2, \dots, c_n$ ($1 \le c_i \le 10^6$), where $c_i$ is the cost of Dogecoin on the $i$-th day.</p><p>The third line contains one integer $q$ ($1 \le q \le 2 \cdot 10^5$) — the number of Ann's plans.</p><p>The following $q$ lines contains two integers $l$ and $r$ ($1 \le l \le r \le n$) — the first and last days of mining. </p></div><div class="output-specification"><p>For each Ann's plan print one integer — the maximum profit that she can get using this plan.</p></div>

## Input

<p>The first line contains one integer $n$ ($1 \le n \le 2 \cdot 10^5$).</p><p>The second line contains $n$ integers $c_1, c_2, \dots, c_n$ ($1 \le c_i \le 10^6$), where $c_i$ is the cost of Dogecoin on the $i$-th day.</p><p>The third line contains one integer $q$ ($1 \le q \le 2 \cdot 10^5$) — the number of Ann's plans.</p><p>The following $q$ lines contains two integers $l$ and $r$ ($1 \le l \le r \le n$) — the first and last days of mining. </p>

## Output

<p>For each Ann's plan print one integer — the maximum profit that she can get using this plan.</p>





```input1
5
4 1 2 3 2
4
1 5
2 4
3 5
5 5
```




```output1
15 9 8 2
```


