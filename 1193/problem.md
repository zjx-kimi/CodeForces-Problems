## Description

<div><p><span class="tex-font-style-bf">This problem was copied by the author from another online platform. Codeforces strongly condemns this action and therefore further submissions to this problem are not accepted.</span></p><p>Debajyoti has a very important meeting to attend and he is already very late. Harsh, his driver, needs to take Debajyoti to the destination for the meeting as fast as possible.</p><p>Harsh needs to pick up Debajyoti from his home and take him to the destination so that Debajyoti can attend the meeting in time. A straight road with $n$ traffic lights connects the home and the destination for the interview. The traffic lights are numbered in order from $1$ to $n$.</p><p>Each traffic light cycles after $t$ seconds. The $i$-th traffic light is $\color{green}{\text{green}}$ (in which case Harsh can cross the traffic light) for the first $g_i$ seconds, and $\color{red}{\text{red}}$ (in which case Harsh must wait for the light to turn $\color{green}{\text{green}}$) for the remaining $(t−g_i)$ seconds, after which the pattern repeats. Each light's cycle repeats indefinitely and initially, the $i$-th light is $c_i$ seconds into its cycle (a light with $c_i=0$ has just turned $\color{green}{\text{green}}$). In the case that Harsh arrives at a light at the same time it changes colour, he will obey the new colour. <span class="tex-font-style-it">Formally</span>, the $i$-th traffic light is $\color{green}{\text{green}}$ from $[0,g_i)$ and $\color{red}{\text{red}}$ from $[g_i,t)$ (after which it repeats the cycle). The $i$-th traffic light is initially at the $c_i$-th second of its cycle.</p><p>From the $i$-th traffic light, <span class="tex-font-style-bf">exactly</span> $d_i$ seconds are required to travel to the next traffic light (that is to the $(i+1)$-th light). Debajyoti's home is located just before the first light and Debajyoti drops for the interview as soon as he passes the $n$-th light. In other words, no time is required to reach the first light from Debajyoti's home or to reach the interview centre from the $n$-th light.</p><p>Harsh does not know how much longer it will take for Debajyoti to get ready. While waiting, he wonders what is the minimum possible amount of time he will spend driving provided he starts the moment Debajyoti arrives, which can be anywhere between $0$ to $\infty$ seconds from now. Can you tell Harsh the minimum possible amount of time he needs to spend on the road?</p><p><span class="tex-font-style-bf">Please note that Harsh can only start or stop driving at integer moments of time.</span></p></div><div class="input-specification"><p>The first line of input will contain two integers, $n$ and $t$ ($2 \le n \le 2 \cdot 10^5$, $2 \le t \le 10^9$) denoting the number of traffic lights and the cycle length of the traffic lights respectively.</p><p>$n$ lines of input follow. The $i$-th line will contain two integers $g_i$ and $c_i$ ($1 \le g_i &lt; t$, $0 \le c_i &lt; t$) describing the $i$-th traffic light.</p><p>The following line of input contains $n−1$ integers $d_1, d_2, \ldots, d_{n-1}$ ($0 \le d_i \le 10^9$) — the time taken to travel from the $i$-th to the $(i+1)$-th traffic light.</p></div><div class="output-specification"><p>Output a single integer&nbsp;— the minimum possible amount of time Harsh will spend driving.</p></div>

## Input

<p>The first line of input will contain two integers, $n$ and $t$ ($2 \le n \le 2 \cdot 10^5$, $2 \le t \le 10^9$) denoting the number of traffic lights and the cycle length of the traffic lights respectively.</p><p>$n$ lines of input follow. The $i$-th line will contain two integers $g_i$ and $c_i$ ($1 \le g_i &lt; t$, $0 \le c_i &lt; t$) describing the $i$-th traffic light.</p><p>The following line of input contains $n−1$ integers $d_1, d_2, \ldots, d_{n-1}$ ($0 \le d_i \le 10^9$) — the time taken to travel from the $i$-th to the $(i+1)$-th traffic light.</p>

## Output

<p>Output a single integer&nbsp;— the minimum possible amount of time Harsh will spend driving.</p>





```input1
5 10
4 2
7 3
3 6
5 2
8 0
1 2 3 4
```




```input2
6 9
5 3
5 5
7 0
5 8
7 7
6 6
0 0 0 0 0
```




```output1
11
```




```output2
3
```



## Note

<p>In the first example, Harsh can do the following:</p><ul><li> Initially, the $5$ traffic lights are at the following seconds in their cycle: $\{2,3,6,2,0\}$.</li><li> An optimal time for Harsh to start is if Debajyoti arrives after $1$ second. Note that this $1$ second will not be counted in the final answer.</li><li> The lights will be now at $\{3,4,7,3,1\}$, so Harsh can drive from the $1$-st light to the $2$-nd light, which requires $1$ second to travel.</li><li> The lights are now at $\{4,5,8,4,2\}$, so Harsh can continue driving, without stopping, to the $3$-rd light, which requires $2$ seconds to travel.</li><li> The lights are now at $\{6,7,0,6,4\}$, so Harsh continues to the $4$-th light, which requires $3$ seconds to travel.</li><li> The lights are now at $\{9,0,3,9,7\}$. Harsh must wait $1$ second for the $4$-th light to turn green before going to the $5$-th light, which requires $4$ seconds to travel.</li><li> The lights are now at $\{4,5,8,4,2\}$, so Harsh can continue traveling, without stopping, to the meeting destination. The total time that Harsh had to drive for is $1+2+3+1+4=11$ seconds.</li></ul><p>In the second example, Harsh can do the following:</p><ul><li> Initially, the $6$ traffic lights are at the following seconds in their cycle: $\{3,5,0,8,7,6\}$.</li><li> An optimal time for Harsh to start is if Debajyoti arrives after $1$ second. Note that this $1$ second will not be counted in the final answer.</li><li> The lights will be now at $\{4,6,1,0,8,7\}$, so Harsh can drive from the $1$-st light to the $2$-nd light, which requires $0$ seconds to travel.</li><li> The lights are still at $\{4,6,1,0,8,7\}$. Harsh must wait $3$ seconds for the $2$-nd light to turn green, before going to the $3$-rd light, which requires $0$ seconds to travel.</li><li> The lights are now at $\{7,0,4,3,2,1\}$, so Harsh continues to the $4$-th light, which requires $0$ seconds to travel.</li><li> The lights are still at $\{7,0,4,3,2,1\}$, so Harsh continues to the $5$-th light, which requires $0$ seconds to travel.</li><li> The lights are still at $\{7,0,4,3,2,1\}$, so Harsh continues to the $6$-th light, which requires $0$ seconds to travel.</li><li> The lights are still at $\{7,0,4,3,2,1\}$, so Harsh can continue traveling, without stopping, to the meeting destination. The total time that Harsh had to drive for is $0+3+0+0+0=3$ seconds.</li></ul>
