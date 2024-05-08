## Description

<div><p>You are given $n$ circles on the plane. The $i$-th of these circles is given by a tuple of integers $(x_i, y_i, r_i)$, where $(x_i, y_i)$ are the coordinates of its center, and $r_i$ is the radius of the circle.</p><p>Please find a circle $C$ which meets the following conditions:</p><ul> <li> $C$ is contained inside all $n$ circles given in the input. </li><li> Among all circles $C$ that meet the first condition, the radius of the circle is maximum. </li></ul><p>Let the largest suitable circle have the radius of $a$.</p><p>Your output $C$, described as $(x,y,r)$, will be accepted if it meets the following conditions:</p><ul> <li> For each $i$, $\sqrt{(x_i-x)^2+(y_i-y)^2}+ r \le r_i+\max(a,1)\cdot 10^{-7}$. </li><li> The absolute or relative error of $r$ does not exceed $10^{-7}$. Formally, your answer is accepted if and only if $\frac{\left|r - a\right|}{\max(1, a)} \le 10^{-7}$. </li></ul></div><div class="input-specification"><p>The first line contains a single integer $n$ ($1 \le n \le 10^5$)&nbsp;— the number of circles.</p><p>The $i$-th of the following $n$ lines contains three integers $x_i$, $y_i$, $r_i$ ($-10^6 \le x_i,y_i \le 10^6$, $1 \le r_i \le 2 \cdot 10^6$).</p><p>It is guaranteed that there is a circle with a radius of at least $10^{-6}$ which is contained inside all $n$ circles.</p></div><div class="output-specification"><p>Output three real values, $x$, $y$, and $r$&nbsp;— the coordinates of the center and the radius of the circle.</p></div>

## Input

<p>The first line contains a single integer $n$ ($1 \le n \le 10^5$)&nbsp;— the number of circles.</p><p>The $i$-th of the following $n$ lines contains three integers $x_i$, $y_i$, $r_i$ ($-10^6 \le x_i,y_i \le 10^6$, $1 \le r_i \le 2 \cdot 10^6$).</p><p>It is guaranteed that there is a circle with a radius of at least $10^{-6}$ which is contained inside all $n$ circles.</p>

## Output

<p>Output three real values, $x$, $y$, and $r$&nbsp;— the coordinates of the center and the radius of the circle.</p>





```input1
4
1 1 3
-1 1 3
1 -1 2
-1 -1 2
```




```input2
4
41580 -23621 95642
-41580 -23621 95642
0 47821 95642
0 0 109750
```




```output1
0.0000000000000000 -0.7637626158259733 0.9724747683480533
```




```output2
0.0000000000000000 0.0000000000000000 47821.0000000000000000
```



## Note

<p>A two-dimensional plot depicting the first test case is given below. The output circle $C$ is dashed with blue lines.</p><center> <img class="tex-graphics" src="file://J1UMy7am.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>A two-dimensional plot depicting the second test case is given below. The output circle $C$ is dashed with blue lines.</p><center> <img class="tex-graphics" src="file://kc3CE96W.png" style="max-width: 100.0%;max-height: 100.0%;"> </center>
