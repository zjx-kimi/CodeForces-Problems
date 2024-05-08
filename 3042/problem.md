## Description

<div><p>A competitive eater, Alice is scheduling some practices for an eating contest on a magical calendar. The calendar is unusual because a week contains not necessarily $7$ days!</p><p>In detail, she can choose any integer $k$ which satisfies $1 \leq k \leq r$, and set $k$ days as the number of days in a week.</p><p>Alice is going to paint some $n$ consecutive days on this calendar. On this calendar, dates are written from the left cell to the right cell in a week. If a date reaches the last day of a week, the next day's cell is the leftmost cell in the next (under) row.</p><p>She wants to make <span class="tex-font-style-bf">all of the painted cells to be connected by side</span>. It means, that for any two painted cells there should exist at least one sequence of painted cells, started in one of these cells, and ended in another, such that any two consecutive cells in this sequence are connected by side.</p><p>Alice is considering the shape of the painted cells. Two shapes are the same if there exists a way to make them exactly overlapped <span class="tex-font-style-bf">using only parallel moves, parallel to the calendar's sides</span>.</p><p>For example, in the picture, a week has $4$ days and Alice paints $5$ consecutive days. [1] and [2] are different shapes, but [1] and [3] are equal shapes.</p><center> <img class="tex-graphics" src="file://4MYEqJVG.png" style="max-width: 100.0%;max-height: 100.0%;">   </center><p>Alice wants to know <span class="tex-font-style-bf">how many possible shapes</span> exists <span class="tex-font-style-bf">if she set how many days a week has and choose consecutive $n$ days and paints them in calendar started in one of the days of the week</span>. As was said before, she considers only shapes, there all cells are connected by side.</p></div><div class="input-specification"><p>The input consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases. Next $t$ lines contain descriptions of test cases.</p><p>For each test case, the only line contains two integers $n$, $r$ ($1 \le n \le 10^9, 1 \le r \le 10^9$).</p></div><div class="output-specification"><p>For each test case, print a single integer &nbsp;— the answer to the problem.</p><p>Please note, that the answer for some test cases won't fit into $32$-bit integer type, so you should use at least $64$-bit integer type in your programming language.</p></div>

## Input

<p>The input consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases. Next $t$ lines contain descriptions of test cases.</p><p>For each test case, the only line contains two integers $n$, $r$ ($1 \le n \le 10^9, 1 \le r \le 10^9$).</p>

## Output

<p>For each test case, print a single integer &nbsp;— the answer to the problem.</p><p>Please note, that the answer for some test cases won't fit into $32$-bit integer type, so you should use at least $64$-bit integer type in your programming language.</p>





```input1
5
3 4
3 2
3 1
13 7
1010000 9999999
```




```output1
4
3
1
28
510049495001
```



## Note

<p>In the first test case, Alice can set $1,2,3$ or $4$ days as the number of days in a week.</p><p>There are $6$ possible paintings shown in the picture, but there are only $4$ different shapes. So, the answer is $4$. Notice that <span class="tex-font-style-bf">the last example in the picture is an invalid painting</span> because all cells are not connected by sides.</p><center> <img class="tex-graphics" src="file://zf4cy6FX.png" style="max-width: 100.0%;max-height: 100.0%;">   </center><p>In the last test case, be careful with the overflow issue, described in the output format.</p>
