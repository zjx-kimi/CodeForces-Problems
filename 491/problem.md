## Description

<div><p>There is a pool of length $l$ where $n$ swimmers plan to swim. People start swimming at the same time (at the time moment $0$), but you can assume that they take different lanes, so they don't interfere with each other.</p><p>Each person swims along the following route: they start at point $0$ and swim to point $l$ with constant speed (which is equal to $v_i$ units per second for the $i$-th swimmer). After reaching the point $l$, the swimmer instantly (in negligible time) turns back and starts swimming to the point $0$ with the same constant speed. After returning to the point $0$, the swimmer starts swimming to the point $l$, and so on.</p><p>Let's say that some <span class="tex-font-style-bf">real</span> moment of time is a <span class="tex-font-style-it">meeting moment</span> if there are <span class="tex-font-style-bf">at least two</span> swimmers that are in the same point of the pool at that moment of time (that point may be $0$ or $l$ as well as any other real point inside the pool).</p><p>The pool will be open for $t$ seconds. You have to calculate the number of meeting moments while the pool is open. Since the answer may be very large, print it modulo $10^9 + 7$.</p></div><div class="input-specification"><p>The first line contains two integers $l$ and $t$ ($1 \le l, t \le 10^9$)&nbsp;— the length of the pool and the duration of the process (in seconds).</p><p>The second line contains the single integer $n$ ($2 \le n \le 2 \cdot 10^5$)&nbsp;— the number of swimmers.</p><p>The third line contains $n$ integers $v_1, v_2, \dots, v_n$ ($1 \le v_i \le 2 \cdot 10^5$), where $v_i$ is the speed of the $i$-th swimmer. All $v_i$ are <span class="tex-font-style-bf">pairwise distinct</span>.</p></div><div class="output-specification"><p>Print one integer&nbsp;— the number of meeting moments (including moment $t$ if needed and <span class="tex-font-style-bf">excluding moment $0$</span>), taken modulo $10^9 + 7$.</p></div>

## Input

<p>The first line contains two integers $l$ and $t$ ($1 \le l, t \le 10^9$)&nbsp;— the length of the pool and the duration of the process (in seconds).</p><p>The second line contains the single integer $n$ ($2 \le n \le 2 \cdot 10^5$)&nbsp;— the number of swimmers.</p><p>The third line contains $n$ integers $v_1, v_2, \dots, v_n$ ($1 \le v_i \le 2 \cdot 10^5$), where $v_i$ is the speed of the $i$-th swimmer. All $v_i$ are <span class="tex-font-style-bf">pairwise distinct</span>.</p>

## Output

<p>Print one integer&nbsp;— the number of meeting moments (including moment $t$ if needed and <span class="tex-font-style-bf">excluding moment $0$</span>), taken modulo $10^9 + 7$.</p>





```input1
9 18
2
1 2
```




```input2
12 13
3
4 2 6
```




```input3
1 1000000000
3
100000 150000 200000
```




```output1
3
```




```output2
10
```




```output3
997200007
```



## Note

<p>In the first example, there are three meeting moments:</p><ul> <li> moment $6$, during which both swimmers are in the point $6$; </li><li> moment $12$, during which both swimmers are in the point $6$; </li><li> and moment $18$, during which both swimmers are in the point $0$. </li></ul>
