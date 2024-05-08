## Description

<div><p>Tema loves cinnabon rolls — buns with cinnabon and chocolate in the shape of a "snail".</p><p>Cinnabon rolls come in different sizes and are square when viewed from above. The most delicious part of a roll is the chocolate, which is poured in a thin layer over the cinnabon roll in the form of a spiral and around the bun, as in the following picture:</p><center> <img class="tex-graphics" src="file://GMDraCRS.png" style="max-width: 100.0%;max-height: 100.0%;"><p> <span class="tex-font-size-small">Cinnabon rolls of sizes 4, 5, 6</span> </p></center><p>For a cinnabon roll of size $n$, the length of the outer side of the square is $n$, and the length of the shortest vertical chocolate segment in the central part is one.</p><p>Formally, the bun consists of two dough spirals separated by chocolate. A cinnabon roll of size $n + 1$ is obtained from a cinnabon roll of size $n$ by wrapping each of the dough spirals around the cinnabon roll for another layer.</p><p><span class="tex-font-style-bf">It is important that a cinnabon roll of size $n$ is defined in a unique way.</span></p><p>Tema is interested in how much chocolate is in his cinnabon roll of size $n$. Since Tema has long stopped buying small cinnabon rolls, it is guaranteed that $n \ge 4$.</p><p>Answer this non-obvious question by calculating the total length of the chocolate layer.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^5$)&nbsp;— the number of test cases.</p><p>The following $t$ lines describe the test cases.</p><p>Each test case is described by a single integer $n$ ($4 \le n \le 10^9$)&nbsp;— the size of the cinnabon roll.</p></div><div class="output-specification"><p>Output $t$ integers. The $i$-th of them should be equal to the total length of the chocolate layer in the $i$-th test case.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^5$)&nbsp;— the number of test cases.</p><p>The following $t$ lines describe the test cases.</p><p>Each test case is described by a single integer $n$ ($4 \le n \le 10^9$)&nbsp;— the size of the cinnabon roll.</p>

## Output

<p>Output $t$ integers. The $i$-th of them should be equal to the total length of the chocolate layer in the $i$-th test case.</p>





```input1|2,4
4
4
5
6
179179179
```




```output1
26
37
50
32105178545472401
```


