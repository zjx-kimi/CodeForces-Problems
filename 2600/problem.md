## Description

<div><p>You have a robot that can move along a number line. At time moment $0$ it stands at point $0$.</p><p>You give $n$ commands to the robot: at time $t_i$ seconds you command the robot to go to point $x_i$. Whenever the robot receives a command, it starts moving towards the point $x_i$ with the speed of $1$ unit per second, and he stops when he reaches that point. However, while the robot is moving, it <span class="tex-font-style-bf">ignores</span> all the other commands that you give him.</p><p>For example, suppose you give three commands to the robot: at time $1$ move to point $5$, at time $3$ move to point $0$ and at time $6$ move to point $4$. Then the robot stands at $0$ until time $1$, then starts moving towards $5$, ignores the second command, reaches $5$ at time $6$ and immediately starts moving to $4$ to execute the third command. At time $7$ it reaches $4$ and stops there.</p><p>You call the command $i$ successful, if there is a time moment in the range $[t_i, t_{i + 1}]$ (i.&nbsp;e. after you give this command and before you give another one, both bounds inclusive; we consider $t_{n + 1} = +\infty$) when the robot is at point $x_i$. Count the number of successful commands. Note that it is possible that an ignored command is successful.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases. The next lines describe the test cases.</p><p>The first line of a test case contains a single integer $n$ ($1 \le n \le 10^5$)&nbsp;— the number of commands.</p><p>The next $n$ lines describe the commands. The $i$-th of these lines contains two integers $t_i$ and $x_i$ ($1 \le t_i \le 10^9$, $-10^9 \le x_i \le 10^9$)&nbsp;— the time and the point of the $i$-th command.</p><p>The commands are ordered by time, that is, $t_i &lt; t_{i + 1}$ for all possible $i$.</p><p>The sum of $n$ over test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each testcase output a single integer&nbsp;— the number of successful commands.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases. The next lines describe the test cases.</p><p>The first line of a test case contains a single integer $n$ ($1 \le n \le 10^5$)&nbsp;— the number of commands.</p><p>The next $n$ lines describe the commands. The $i$-th of these lines contains two integers $t_i$ and $x_i$ ($1 \le t_i \le 10^9$, $-10^9 \le x_i \le 10^9$)&nbsp;— the time and the point of the $i$-th command.</p><p>The commands are ordered by time, that is, $t_i &lt; t_{i + 1}$ for all possible $i$.</p><p>The sum of $n$ over test cases does not exceed $10^5$.</p>

## Output

<p>For each testcase output a single integer&nbsp;— the number of successful commands.</p>





```input1
8
3
1 5
3 0
6 4
3
1 5
2 4
10 -5
5
2 -5
3 1
4 1
5 1
6 1
4
3 3
5 -3
9 2
12 0
8
1 1
2 -6
7 2
8 3
12 -9
14 2
18 -1
23 9
5
1 -4
4 -7
6 -1
7 -3
8 -7
2
1 2
2 -2
6
3 10
5 5
8 0
12 -4
14 -7
19 -5
```




```output1
1
2
0
2
1
1
0
2
```



## Note

<p>The movements of the robot in the first test case are described in the problem statement. Only the last command is successful.</p><p>In the second test case the second command is successful: the robot passes through target point $4$ at time $5$. Also, the last command is eventually successful.</p><p>In the third test case no command is successful, and the robot stops at $-5$ at time moment $7$.</p><p>Here are the $0$-indexed sequences of the positions of the robot in each second for each testcase of the example. After the cut all the positions are equal to the last one: </p><ol> <li> $[0, 0, 1, 2, 3, 4, 5, 4, 4, \dots]$ </li><li> $[0, 0, 1, 2, 3, 4, 5, 5, 5, 5, 5, 4, 3, 2, 1, 0, -1, -2, -3, -4, -5, -5, \dots]$ </li><li> $[0, 0, 0, -1, -2, -3, -4, -5, -5, \dots]$ </li><li> $[0, 0, 0, 0, 1, 2, 3, 3, 3, 3, 2, 2, 2, 1, 0, 0, \dots]$ </li><li> $[0, 0, 1, 0, -1, -2, -3, -4, -5, -6, -6, -6, -6, -7, -8, -9, -9, -9, -9, -8, -7, -6, -5, -4, -3, -2, -1, -1, \dots]$ </li><li> $[0, 0, -1, -2, -3, -4, -4, -3, -2, -1, -1, \dots]$ </li><li> $[0, 0, 1, 2, 2, \dots]$ </li><li> $[0, 0, 0, 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 10, 9, 8, 7, 6, 5, 4, 3, 2, 1, 0, -1, -2, -3, -4, -5, -6, -7, -7, \dots]$ </li></ol>
