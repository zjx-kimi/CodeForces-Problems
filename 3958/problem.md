## Description

<div><p>Polycarp decided to relax on his weekend and visited to the performance of famous ropewalkers: Agafon, Boniface and Konrad.</p><p>The rope is straight and infinite in both directions. At the beginning of the performance, Agafon, Boniface and Konrad are located in positions $a$, $b$ and $c$ respectively. At the end of the performance, the distance between each pair of ropewalkers was <span class="tex-font-style-bf">at least</span> $d$.</p><p>Ropewalkers can walk on the rope. In one second, only one ropewalker can change his position. Every ropewalker can change his position exactly by $1$ (i. e. shift by $1$ to the left or right direction on the rope). Agafon, Boniface and Konrad <span class="tex-font-style-bf">can not</span> move at the same time (<span class="tex-font-style-bf">Only one of them can move at each moment</span>). Ropewalkers can be at the same positions at the same time and can "walk past each other".</p><p>You should find the minimum duration (in seconds) of the performance. In other words, find the minimum number of seconds needed so that the distance between each pair of ropewalkers can be greater or equal to $d$.</p><p>Ropewalkers can walk to negative coordinates, due to the rope is infinite to both sides.</p></div><div class="input-specification"><p>The only line of the input contains four integers $a$, $b$, $c$, $d$ ($1 \le a, b, c, d \le 10^9$). It is possible that any two (or all three) ropewalkers are in the same position at the beginning of the performance.</p></div><div class="output-specification"><p>Output one integer — the minimum duration (in seconds) of the performance.</p></div>

## Input

<p>The only line of the input contains four integers $a$, $b$, $c$, $d$ ($1 \le a, b, c, d \le 10^9$). It is possible that any two (or all three) ropewalkers are in the same position at the beginning of the performance.</p>

## Output

<p>Output one integer — the minimum duration (in seconds) of the performance.</p>





```input1
5 2 6 3
```




```input2
3 1 5 6
```




```input3
8 3 3 2
```




```input4
2 3 10 4
```




```output1
2
```




```output2
8
```




```output3
2
```




```output4
3
```



## Note

<p>In the first example: in the first two seconds Konrad moves for 2 positions to the right (to the position $8$), while Agafon and Boniface stay at their positions. Thus, the distance between Agafon and Boniface will be $|5 - 2| = 3$, the distance between Boniface and Konrad will be $|2 - 8| = 6$ and the distance between Agafon and Konrad will be $|5 - 8| = 3$. Therefore, all three pairwise distances will be at least $d=3$, so the performance could be finished within 2 seconds.</p>
