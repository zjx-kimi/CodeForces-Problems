## Description

<div><p>Alex has bought a new novel that was published in $n$ volumes. He has read these volumes one by one, and each volume has taken him several (maybe one) full days to read. So, on the first day, he was reading the first volume, and on each of the following days, he was reading either the same volume he had been reading on the previous day, or the next volume.</p><p>Let $v_i$ be the number of the volume Alex was reading on the $i$-th day. Here are some examples:</p><ul> <li> one of the possible situations is $v_1 = 1$, $v_2 = 1$, $v_3 = 2$, $v_4 = 3$, $v_5 = 3$&nbsp;— this situation means that Alex has spent two days ($1$-st and $2$-nd) on the first volume, one day ($3$-rd) on the second volume, and two days ($4$-th and $5$-th) on the third volume; </li><li> a situation $v_1 = 2$, $v_2 = 2$, $v_3 = 3$ is impossible, since Alex started with the first volume (so $v_1$ cannot be anything but $1$); </li><li> a situation $v_1 = 1$, $v_2 = 2$, $v_3 = 3$, $v_4 = 1$ is impossible, since Alex won't return to the first volume after reading the third one; </li><li> a situation $v_1 = 1$, $v_2 = 3$ is impossible, since Alex doesn't skip volumes. </li></ul><p>You know that Alex was reading the volume $v_a$ on the day $a$, and the volume $v_c$ on the day $c$. Now you want to guess which volume was he reading on the day $b$, which is between the days $a$ and $c$ (so $a &lt; b &lt; c$). There may be some ambiguity, so you want to make any valid guess (i. e. choose some volume number $v_b$ so it's possible that Alex was reading volume $v_a$ on day $a$, volume $v_b$ on day $b$, and volume $v_c$ on day $c$).</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). Description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 100$)&nbsp;— the number of volumes the novel consists of.</p><p>The second line of each test case contains two integers $a$ and $v_a$ ($1 \le a \le 98$; $1 \le v_a \le a$) denoting that Alex was reading volume $v_a$ at day $a$.</p><p>The third line of each test case contains two integers $c$ and $v_c$ ($a + 2 \le c \le 100$; $v_a \le v_c \le c$) denoting that Alex was reading volume $v_c$ at day $c$.</p><p>The fourth line of each test case contains one integer $b$ ($a &lt; b &lt; c$)&nbsp;— the day you are interested in.</p><p>It's guaranteed that the input is not controversial, in other words, Alex could read volume $v_a$ at day $a$ and volume $v_c$ at day $c$.</p></div><div class="output-specification"><p>For each test case, print the possible index of volume Alex could read at day $b$. If there are multiple answers, print any.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). Description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 100$)&nbsp;— the number of volumes the novel consists of.</p><p>The second line of each test case contains two integers $a$ and $v_a$ ($1 \le a \le 98$; $1 \le v_a \le a$) denoting that Alex was reading volume $v_a$ at day $a$.</p><p>The third line of each test case contains two integers $c$ and $v_c$ ($a + 2 \le c \le 100$; $v_a \le v_c \le c$) denoting that Alex was reading volume $v_c$ at day $c$.</p><p>The fourth line of each test case contains one integer $b$ ($a &lt; b &lt; c$)&nbsp;— the day you are interested in.</p><p>It's guaranteed that the input is not controversial, in other words, Alex could read volume $v_a$ at day $a$ and volume $v_c$ at day $c$.</p>

## Output

<p>For each test case, print the possible index of volume Alex could read at day $b$. If there are multiple answers, print any.</p>





```input1
4
1
1 1
100 1
99
4
10 1
20 4
16
100
1 1
100 100
42
100
1 1
100 2
99
```




```output1
1
2
42
1
```



## Note

<p>In the first test case, since Alex was reading volume $1$ both at day $1$ and at day $100$ then he was reading volume $1$ at any day between them.</p><p>In the second test case, Alex could read any volume from $1$ to $4$ at day $16$. For example, he could read volume $1$ from day $1$ to day $15$, volume $2$ at days $16$ and $17$, volume $3$ at day $18$ and volume $4$ at days $19$ and $20$.</p><p>In the third test case, there is only one possible situation: Alex read one volume per day, so at day $42$ he read volume $42$.</p>
