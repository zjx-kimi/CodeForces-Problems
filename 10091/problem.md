## Description

<div><p>You are given $n$ disks in the plane. The center of each disk has integer coordinates, and the radius of each disk is a positive integer. No two disks overlap in a region of positive area, but it is possible for disks to be tangent to each other.</p><p>Your task is to determine whether it is possible to change the radii of the disks in such a way that: </p><ul> <li> Disks that were tangent to each other remain tangent to each other. </li><li> No two disks overlap in a region of positive area. </li><li> The sum of all radii strictly decreases. </li></ul> The new radii are allowed to be arbitrary positive real numbers. The centers of the disks cannot be changed.</div><div class="input-specification"><p>The first line contains an integer $n$ ($1\le n \le 1000$) — the number of disks.</p><p>The next $n$ lines contain three integers each. The $i$-th of such lines contains $x_i$, $y_i$ ($-10^9 \leq x_i, y_i \leq 10^9$), and $r_i$ ($1 \leq r_i \leq 10^9$) — the coordinates of the center, and the radius, of the $i$-th disk.</p></div><div class="output-specification"><p>Print $\texttt{YES}$ if it is possible to change the radii in the desired manner. Otherwise, print $\texttt{NO}$.</p></div>

## Input

<p>The first line contains an integer $n$ ($1\le n \le 1000$) — the number of disks.</p><p>The next $n$ lines contain three integers each. The $i$-th of such lines contains $x_i$, $y_i$ ($-10^9 \leq x_i, y_i \leq 10^9$), and $r_i$ ($1 \leq r_i \leq 10^9$) — the coordinates of the center, and the radius, of the $i$-th disk.</p>

## Output

<p>Print $\texttt{YES}$ if it is possible to change the radii in the desired manner. Otherwise, print $\texttt{NO}$.</p>





```input1|
5
0 2 1
0 0 1
4 -3 4
11 0 3
11 5 2
```




```input2|
4
2 2 2
7 2 3
7 7 2
2 7 3
```




```output1
YES
```




```output2
NO
```



## Note

<p>In the <span class="tex-font-style-bf">first sample</span>, one can decrease the radii of the first and third disk by $0.5$, and increase the radius of the second disk by $0.5$. This way, the sum of all radii decreases by $0.5$. The situation before and after changing the radii is depicted below.</p><center> <img class="tex-graphics" height="302px" src="file://Dn3klWgj.png" style="max-width: 100.0%;max-height: 100.0%;"> <span class="tex-font-size-small">First sample (left) and a valid way to change the radii of the disks (right).</span> </center><p>In the <span class="tex-font-style-bf">second sample</span>, depicted below, there is no way to change the radii of the disks in the desired manner.</p><center> <img class="tex-graphics" height="302px" src="file://zuWEXph9.png" style="max-width: 100.0%;max-height: 100.0%;">  <span class="tex-font-size-small">Second sample.</span> </center>
