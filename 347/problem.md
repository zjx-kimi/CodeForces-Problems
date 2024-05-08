## Description

<div><p>You are in a corridor that extends infinitely to the right, divided into square rooms. You start in room $1$, proceed to room $k$, and then return to room $1$. You can choose the value of $k$. Moving to an adjacent room takes $1$ second.</p><p>Additionally, there are $n$ traps in the corridor: the $i$-th trap is located in room $d_i$ and will be activated $s_i$ seconds <span class="tex-font-style-bf">after you enter the room</span> $\boldsymbol{d_i}$. Once a trap is activated, you cannot enter or exit a room with that trap.</p><center> <img class="tex-graphics" src="file://4uJH2yrO.png" style="max-width: 100.0%;max-height: 100.0%;">  <span class="tex-font-size-small">A schematic representation of a possible corridor and your path to room $k$ and back.</span> </center><p>Determine the maximum value of $k$ that allows you to travel from room $1$ to room $k$ and then return to room $1$ safely.</p><p>For instance, if $n=1$ and $d_1=2, s_1=2$, you can proceed to room $k=2$ and return safely (the trap will activate at the moment $1+s_1=1+2=3$, it can't prevent you to return back). But if you attempt to reach room $k=3$, the trap will activate at the moment $1+s_1=1+2=3$, preventing your return (you would attempt to enter room $2$ on your way back at second $3$, but the activated trap would block you). Any larger value for $k$ is also not feasible. Thus, the answer is $k=2$.</p></div><div class="input-specification"><p>The first line of the input contains an integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>The descriptions of the test cases follow.</p><p>The first line of each test case description contains an integer $n$ ($1 \le n \le 100$)&nbsp;— the number of traps.</p><p>The following $n$ lines of each test case description present two integers $d_i$ and $s_i$ ($1 \le d_i, s_i \le 200$)&nbsp;— the parameters of a trap (you must leave room $d_i$ strictly before $s_i$ seconds have passed since entering this room). It's possible for multiple traps to occupy a single room (the values of $d_i$ can be repeated).</p></div><div class="output-specification"><p>For each test case, print the maximum value of $k$ that allows you to travel to room $k$ and return to room $1$ without encountering an active trap.</p></div>

## Input

<p>The first line of the input contains an integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>The descriptions of the test cases follow.</p><p>The first line of each test case description contains an integer $n$ ($1 \le n \le 100$)&nbsp;— the number of traps.</p><p>The following $n$ lines of each test case description present two integers $d_i$ and $s_i$ ($1 \le d_i, s_i \le 200$)&nbsp;— the parameters of a trap (you must leave room $d_i$ strictly before $s_i$ seconds have passed since entering this room). It's possible for multiple traps to occupy a single room (the values of $d_i$ can be repeated).</p>

## Output

<p>For each test case, print the maximum value of $k$ that allows you to travel to room $k$ and return to room $1$ without encountering an active trap.</p>





```input1|2,3,8,9,15,16,17,21,22,23,24
7
1
2 2
3
2 8
4 3
5 2
1
200 200
4
1 20
5 9
3 179
100 1
2
10 1
1 18
2
1 1
1 2
3
1 3
1 1
1 3
```




```output1
2
5
299
9
9
1
1
```



## Note

<p>The first test case is explained in the problem statement above.</p><p>In the second test case, the second trap prevents you from achieving $k\ge6$. If $k\ge6$, the second trap will activate at the moment $3+s_2=3+3=6$ (the time you enter room $4$ plus $s_2$). In the case of $k\ge6$, you will return to room $4$ at time $7$ or later. The trap will be active at that time. It can be shown that room $k=5$ can be reached without encountering an active trap.</p><p>In the third test case, you can make it to room $299$ and then immediately return to room $1$.</p>
