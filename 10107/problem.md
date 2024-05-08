## Description

<div><p>Finally, lunchtime!</p><p>$n$ schoolchildren have lined up in a long queue at the cook's tent for porridge. The cook will be serving porridge for $D$ minutes. The schoolchild standing in the $i$-th position in the queue has a priority of $k_i$ and eats one portion of porridge in $s_i$ minutes.</p><p><span class="tex-font-style-bf">At the beginning</span> of each minute of the break, the cook serves the first schoolchild in the queue one portion of porridge, after which the schoolchild goes to eat their portion. If the $i$-th schoolchild is served a portion at the beginning of the $x$-th minute, then they will return to the queue <span class="tex-font-style-bf">at the end</span> of the $(x + s_i)$-th minute.</p><p>When the $i$-th schoolchild returns to the queue, the schoolchildren at the end of the queue whose priority is <span class="tex-font-style-bf">strictly lower</span> than that of the $i$-th schoolchild must let them pass. Thus, they will stand in the queue behind the last schoolchild whose priority is <span class="tex-font-style-bf">not lower</span> than their own. That is, behind the last schoolchild $j$ with $k_j \ge k_i$. If there is no such schoolchild in the queue, the $i$-th schoolchild will stand at the front of the queue.</p><p>If several schoolchildren return at the same time, they will return to the queue in ascending order of their $s_i$.</p><p>For example, if $n = 3$, $D = 3$, $k = [2, 3, 2]$, and $s = [2, 1, 3]$, the serving will occur as follows:</p><ul> <li> At the beginning of minute $1$, the students in the queue are $[1, 2, 3]$, and student $1$ is served porridge; </li><li> at the beginning of minute $2$, the students in the queue are $[2, 3]$, and student $2$ is served porridge; </li><li> at the beginning of minute $3$, the student in the queue is $[3]$, and student $3$ is served porridge; </li><li> at the end of minute $3$, student $2$ returns to the queue, and the queue becomes $[2]$; </li><li> at the end of minute $3$, student $1$ returns to the queue, and the queue becomes $[2, 1]$, as his priority is lower. </li></ul><p>Determine the minimum number of minutes after the start of the break that each schoolchild will receive porridge at least once, or report that this will not happen within $D$ minutes.</p></div><div class="input-specification"><p>Each test consists of several test cases. The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases. This is followed by a description of the test cases.</p><p>The first line of each test case contains two integers $n$ and $D$ ($1 \le n \le 2 \cdot 10^5$, $1 \le D \le 3\cdot 10^5$)&nbsp;— the number of schoolchildren in the queue and the break time, respectively.</p><p>The next $n$ lines contain two integers $k_i$ and $s_i$ ($1 \le k_i, s_i, \le 10^9$)&nbsp;— the priority and the time to eat one portion of porridge for the respective schoolchild. The schoolchildren are given in the order they stand in the queue (from the front to the end).</p><p>It is guaranteed that the sum of the values of $n$ for all input data sets does not exceed $2\cdot 10^5$. Similarly, it is guaranteed that the sum of the values of $D$ for all input data sets does not exceed $3\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output the minimum number of minutes after which each schoolchild will receive porridge at least once. If this does not happen within the break time, output $-1$.</p></div>

## Input

<p>Each test consists of several test cases. The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases. This is followed by a description of the test cases.</p><p>The first line of each test case contains two integers $n$ and $D$ ($1 \le n \le 2 \cdot 10^5$, $1 \le D \le 3\cdot 10^5$)&nbsp;— the number of schoolchildren in the queue and the break time, respectively.</p><p>The next $n$ lines contain two integers $k_i$ and $s_i$ ($1 \le k_i, s_i, \le 10^9$)&nbsp;— the priority and the time to eat one portion of porridge for the respective schoolchild. The schoolchildren are given in the order they stand in the queue (from the front to the end).</p><p>It is guaranteed that the sum of the values of $n$ for all input data sets does not exceed $2\cdot 10^5$. Similarly, it is guaranteed that the sum of the values of $D$ for all input data sets does not exceed $3\cdot 10^5$.</p>

## Output

<p>For each test case, output the minimum number of minutes after which each schoolchild will receive porridge at least once. If this does not happen within the break time, output $-1$.</p>





```input1|2,3,4,5,12,13,14,15,16,17,24,25,26,27,28,29,32,33,34,35,36,37
7
3 3
2 2
3 1
2 3
5 10
10 3
7 1
11 3
5 1
6 1
5 20
4 2
7 2
8 5
1 5
3 1
5 17
1 3
8 2
8 3
2 2
1 1
5 14
8 2
4 2
1 3
8 3
6 4
1 11
4 5
5 14
8 2
4 2
1 3
8 3
6 4
```




```output1
3
-1
12
6
6
1
6
```


