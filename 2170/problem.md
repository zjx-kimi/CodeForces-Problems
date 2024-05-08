## Description

<div><p><span class="tex-font-style-bf">Note that the differences between easy and hard versions are the constraints on $n$ and the time limit. You can make hacks only if both versions are solved.</span></p><p>AquaMoon knew through foresight that some ghosts wanted to curse tourists on a pedestrian street. But unfortunately, this time, these ghosts were hiding in a barrier, and she couldn't enter this barrier in a short time and destroy them. Therefore, all that can be done is to save any unfortunate person on the street from the ghosts.</p><p>The pedestrian street can be represented as a one-dimensional coordinate system. There is one person hanging out on the pedestrian street. At the time $0$ he is at coordinate $x$, moving with a speed of $1$ unit per second. In particular, at time $i$ the person will be at coordinate $x+i$.</p><p>The ghosts are going to cast $n$ curses on the street. The $i$-th curse will last from time $tl_i-1+10^{-18}$ to time $tr_i+1-10^{-18}$ (exclusively) and will kill people with coordinates from $l_i-1+10^{-18}$ to $r_i+1-10^{-18}$ (exclusively). Formally that means, that the person, whose coordinate is between $(l_i-1+10^{-18},r_i+1-10^{-18})$ in the time range $(tl_i-1+10^{-18},tr_i+1-10^{-18})$ will die.</p><p>To save the person on the street, AquaMoon can stop time at any moment $t$, and then move the person from his current coordinate $x$ to any coordinate $y$ ($t$, $x$ and $y$ are not necessarily integers). The movement costs AquaMoon $|x-y|$ energy. The movement is continuous, so if there exists some cursed area between points $x$ and $y$ at time $t$, the person will <span class="tex-font-style-bf">die too</span>.</p><p>AquaMoon wants to know what is the minimum amount of energy she needs to spend in order to save the person on the street from all $n$ curses. But she is not good at programming. As her friend, can you help her?</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($1\le n\le 2 \cdot 10^5$) — the number of curses.</p><p>The next line contains a single integer $x$ ($1\le x\le 10^6$) — the initial coordinate of the person.</p><p>The following $n$ lines contain four integers $tl_i$, $tr_i$, $l_i$, $r_i$ each ($1\le tl_i\le tr_i\le 10^6$, $1\le l_i\le r_i\le 10^6$).</p></div><div class="output-specification"><p>Print a single integer — the minimum energy which AquaMoon needs to spent, rounded up to the nearest integer (in case there are two nearest integers you should round the answer to the highest of them).</p></div>

## Input

<p>The first line contains a single integer $n$ ($1\le n\le 2 \cdot 10^5$) — the number of curses.</p><p>The next line contains a single integer $x$ ($1\le x\le 10^6$) — the initial coordinate of the person.</p><p>The following $n$ lines contain four integers $tl_i$, $tr_i$, $l_i$, $r_i$ each ($1\le tl_i\le tr_i\le 10^6$, $1\le l_i\le r_i\le 10^6$).</p>

## Output

<p>Print a single integer — the minimum energy which AquaMoon needs to spent, rounded up to the nearest integer (in case there are two nearest integers you should round the answer to the highest of them).</p>





```input1
2
1
1 2 1 2
2 3 2 3
```




```input2
3
4
1 4 1 2
1 4 4 15
6 7 1 4
```




```input3
4
3
1 5 1 1
4 10 1 4
1 2 3 13
1 10 7 19
```




```input4
7
5
78 96 76 91
6 16 18 37
53 63 40 56
83 88 21 38
72 75 17 24
63 63 53 60
34 46 60 60
```




```output1
2
```




```output2
8
```




```output3
14
```




```output4
20
```


