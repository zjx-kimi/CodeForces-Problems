## Description

<div><p>Bosco is studying the behaviour of particles. He decided to investigate on the peculiar behaviour of the so-called "four-one-two" particle. He does the following:</p><p>There is a line of length $n+1$, where the topmost point is position $0$ and bottommost is position $n+1$. The particle is initially (at time $t=0$) at position $0$ and heading downwards. The particle moves at the speed of $1$ unit per second. There are $n$ oscillators at positions $1,2,\ldots,n$.</p><p>Each oscillator can be described by a binary string. The initial state of each oscillator is the first character of its binary string. When the particle hits with an oscillator, the particle reverses its direction if its current state is $\texttt{1}$ and continues to move at the same direction if its current state is $\texttt{0}$, and that oscillator moves on to the next state (the next state of the last state is defined as the first state). Additionally, the particle always reverses its direction when it is at position $0$ or $n+1$ at time $t &gt; 0$.</p><p>Bosco would like to know the cycle length of the movement of particle. The cycle length is defined as the minimum value of $c$ such that for any time $t \ge 0$, the position of the particle at time $t$ is same as the position of the particle at time $t+c$. It can be proved that such value $c$ always exists. As he realises the answer might be too large, he asks you to output your answer modulo $998244353$.</p></div><div class="input-specification"><p>The first line contains an integer $n$ ($1\le n\le10^6$) — the number of oscillators.</p><p>The $i$-th of the next $n$ line contains a binary string $s_i$ ($1\le\left|s_i\right|\le10^6$) — the binary string, that contains only characters $\texttt{0}$ and $\texttt{1}$, describing the oscillator at position $i$.</p><p>It is guaranteed that the sum of all $|s_i|$ does not exceed $10^6$.</p></div><div class="output-specification"><p>Output a single integer integer — the cycle length of the movement of the particle, modulo $998244353$.</p></div>

## Input

<p>The first line contains an integer $n$ ($1\le n\le10^6$) — the number of oscillators.</p><p>The $i$-th of the next $n$ line contains a binary string $s_i$ ($1\le\left|s_i\right|\le10^6$) — the binary string, that contains only characters $\texttt{0}$ and $\texttt{1}$, describing the oscillator at position $i$.</p><p>It is guaranteed that the sum of all $|s_i|$ does not exceed $10^6$.</p>

## Output

<p>Output a single integer integer — the cycle length of the movement of the particle, modulo $998244353$.</p>





```input1
1
00
```




```input2
2
01
010
```




```input3
4
0101
000
1
01
```




```input4
4
01010
0001
11
0001
```




```output1
4
```




```output2
16
```




```output3
12
```




```output4
120
```



## Note

<p>In the first sample, the only oscillator at position $1$ always has state $\texttt{0}$. At time moments $0,1,2,3$ positions the particle are $0,1,2,1$ respectively. Then the same positions will be repeated, so $c=4$.</p><p>Animation for the second sample: <a href="https://u.cubeupload.com/culver0412/GJ5PNy.png">here</a> or <a href="https://i.imgur.com/X35t71G.gif">a smoother animation</a>.</p>
