## Description

<div><p>An <span class="tex-font-style-it">Italian data center</span> consists of a set of servers, each colored green, white, or red, and a set of wires connecting them. Each wire connects two distinct servers and two servers are connected by at most one wire. Additionally, the data center is connected, i.e. there is a way to transmit information between any two servers through a sequence of wires.</p><p>To judge all of the contestant submissions, SWERC has an Italian data center. Since every year the number of contestants doubles, the data center needs to grow to adapt to the extra load. To address this, SWERC builds a new data center based on the previous year's one by following these steps:</p><ul> <li> For each server $s$ in the old data center, the new data center contains two servers $s_1$ and $s_2$ of the same color as $s$. A wire is placed connecting the two servers $s_1$ and $s_2$. </li><li> For each wire connecting servers $s$ and $t$ in the old data center: if $s$ and $t$ have the same color, then a wire is placed in the new data center connecting $s_1$ and $t_1$ and another wire connecting $s_2$ and $t_2$; otherwise, a wire is placed in the new data center connecting $s_1$ and $t_2$ and another one connecting $s_2$ and $t_1$. </li></ul><p>One can show that if the old data center is connected than the new data center is also connected.</p><p>You are given the Italian data center that SWERC currently has, which contains $n$ servers (indexed by $1, \, 2, \, \dots, \, n$) and $m$ wires connecting them. The organization wants to know how good their data center will be after $k$ years, so you should determine the <span class="tex-font-style-it">diameter</span> of the data center SWERC will have in $k$ years. The diameter of the data center is the largest distance between any two servers, i.e. the shortest number of wires that have to be used to transmit something between the two servers.</p></div><div class="input-specification"><p>The first line contains three integers $n$, $m$ and $k$ ($2 \leq n \leq 100$, $n - 1 \leq m \leq n (n - 1) / 2$, $0 \leq k \leq 100$) — the number of servers, the number of wires, and the number of years to consider.</p><p>The second line contains $n$ integers $c_1, \, c_2, \, \dots, \, c_n$ ($1 \leq c_i \leq 3$) — $c_i$ is the color of server $i$ (where $1$ stands for <span class="tex-font-style-it">green</span>, $2$ for <span class="tex-font-style-it">white</span> and $3$ for <span class="tex-font-style-it">red</span>).</p><p>Each of the next $m$ lines contains two integers $s_i$ and $t_i$ ($1 \leq s_i, t_i \leq n$) — the two servers the $i$-th wire connects.</p><p>It is guaranteed that the data center is connected, the endpoints of each wire are distinct, and that there are no repeated wires.</p></div><div class="output-specification"><p>Print the diameter of SWERC's data center after $k$ years.</p></div>

## Input

<p>The first line contains three integers $n$, $m$ and $k$ ($2 \leq n \leq 100$, $n - 1 \leq m \leq n (n - 1) / 2$, $0 \leq k \leq 100$) — the number of servers, the number of wires, and the number of years to consider.</p><p>The second line contains $n$ integers $c_1, \, c_2, \, \dots, \, c_n$ ($1 \leq c_i \leq 3$) — $c_i$ is the color of server $i$ (where $1$ stands for <span class="tex-font-style-it">green</span>, $2$ for <span class="tex-font-style-it">white</span> and $3$ for <span class="tex-font-style-it">red</span>).</p><p>Each of the next $m$ lines contains two integers $s_i$ and $t_i$ ($1 \leq s_i, t_i \leq n$) — the two servers the $i$-th wire connects.</p><p>It is guaranteed that the data center is connected, the endpoints of each wire are distinct, and that there are no repeated wires.</p>

## Output

<p>Print the diameter of SWERC's data center after $k$ years.</p>





```input1
3 3 0
1 2 3
1 2
2 3
3 1
```




```input2
3 3 1
1 2 3
1 2
2 3
3 1
```




```input3
3 3 2
1 2 1
1 2
2 3
3 1
```




```input4
8 14 100
3 3 2 2 1 2 2 1
2 7
1 5
7 8
4 6
2 8
1 8
2 6
6 7
1 6
1 4
3 5
1 3
4 5
5 7
```




```output1
1
```




```output2
2
```




```output3
3
```




```output4
53
```



## Note

<p>In the <span class="tex-font-style-bf">first sample</span>, the Italian data center is the following:</p><center> <img class="tex-graphics" src="file://QbJbgKAv.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>The distance between any pair of servers is $1$ so the diameter is $1$.</p><p>In the <span class="tex-font-style-bf">second sample</span>, the initial Italian data center is the one from the first sample.</p><p>After one year we obtain the following (where the numbers indicate which copy the server refers to):</p><center> <img class="tex-graphics" src="file://2Arr8KFS.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>Consider the highlighted servers. The distance between them is $2$ and there is no pair of servers with greater distance, so the diameter is $2$.</p><p>In the <span class="tex-font-style-bf">third sample</span>, the data center after one year is the following:</p><center> <img class="tex-graphics" src="file://SDTUP7i3.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>After one more year:</p><center> <img class="tex-graphics" src="file://WpVSdWON.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>Consider the highlighted servers. The distance between them is $3$ and there is no pair of servers with greater distance, so the diameter is $3$.</p>
