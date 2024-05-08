## Description

<div><p>One of the days of the hike coincided with a holiday, so in the evening at the camp, it was decided to arrange a festive fireworks display. For this purpose, the organizers of the hike bought two installations for launching fireworks and a huge number of shells for launching.</p><p>Both installations are turned on simultaneously. The first installation launches fireworks every $a$ minutes (i.e., after $a, 2 \cdot a, 3 \cdot a, \dots$ minutes after launch). The second installation launches fireworks every $b$ minutes (i.e., after $b, 2 \cdot b, 3 \cdot b, \dots$ minutes after launch).</p><p>Each firework is visible in the sky for $m + 1$ minutes after launch, i.e., if a firework was launched after $x$ minutes after the installations were turned on, it will be visible every minute from $x$ to $x + m$, inclusive. If one firework was launched $m$ minutes after another, both fireworks will be visible for one minute.</p><p>What is the maximum number of fireworks that could be seen in the sky at the same time?</p></div><div class="input-specification"><p>Each test consists of several test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then follow the descriptions of the test cases.</p><p>The first and only line of each test case contains integers $a$, $b$, $m$ ($1 \le a, b, m \le 10^{18}$)&nbsp;— the frequency of launching for the first installation, the second installation, and the time the firework is visible in the sky.</p></div><div class="output-specification"><p>For each set of input data, output a single number&nbsp;— the maximum number of fireworks that can be seen simultaneously.</p></div>

## Input

<p>Each test consists of several test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then follow the descriptions of the test cases.</p><p>The first and only line of each test case contains integers $a$, $b$, $m$ ($1 \le a, b, m \le 10^{18}$)&nbsp;— the frequency of launching for the first installation, the second installation, and the time the firework is visible in the sky.</p>

## Output

<p>For each set of input data, output a single number&nbsp;— the maximum number of fireworks that can be seen simultaneously.</p>





```input1|2,4,6
6
6 7 4
3 4 10
7 8 56
5 6 78123459896
1 1 1
1 1 1000000000000000000
```




```output1
2
7
17
28645268630
4
2000000000000000002
```



## Note

<p>In the first set of input data, the fireworks are visible in the sky for $5$ minutes. Since the first installation launches fireworks every $6$ minutes, and the second one every $7$ minutes, two fireworks launched from the same installation will not be visible in the sky at the same time. At the same time, after $7$ minutes from the start of the holiday, one firework from the first and one from the second camp will be visible. Thus, it is possible to see no more than $2$ fireworks simultaneously.</p><p>In the third set of input data, $17$ fireworks will be visible after $112$ minutes: </p><ul> <li> $9$ fireworks launched from the first installation at times [$56, 63, 70, 77, 84, 91, 98, 105, 112$]; </li><li> $8$ fireworks launched from the second installation at times [$56, 64, 72, 80, 88, 96, 104, 112$]. </li></ul>
