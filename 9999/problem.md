## Description

<div><p>The Chaya tribe believes that there are $n$ signs of the apocalypse. Over time, it has been found out that the $i$-th sign occurs every $a_i$ years (in years $a_i$, $2 \cdot a_i$, $3 \cdot a_i$, $\dots$).</p><p>According to the legends, for the apocalypse to happen, the signs must occur sequentially. That is, first they wait for the first sign to occur, then strictly after it, the second sign will occur, and so on. That is, if the $i$-th sign occurred in the year $x$, the tribe starts waiting for the occurrence of the $(i+1)$-th sign, starting from the year $x+1$.</p><p>In which year will the $n$-th sign occur and the apocalypse will happen?</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases. Then follow the descriptions of the test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 100$)&nbsp;— the number of signs.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, a_3, \dots, a_n$ ($1 \le a_i \le 10^6$)&nbsp;— the periodicities of the signs.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the year in which all $n$ signs will occur.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases. Then follow the descriptions of the test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 100$)&nbsp;— the number of signs.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, a_3, \dots, a_n$ ($1 \le a_i \le 10^6$)&nbsp;— the periodicities of the signs.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the year in which all $n$ signs will occur.</p>





```input1|2,3,6,7
4
6
3 2 4 5 9 18
5
1 2 3 4 5
5
1 1 1 1 1
6
50 30 711 200 503 1006
```




```output1
36
5
5
2012
```



## Note

<p>In the first set of input data of the example:</p><ul> <li> The tribe will wait for the first sign in the $3$-rd year; </li><li> the tribe will wait for the second sign in the $4$-th year (since year $2$ have already passed); </li><li> the tribe will wait for the third sign in the $8$-th year (since the second sign has already occurred in the $4$-th year); </li><li> the tribe will wait for the fourth sign in the $10$-th year (since year $5$ have already passed); </li><li> the tribe will wait for the fifth sign in the $18$-th year (since year $9$ have already passed); </li><li> the tribe will wait for the sixth sign in the $36$-th year (since the fifth sign has already occurred in the $18$-th year). </li></ul>
