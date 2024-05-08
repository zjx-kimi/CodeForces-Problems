## Description

<div><center> <img class="tex-graphics" height="302px" src="file://ODDuhirn.png" style="max-width: 100.0%;max-height: 100.0%;" width="454px"> </center><p>There're $n$ robots placed on a number line. Initially, $i$-th of them occupies unit segment $[x_i, x_i + 1]$. Each robot has a program, consisting of $k$ instructions numbered from $1$ to $k$. The robot performs instructions in a cycle. Each instruction is described by an integer number. Let's denote the number corresponding to the $j$-th instruction of the $i$-th robot as $f_{i, j}$.</p><p>Initial placement of robots corresponds to the moment of time $0$. During one second from moment of time $t$ ($0 \le t$) until $t + 1$ the following process occurs: </p><ol> <li> Each robot performs $(t \bmod k + 1)$-th instruction from its list of instructions. Robot number $i$ takes number $F = f_{i, (t \bmod k + 1)}$. If this number is negative (less than zero), the robot is trying to move to the left with force $|F|$. If the number is positive (more than zero), the robot is trying to move to the right with force $F$. Otherwise, the robot does nothing. </li><li> Let's imaginary divide robots into groups of consecutive, using the following algorithm: <ul> <li> Initially, each robot belongs to its own group. </li><li> Let's sum up numbers corresponding to the instructions of the robots from one group. Note that we are summing numbers without taking them by absolute value. Denote this sum as $S$. We say that the whole group moves together, and does it with force $S$ by the same rules as a single robot. That is if $S$ is negative, the group is trying to move to the left with force $|S|$. If $S$ is positive, the group is trying to move to the right with force $S$. Otherwise, the group does nothing. </li><li> If one group is trying to move, and in the direction of movement touches another group, let's unite them. One group is touching another if their outermost robots occupy adjacent unit segments. </li><li> Continue this process until groups stop uniting. </li></ul> </li><li> Each robot moves by $1$ in the direction of movement of its group or stays in place if its group isn't moving. But there's one exception. </li><li> The exception is if there're two groups of robots, divided by exactly one unit segment, such that the left group is trying to move to the right and the right group is trying to move to the left. Let's denote sum in the left group as $S_l$ and sum in the right group as $S_r$. If $|S_l| \le |S_r|$ only the right group will move. Otherwise, only the left group will move. </li><li> Note that robots from one group don't glue together. They may separate in the future. The division into groups is imaginary and is needed only to understand how robots will move during one second $[t, t + 1]$. </li></ol><p>An illustration of the process happening during one second: </p><center> <img class="tex-graphics" src="file://IwyLU2qL.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>Rectangles represent robots. Numbers inside rectangles correspond to instructions of robots. The final division into groups is marked with arcs. Below are the positions of the robots after moving. Only the left of the two rightmost groups moved. That's because these two groups tried to move towards each other, and were separated by exactly one unit segment.</p><p>Look at the examples for a better understanding of the process.</p><p>You need to answer several questions. What is the position of $a_i$-th robot at the moment of time $t_i$?</p></div><div class="input-specification"><p>The first line contains two integer numbers $n$ and $k$&nbsp;— the number of robots and the number of instructions in the program of one robot ($1 \le n \le 100$, $1 \le k \le 50$).</p><p>The next line contains $n$ integer numbers $x_i$&nbsp;— positions of robots at moment of time $0$ ($-10^9 \le x_1 &lt; x_2 &lt; \dots &lt; x_n &lt; 10^9$).</p><p>The next $n$ lines contain descriptions of robots' programs. The $i$-th of these lines contains $k$ integer numbers $f_{i, j}$ ($|f_{i, j}| \le 10^6$).</p><p>The next line contains a single integer number $q$&nbsp;— the number of questions you to answer ($1 \le q \le 1000$).</p><p>The next $q$ lines contain two integer number $a_i$ and $t_i$ each, meaning that you should find a position of $a_i$-th robot at moment of time $t_i$ ($1 \le a_i \le n$, $0 \le t_i \le 10^{18}$).</p></div><div class="output-specification"><p>For every question output a single integer on the new line. Coordinate of the left border of unit segment occupied by the $a_i$-th robot at the moment of time $t_i$.</p></div>

## Input

<p>The first line contains two integer numbers $n$ and $k$&nbsp;— the number of robots and the number of instructions in the program of one robot ($1 \le n \le 100$, $1 \le k \le 50$).</p><p>The next line contains $n$ integer numbers $x_i$&nbsp;— positions of robots at moment of time $0$ ($-10^9 \le x_1 &lt; x_2 &lt; \dots &lt; x_n &lt; 10^9$).</p><p>The next $n$ lines contain descriptions of robots' programs. The $i$-th of these lines contains $k$ integer numbers $f_{i, j}$ ($|f_{i, j}| \le 10^6$).</p><p>The next line contains a single integer number $q$&nbsp;— the number of questions you to answer ($1 \le q \le 1000$).</p><p>The next $q$ lines contain two integer number $a_i$ and $t_i$ each, meaning that you should find a position of $a_i$-th robot at moment of time $t_i$ ($1 \le a_i \le n$, $0 \le t_i \le 10^{18}$).</p>

## Output

<p>For every question output a single integer on the new line. Coordinate of the left border of unit segment occupied by the $a_i$-th robot at the moment of time $t_i$.</p>





```input1
2 1
0 4
1
-1
8
1 0
2 0
1 1
2 1
1 2
2 2
1 3
2 3
```




```input2
2 1
0 4
2
-1
8
1 0
2 0
1 1
2 1
1 2
2 2
1 3
2 3
```




```input3
2 2
0 1
1 -1
-1 1
4
1 0
1 1
1 2
1 3
```




```input4
1 3
0
3 -2 1
3
1 5
1 10
1 15
```




```input5
4 3
-8 -4 2 5
-1 3 0
1 -3 -4
2 -5 2
-1 -4 2
5
3 12
4 18
4 11
1 6
1 10
```




```output1
0
4
1
3
1
2
1
2
```




```output2
0
4
1
3
2
3
3
4
```




```output3
0
0
-1
0
```




```output4
1
4
5
```




```output5
6
9
6
-8
-9
```


