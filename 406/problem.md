## Description

<div><p>Recently, Kolya found out that a new movie theatre is going to be opened in his city soon, which will show a new movie every day for $n$ days. So, on the day with the number $1 \le i \le n$, the movie theatre will show the premiere of the $i$-th movie. Also, Kolya found out the schedule of the movies and assigned the entertainment value to each movie, denoted by $a_i$.</p><p>However, the longer Kolya stays without visiting a movie theatre, the larger the decrease in entertainment value of the next movie. That decrease is equivalent to $d \cdot cnt$, where $d$ is a predetermined value and $cnt$ is the number of days since the last visit to the movie theatre. It is also known that Kolya managed to visit another movie theatre a day before the new one opened&nbsp;— the day with the number $0$. <span class="tex-font-style-bf">So if we visit the movie theatre the first time on the day with the number $i$, then $cnt$&nbsp;— the number of days since the last visit to the movie theatre will be equal to $i$</span>.</p><p>For example, if $d = 2$ and $a = [3, 2, 5, 4, 6]$, then by visiting movies with indices $1$ and $3$, $cnt$ value for the day $1$ will be equal to $1 - 0 = 1$ and $cnt$ value for the day $3$ will be $3 - 1 = 2$, so the total entertainment value of the movies will be $a_1 - d \cdot 1 + a_3 - d \cdot 2 = 3 - 2 \cdot 1 + 5 - 2 \cdot 2 = 2$.</p><p>Unfortunately, Kolya only has time to visit <span class="tex-font-style-bf">at most $m$ movies</span>. Help him create a plan to visit the cinema in such a way that the total entertainment value of all the movies he visits is maximized.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains three integers $n$, $m$, and $d$ ($1 \le n \le 2 \cdot 10^5$, $1 \le m \le n$, $1 \le d \le 10^9$).</p><p>The second line of each set of input data contains $n$ integers $a_1, a_2, \ldots, a_n$ ($-10^9 \le a_i \le 10^9$)&nbsp;— the entertainment values of the movies.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the maximum total entertainment value that Kolya can get.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains three integers $n$, $m$, and $d$ ($1 \le n \le 2 \cdot 10^5$, $1 \le m \le n$, $1 \le d \le 10^9$).</p><p>The second line of each set of input data contains $n$ integers $a_1, a_2, \ldots, a_n$ ($-10^9 \le a_i \le 10^9$)&nbsp;— the entertainment values of the movies.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the maximum total entertainment value that Kolya can get.</p>





```input1|2,3,6,7,10,11
6
5 2 2
3 2 5 4 6
4 3 2
1 1 1 1
6 6 6
-82 45 1 -77 39 11
5 2 2
3 2 5 4 8
2 1 1
-1 2
6 3 2
-8 8 -2 -1 9 0
```




```output1
2
0
60
3
0
7
```



## Note

<p>The first test case is explained in the problem statement.</p><p>In the second test case, it is optimal not to visit any movies.</p><p>In the third test case, it is optimal to visit movies with numbers $2$, $3$, $5$, $6$, so the total entertainment value of the visited movies will be $45 - 6 \cdot 2 + 1 - 6 \cdot 1 + 39 - 6 \cdot 2 + 11 - 6 \cdot 1 = 60$.</p>
