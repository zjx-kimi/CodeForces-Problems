## Description

<div><p>Vlad went into his appartment house entrance, now he is on the $1$-th floor. He was going to call the elevator to go up to his apartment.</p><p>There are only two elevators in his house. Vlad knows for sure that:</p><ul> <li> the first elevator is currently on the floor $a$ (it is currently motionless), </li><li> the second elevator is located on floor $b$ and goes to floor $c$ ($b \ne c$). Please note, if $b=1$, then the elevator is already leaving the floor $1$ and Vlad does not have time to enter it. </li></ul><p>If you call the first elevator, it will immediately start to go to the floor $1$. If you call the second one, then first it will reach the floor $c$ and only then it will go to the floor $1$. It takes $|x - y|$ seconds for each elevator to move from floor $x$ to floor $y$.</p><p>Vlad wants to call an elevator that will come to him faster. Help him choose such an elevator.</p></div><div class="input-specification"><p>The first line of the input contains the only $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>This is followed by $t$ lines, three integers each $a$, $b$ and $c$ ($1 \le a, b, c \le 10^8$, $b \ne c$)&nbsp;— floor numbers described in the statement.</p></div><div class="output-specification"><p>Output $t$ numbers, each of which is the answer to the corresponding test case. As an answer, output:</p><ul> <li> $1$, if it is better to call the first elevator; </li><li> $2$, if it is better to call the second one; </li><li> $3$, if it doesn't matter which elevator to call (both elevators will arrive in the same time). </li></ul></div>

## Input

<p>The first line of the input contains the only $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>This is followed by $t$ lines, three integers each $a$, $b$ and $c$ ($1 \le a, b, c \le 10^8$, $b \ne c$)&nbsp;— floor numbers described in the statement.</p>

## Output

<p>Output $t$ numbers, each of which is the answer to the corresponding test case. As an answer, output:</p><ul> <li> $1$, if it is better to call the first elevator; </li><li> $2$, if it is better to call the second one; </li><li> $3$, if it doesn't matter which elevator to call (both elevators will arrive in the same time). </li></ul>





```input1|2,4
3
1 2 3
3 1 2
3 2 1
```




```output1
1
3
2
```



## Note

<p>In the first test case of the example, the first elevator is already on the floor of $1$.</p><p>In the second test case of the example, when called, the elevators would move as follows:</p><ul> <li> At the time of the call, the first elevator is on the floor of $3$, and the second one is on the floor of $1$, but is already going to another floor; </li><li> in $1$ second after the call, the first elevator would be on the floor $2$, the second one would also reach the floor $2$ and now can go to the floor $1$; </li><li> in $2$ seconds, any elevator would reach the floor $1$. </li></ul><p>In the third test case of the example, the first elevator will arrive in $2$ seconds, and the second in $1$.</p>
