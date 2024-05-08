## Description

<div><p>In the Land of Fire there are $n$ villages and $n-1$ bidirectional road, and there is a path between any pair of villages by roads. There are only two types of roads: stone ones and sand ones. Since the Land of Fire is constantly renovating, every morning workers choose a single road and flip its type (so it becomes a stone road if it was a sand road and vice versa). Also everyone here loves ramen, that's why every morning a ramen pavilion is set in the middle of every <span class="tex-font-style-bf">stone</span> road, and at the end of each day all the pavilions are removed.</p><p>For each of the following $m$ days, after another road is flipped, Naruto and Jiraiya choose a simple path — that is, a route which starts in a village and ends in a (possibly, the same) village, and doesn't contain any road twice. Since Naruto and Jiraiya also love ramen very much, they buy a single cup of ramen on each stone road and one of them eats it. Since they don't want to offend each other, they only choose routes where they can eat equal number of ramen cups. Since they both like traveling, they choose any longest possible path. After every renovation find the maximal possible length of a path (that is, the number of roads in it) they can follow.</p></div><div class="input-specification"><p>The first line contains the only positive integer $n$ ($2 \leq n \leq 500\,000$) standing for the number of villages in the Land of Fire.</p><p>Each of the following $(n-1)$ lines contains a description of another road, represented as three positive integers $u$, $v$ and $t$ ($1 \leq u, v \leq n$, $t \in \{0,1\}$). The first two numbers denote the villages connected by the road, and the third denotes the initial type of the road: $0$ for the sand one and $1$ for the stone one. Roads are numbered from $1$ to $(n-1)$ in the order from the input.</p><p>The following line contains a positive integer $m$ ($1 \leq m \leq 500\,000$) standing for the number of days Naruto and Jiraiya travel for.</p><p>Each of the following $m$ lines contains the single integer $id$ ($1 \leq id \leq n-1$) standing for the index of the road whose type is flipped on the morning of corresponding day.</p><p>It is guaranteed that there is a road path between any pair of villages.</p></div><div class="output-specification"><p>Output $m$ lines. In the $i$-th of them print the only integer denoting the maximal possible length of any valid path on the $i$-th day.</p></div>

## Input

<p>The first line contains the only positive integer $n$ ($2 \leq n \leq 500\,000$) standing for the number of villages in the Land of Fire.</p><p>Each of the following $(n-1)$ lines contains a description of another road, represented as three positive integers $u$, $v$ and $t$ ($1 \leq u, v \leq n$, $t \in \{0,1\}$). The first two numbers denote the villages connected by the road, and the third denotes the initial type of the road: $0$ for the sand one and $1$ for the stone one. Roads are numbered from $1$ to $(n-1)$ in the order from the input.</p><p>The following line contains a positive integer $m$ ($1 \leq m \leq 500\,000$) standing for the number of days Naruto and Jiraiya travel for.</p><p>Each of the following $m$ lines contains the single integer $id$ ($1 \leq id \leq n-1$) standing for the index of the road whose type is flipped on the morning of corresponding day.</p><p>It is guaranteed that there is a road path between any pair of villages.</p>

## Output

<p>Output $m$ lines. In the $i$-th of them print the only integer denoting the maximal possible length of any valid path on the $i$-th day.</p>





```input1
5
1 2 0
1 3 0
3 5 0
3 4 0
5
3
4
1
3
4
```




```output1
3
2
3
3
2
```



## Note

<p>After the renovation of the $3$-rd road the longest path consists of the roads $1$, $2$ and $4$.</p><p>After the renovation of the $4$-th road one of the longest paths consists of the roads $1$ and $2$.</p><p>After the renovation of the $1$-st road one of the longest paths consists of the roads $1$, $2$ and $3$.</p><p>After the renovation of the $3$-rd road the longest path consists of the roads $1$, $2$ and $4$.</p><p>After the renovation of the $4$-rd road one of the longest paths consists of the roads $2$ and $4$.</p>
