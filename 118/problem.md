## Description

<div><p>Alice and Bob are swimming in the pool under the guidance of their instructor Monocarp.</p><p>The pool can be represented as a segment on the OX-axis from $0$ to $50$. Both Alice and Bob started at moment $0$ at point $0$ with <span class="tex-font-style-it">positive real</span> speeds $v_A$ and $v_B$ correspondingly.</p><p>Both Alice and Bob swim from $0$ to point $50$, then instantly turn back and swim from $50$ to $0$. At $0$ they turn back again and swim to $50$ and so on.</p><p>Monocarp logged all valuable info about Alice and Bob, including moments of time when they met at the same point (Alice and Bob swim on parallel lanes, so they don't bother each other). Let's name that moments of time as sequence $t_1, t_2, \dots, t_n$.</p><p>Due to some incident, Monocarp lost almost all data he recorded, and all he has now is array $t$. Monocarp remembers that Alice and Bob had distinct positive real swimming speeds $v_A$ and $v_B$ ($v_A &gt; 0$; $v_B &gt; 0$; $v_A \neq v_B$) and that sequence $t$ contains the first $n$ meeting moments.</p><p>But looking at sequence $t$ he noticed that all $t_i$ are integer values, and now he doubts is sequence $t$ valid or there are some errors in it. Help Monocarp to check array $t$!</p></div><div class="input-specification"><p>The first line contains a single integer $c$ ($1 \le c \le 10^4$)&nbsp;— the number of test cases. Then $c$ cases follow.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the size of array $t$.</p><p>The second line of each test case contains $n$ integers $t_1, t_2, \dots, t_n$ ($1 \le t_1 &lt; t_2 &lt; \dots &lt; t_n \le 10^9$)&nbsp;— the meeting moments in the increasing order.</p><p>It's guaranteed that the sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print <span class="tex-font-style-tt">VALID</span> if the array $t$ is a valid array, or (in other words) exist such real values $v_A$ and $v_B$ ($v_A, v_B &gt; 0$; $v_A \neq v_B$) that array $t$ contains the first $n$ meeting moments of Alice and Bob in the pool.</p><p>Otherwise, print <span class="tex-font-style-tt">INVALID</span>.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">vALid</span>", "<span class="tex-font-style-tt">valid</span>", "<span class="tex-font-style-tt">Valid</span>", and "<span class="tex-font-style-tt">VALID</span>" will be recognized as positive responses.</p></div>

## Input

<p>The first line contains a single integer $c$ ($1 \le c \le 10^4$)&nbsp;— the number of test cases. Then $c$ cases follow.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the size of array $t$.</p><p>The second line of each test case contains $n$ integers $t_1, t_2, \dots, t_n$ ($1 \le t_1 &lt; t_2 &lt; \dots &lt; t_n \le 10^9$)&nbsp;— the meeting moments in the increasing order.</p><p>It's guaranteed that the sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, print <span class="tex-font-style-tt">VALID</span> if the array $t$ is a valid array, or (in other words) exist such real values $v_A$ and $v_B$ ($v_A, v_B &gt; 0$; $v_A \neq v_B$) that array $t$ contains the first $n$ meeting moments of Alice and Bob in the pool.</p><p>Otherwise, print <span class="tex-font-style-tt">INVALID</span>.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">vALid</span>", "<span class="tex-font-style-tt">valid</span>", "<span class="tex-font-style-tt">Valid</span>", and "<span class="tex-font-style-tt">VALID</span>" will be recognized as positive responses.</p>





```input1|2,3,6,7,10,11,14,15
7
1
42
4
3 4 6 8
5
1 2 3 4 5
3
999999998 999999999 1000000000
5
4 6 8 12 16
4
6 11 12 14
2
10 30
```




```output1
VALID
VALID
VALID
INVALID
VALID
INVALID
INVALID
```



## Note

<p>In the first test case, imagine a situation: $v_A = 1$ and $v_B = \frac{29}{21}$. Then, at moment $42$ Alice and Bob will be at point $42$.</p><p>In the second test case, imagine a situation: $v_A = \frac{175}{6}$ and $v_B = \frac{25}{6}$. Then, at moment $3$ Alice and Bob will meet at point $12.5$, at $4$ they'll meet at point $\frac{50}{3}$, at moment $6$ they'll meet at $25$ and at moment $8$&nbsp;— at point $\frac{100}{3}$. Since it's exactly the first $4$ meeting moments. Array $t$ may be <span class="tex-font-style-tt">valid</span>.</p><p>In the third test case, one of the possible situations is $v_A = 25$ and $v_B = 75$.</p>
