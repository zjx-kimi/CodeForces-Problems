## Description

<div><p>There are $n$ cities in Berland, and they are connected by two railroads — the Main railroad and the Auxiliary railroad. Each city has two railway stations, one connected to the Main railroad (called the Main station), and the other connected to the Auxiliary railroad.</p><p>The railroads are identical in their structure. The Main railroad consists of $n-1$ railroad segments; the $i$-th railroad segment connects the Main station of the city $i$ with the Main station of the city $i+1$. Similarly, the Auxiliary railroad consists of $n-1$ railroad segments; the $i$-th railroad segment connects the Auxiliary station of the city $i$ with the Auxiliary station of the city $i+1$.</p><p>These railroads are used to transfer different goods and resources from one city to another. In particular, the Ministry of Energetics is interested in using these railroads to transfer coal.</p><p>The Ministry has estimated the following capabilities of the railroads:</p><ul> <li> for every $i \in [1, n-1]$, at most $a_i$ tons of coal per day can be transferred from the Main station $i$ to the Main station $i+1$ <span class="tex-font-style-bf">(only in this direction)</span>; </li><li> for every $i \in [1, n-1]$, at most $b_i$ tons of coal per day can be transferred from the Auxiliary station $i$ to the Auxiliary station $i+1$ <span class="tex-font-style-bf">(only in this direction)</span>; </li><li> for every $i \in [1, n]$, at most $c_i$ tons of coal per day can be transferred from the Main station $i$ to the Auxiliary station $i$, <span class="tex-font-style-bf">or in the opposite direction</span>. </li></ul><p>To analyze the capacity of the whole railroad network, the Ministry requires a software that would process and answer queries of the following format:</p><ul> <li> calculate the maximum number of tons of coal that can be transferred per day from the Main station $l_i$ to the Main station $r_i$. </li></ul><p>Your task is to implement this software.</p></div><div class="input-specification"><p>The first line contains one integer $n$ ($2 \le n \le 3 \cdot 10^5$) — the number of cities.</p><p>The second line contains $n-1$ integers $a_1, a_2, \dots, a_{n-1}$ ($1 \le a_i \le 10^9$).</p><p>The third line contains $n-1$ integers $b_1, b_2, \dots, b_{n-1}$ ($1 \le b_i \le 10^9$).</p><p>The fourth line contains $n$ integers $c_1, c_2, \dots, c_{n}$ ($1 \le c_i \le 10^9$).</p><p>The fifth line contains one integer $q$ ($1 \le q \le 3 \cdot 10^5$) — the number of queries.</p><p>Then $q$ lines follow, the $i$-th line contains two integers $l_i$ and $r_i$ ($1 \le l_i &lt; r_i \le n$) — the parameters of the $i$-th query.</p></div><div class="output-specification"><p>Print $q$ integers, where the $i$-th integer should be the answer to the $i$-th query, i. e. the maximum number of tons of coal that can be transferred per day from the Main station $l_i$ to the Main station $r_i$.</p></div>

## Input

<p>The first line contains one integer $n$ ($2 \le n \le 3 \cdot 10^5$) — the number of cities.</p><p>The second line contains $n-1$ integers $a_1, a_2, \dots, a_{n-1}$ ($1 \le a_i \le 10^9$).</p><p>The third line contains $n-1$ integers $b_1, b_2, \dots, b_{n-1}$ ($1 \le b_i \le 10^9$).</p><p>The fourth line contains $n$ integers $c_1, c_2, \dots, c_{n}$ ($1 \le c_i \le 10^9$).</p><p>The fifth line contains one integer $q$ ($1 \le q \le 3 \cdot 10^5$) — the number of queries.</p><p>Then $q$ lines follow, the $i$-th line contains two integers $l_i$ and $r_i$ ($1 \le l_i &lt; r_i \le n$) — the parameters of the $i$-th query.</p>

## Output

<p>Print $q$ integers, where the $i$-th integer should be the answer to the $i$-th query, i. e. the maximum number of tons of coal that can be transferred per day from the Main station $l_i$ to the Main station $r_i$.</p>





```input1
5
3 4 7 4
8 5 3 5
10 5 3 4 10
4
1 4
1 2
3 4
2 4
```




```output1
9 8 10 9
```


