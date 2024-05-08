## Description

<div><p>There is a fun game where you need to feed cats that come and go. The level of the game consists of $n$ steps. There are $m$ cats; the cat $i$ is present in steps from $l_i$ to $r_i$, inclusive. In each step, you can feed all the cats that are currently present or do nothing. </p><p>If you feed the same cat more than once, it will overeat, and you will immediately lose the game. Your goal is to feed as many cats as possible without causing any cat to overeat. </p><p>Find the maximum number of cats you can feed.</p><p>Formally, you need to select several integer points from the segment from $1$ to $n$ in such a way that among given segments, none covers two or more of the selected points, and as many segments as possible cover one of the selected points.</p></div><div class="input-specification"><p>The first line of input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then the descriptions of the test cases follow.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \le n \le 10^6$, $1 \le m\le 2\cdot 10^5$). </p><p>The $i$-th of the next $m$ lines contains a pair of integers $l_i$ and $r_i$ ($1 \le l_i \le r_i \le n$).</p><p>The sum of $n$ for all tests does not exceed $10^6$, the sum of $m$ for all tests does not exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print a single integer, the maximum number of cats you can feed.</p></div>

## Input

<p>The first line of input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then the descriptions of the test cases follow.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \le n \le 10^6$, $1 \le m\le 2\cdot 10^5$). </p><p>The $i$-th of the next $m$ lines contains a pair of integers $l_i$ and $r_i$ ($1 \le l_i \le r_i \le n$).</p><p>The sum of $n$ for all tests does not exceed $10^6$, the sum of $m$ for all tests does not exceed $2\cdot 10^5$.</p>

## Output

<p>For each test case, print a single integer, the maximum number of cats you can feed.</p>





```input1|2,3,4,5,6,7,8,11,12,13,14,15,16,17,18,19,20,21
3
15 6
2 10
3 5
2 4
7 7
8 12
11 11
1000 1
1 1000
5 10
1 2
3 4
3 4
3 4
3 4
1 1
1 2
3 3
3 4
3 4
```




```output1
5
1
10
```



## Note

<p>In the first example, one of the ways to feed five cats is to feed at steps $4$ and $11$.</p><ul><li> At step $4$, cats $1$, $2$, and $3$ will be fed.</li><li> At step $11$, cats $5$ and $6$ will be fed.</li></ul>
