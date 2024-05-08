## Description

<div><p>YunQian is standing on an infinite plane with the Cartesian coordinate system on it. In one move, she can move to the diagonally adjacent point on the top right or the adjacent point on the left.</p><p>That is, if she is standing on point $(x,y)$, she can either move to point $(x+1,y+1)$ or point $(x-1,y)$.</p><p>YunQian initially stands at point $(a,b)$ and wants to move to point $(c,d)$. Find the minimum number of moves she needs to make or declare that it is impossible.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1\le t\le 10^4$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line and only line of each test case contain four integers $a$, $b$, $c$, $d$ ($-10^8\le a,b,c,d\le 10^8$).</p></div><div class="output-specification"><p>For each test case, if it is possible to move from point $(a,b)$ to point $(c,d)$, output the minimum number of moves. Otherwise, output $-1$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1\le t\le 10^4$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line and only line of each test case contain four integers $a$, $b$, $c$, $d$ ($-10^8\le a,b,c,d\le 10^8$).</p>

## Output

<p>For each test case, if it is possible to move from point $(a,b)$ to point $(c,d)$, output the minimum number of moves. Otherwise, output $-1$.</p>





```input1|2,4,6
6
-1 0 -1 2
0 0 4 5
-2 -1 1 1
-3 2 -3 2
2 -1 -1 -1
1 1 0 2
```




```output1
4
6
-1
0
3
3
```



## Note

<p>In the first test case, one possible way using $4$ moves is $(-1,0)\to (0,1)\to (-1,1)\to (0,2)\to (-1,2)$. It can be proven that it is impossible to move from point $(-1,0)$ to point $(-1,2)$ in less than $4$ moves.</p>
