## Description

<div><p>You just created a new character in your favourite role-playing game and now have to decide how to skill him.</p><center> <img class="tex-graphics" src="file://4EeU5G8n.png" style="max-width: 100.0%;max-height: 100.0%;" width="189px"> </center><p>The two skill attributes to be chosen are: <span class="tex-font-style-underline">damage per hit</span> and <span class="tex-font-style-underline">hits per second</span>. Damage per hit is the amount of damage you deal with a single hit, while hits per second is the number of hits you can make in one second. Initially, both skill attributes are set at $0$. You have $k$ skill points to distribute as you want; in other words, you can choose the values of the two skills so that they are positive integers with sum at most $k$. </p><p>The tutorial of the game (the boring part you want to finish as soon as possible) consists of $n$ monsters to be killed one after the other. The $i$-th monster has $h_i$ health points, i.e., it dies after you have inflicted at least $h_i$ damage.</p><p>How can you assign the two skill attributes to minimize the time necessary to kill all the $n$ monsters?</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $k$ ($1\leq n\leq200\,000$, $2\leq k\leq200\,000$) — the number of enemies and the number of skill points.</p><p>The second line contains $n$ integers $h_i$ ($1\leq h_i\leq10^{13}$) — the health of the $i$th enemy.</p></div><div class="output-specification"><p>Print two positive integers $x$ and $y$ ($1\le x, y$ and $x+y\le k$)&nbsp;— the number of skill points you want to invest in damage per hit and hits per second. If there are multiple optimal solutions, print any of them.</p></div>

## Input

<p>The first line contains two integers $n$ and $k$ ($1\leq n\leq200\,000$, $2\leq k\leq200\,000$) — the number of enemies and the number of skill points.</p><p>The second line contains $n$ integers $h_i$ ($1\leq h_i\leq10^{13}$) — the health of the $i$th enemy.</p>

## Output

<p>Print two positive integers $x$ and $y$ ($1\le x, y$ and $x+y\le k$)&nbsp;— the number of skill points you want to invest in damage per hit and hits per second. If there are multiple optimal solutions, print any of them.</p>





```input1|
1 7
14
```




```input2|
4 9
1 2 3 4
```




```input3|
5 13
3 4 5 6 7
```




```output1
3 4
```




```output2
4 5
```




```output3
7 6
```



## Note

<p>In the <span class="tex-font-style-bf">first sample</span>, there is only one monster and you have $7$ skill points to distribute. If you make $3$ damage per hit, you will need $5$ hits to kill it. If you do $4$ hits per second, you will need $1.25$ seconds to beat the monster. There is no way to beat the monster faster than this.</p><p>In the <span class="tex-font-style-bf">second sample</span>, you will need one hit for each monster and a total time of $0.8$ seconds if you distribute $4$ skill points on damage per hit and the remaining $5$ points on hits per second.</p>
