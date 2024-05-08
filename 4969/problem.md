## Description

<div><p>The Government of Mars is not only interested in optimizing space flights, but also wants to improve the road system of the planet.</p><p>One of the most important highways of Mars connects Olymp City and Kstolop, the capital of Cydonia. In this problem, we only consider the way from Kstolop to Olymp City, but not the reverse path (i.&nbsp;e. the path from Olymp City to Kstolop).</p><p>The road from Kstolop to Olymp City is $\ell$ kilometers long. Each point of the road has a coordinate $x$ ($0 \le x \le \ell$), which is equal to the distance from Kstolop in kilometers. So, Kstolop is located in the point with coordinate $0$, and Olymp City is located in the point with coordinate $\ell$.</p><p>There are $n$ signs along the road, $i$-th of which sets a speed limit $a_i$. This limit means that the next kilometer must be passed in $a_i$ minutes and is active until you encounter the next along the road. There is a road sign at the start of the road (i.&nbsp;e. in the point with coordinate $0$), which sets the initial speed limit.</p><p>If you know the location of all the signs, it's not hard to calculate how much time it takes to drive from Kstolop to Olymp City. Consider an example:</p><center> <img class="tex-graphics" src="file://7M3Dci7P.png" style="max-width: 100.0%;max-height: 100.0%;" width="756px"> </center><p>Here, you need to drive the first three kilometers in five minutes each, then one kilometer in eight minutes, then four kilometers in three minutes each, and finally the last two kilometers must be passed in six minutes each. Total time is $3\cdot 5 + 1\cdot 8 + 4\cdot 3 + 2\cdot 6 = 47$ minutes.</p><p>To optimize the road traffic, the Government of Mars decided to remove no more than $k$ road signs. It cannot remove the sign at the start of the road, otherwise, there will be no limit at the start. By removing these signs, the Government also wants to make the time needed to drive from Kstolop to Olymp City as small as possible.</p><p>The largest industrial enterprises are located in Cydonia, so it's the priority task to optimize the road traffic from Olymp City. So, the Government of Mars wants you to remove the signs in the way described above.</p></div><div class="input-specification"><p>The first line contains three integers $n$, $\ell$, $k$ ($1 \le n \le 500$, $1 \le \ell \le 10^5$, $0 \le k \le n-1$), the amount of signs on the road, the distance between the cities and the maximal number of signs you may remove.</p><p>The second line contains $n$ integers $d_i$ ($d_1 = 0$, $d_i &lt; d_{i+1}$, $0 \le d_i \le \ell - 1$) — coordinates of all signs.</p><p>The third line contains $n$ integers $a_i$ ($1 \le a_i \le 10^4$) — speed limits.</p></div><div class="output-specification"><p>Print a single integer — minimal possible time to drive from Kstolop to Olymp City in minutes, if you remove no more than $k$ road signs.</p></div>

## Input

<p>The first line contains three integers $n$, $\ell$, $k$ ($1 \le n \le 500$, $1 \le \ell \le 10^5$, $0 \le k \le n-1$), the amount of signs on the road, the distance between the cities and the maximal number of signs you may remove.</p><p>The second line contains $n$ integers $d_i$ ($d_1 = 0$, $d_i &lt; d_{i+1}$, $0 \le d_i \le \ell - 1$) — coordinates of all signs.</p><p>The third line contains $n$ integers $a_i$ ($1 \le a_i \le 10^4$) — speed limits.</p>

## Output

<p>Print a single integer — minimal possible time to drive from Kstolop to Olymp City in minutes, if you remove no more than $k$ road signs.</p>





```input1
4 10 0
0 3 4 8
5 8 3 6
```




```input2
4 10 2
0 3 4 8
5 8 3 6
```




```output1
47
```




```output2
38
```



## Note

<p>In the first example, you cannot remove the signs. So the answer is $47$, as it's said in the statements above.</p><p>In the second example, you may remove the second and the fourth sign. In this case, you need to drive four kilometers in $4\cdot5 = 20$ minutes, and then six kilometers in $6\cdot3 = 18$, so the total time is $4\cdot5 + 6\cdot3 = 38$ minutes.</p>
