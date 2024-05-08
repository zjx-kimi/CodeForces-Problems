## Description

<div><p>Flowey has planted a bomb in Snowdin!</p><p>The bomb has a timer that is initially set to $b$. Every second, the timer will decrease by $1$. When the timer reaches $0$, the bomb will explode! To give the residents of Snowdin enough time to evacuate, you will need to delay the bomb from exploding for as long as possible.</p><p>You have $n$ tools. Each tool can only be used <span class="tex-font-style-bf">at most</span> once. If you use the $i$-th tool, the timer will increase by $x_i$. However, if the timer is changed to an integer larger than $a$, the timer will be set to $a$ due to a bug.</p><p>More specifically, the following events will happen every second in the following order:</p><ol> <li> You will choose some (possibly none) of your tools that have not been used before. If you choose the $i$-th tool, and the bomb's timer is currently set to $c$, the timer will be changed to $\min(c + x_i, a)$. </li><li> The timer decreases by $1$. </li><li> If the timer reaches $0$, the bomb explodes. </li></ol><p>Jellyfish now wants to know the maximum time in seconds until the bomb explodes if the tools are used optimally.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 2000$). The description of the test cases follows.</p><p>The first line of each test case contains three integers $a$, $b$ and $n$ ($1 \leq b \leq a \leq 10^9$, $1 \leq n \leq 100$)&nbsp;— the maximum value of the bomb's timer, the initial value of the timer of the bomb and the number of tools.</p><p>The second line of each test contains $n$ integers $x_1, x_2, \dots, x_n$ ($1 \leq x_i \leq 10^9$)&nbsp;— the number the timer can increase by using the $i$-th tool.</p><p>Note that the sum of $n$ over all test cases is not bounded.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the maximum time in seconds until the bomb explodes.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 2000$). The description of the test cases follows.</p><p>The first line of each test case contains three integers $a$, $b$ and $n$ ($1 \leq b \leq a \leq 10^9$, $1 \leq n \leq 100$)&nbsp;— the maximum value of the bomb's timer, the initial value of the timer of the bomb and the number of tools.</p><p>The second line of each test contains $n$ integers $x_1, x_2, \dots, x_n$ ($1 \leq x_i \leq 10^9$)&nbsp;— the number the timer can increase by using the $i$-th tool.</p><p>Note that the sum of $n$ over all test cases is not bounded.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the maximum time in seconds until the bomb explodes.</p>





```input1|2,3
2
5 3 3
1 1 7
7 1 5
1 2 5 6 8
```




```output1
9
21
```



## Note

<p>Let $c$ denote the value of the bomb's timer. In the first test case:</p><ul> <li> Second $1$: choose tool $1$ and $2$ at this second, then $c=5$; the timer decreases by $1$, then $c=4$. </li><li> Second $2$: the timer decreases by $1$, then $c=3$. </li><li> Second $3$: the timer decreases by $1$, then $c=2$. </li><li> Second $4$: the timer decreases by $1$, then $c=1$. </li><li> Second $5$: choose tool $3$, then $c=5$; the timer decreases by $1$, then $c=4$. </li><li> Second $6$: the timer decreases by $1$, then $c=3$. </li><li> Second $7$: the timer decreases by $1$, then $c=2$. </li><li> Second $8$: the timer decreases by $1$, then $c=1$. </li><li> Second $9$: the timer decreases by $1$, then $c=0$. The bomb explodes. </li></ul><p>It can be proved that there is no way to use the tools such that the bomb explodes after more than $9$ seconds.</p>
