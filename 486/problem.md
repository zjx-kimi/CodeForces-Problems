## Description

<div><p><span class="tex-font-style-bf">This is a simple version of the problem. The only difference is that in this version $n \le 10^6$.</span></p><p>One winter morning, Rudolf was looking thoughtfully out the window, watching the falling snowflakes. He quickly noticed a certain symmetry in the configuration of the snowflakes. And like a true mathematician, Rudolf came up with a mathematical model of a snowflake.</p><p>He defined a snowflake as an undirected graph constructed according to the following rules: </p><ul> <li> Initially, the graph has only one vertex. </li><li> Then, more vertices are added to the graph. The initial vertex is connected by edges to $k$ new vertices ($k &gt; 1$). </li><li> Each vertex that is connected to only one other vertex is connected by edges to $k$ more new vertices. This step should be done <span class="tex-font-style-bf">at least once</span>. </li></ul><p>The smallest possible snowflake for $k = 4$ is shown in the figure.</p><center>  <img class="tex-graphics" src="file://hOkBtWjM.png" style="max-width: 100.0%;max-height: 100.0%;" width="360px"> </center><p>After some mathematical research, Rudolf realized that such snowflakes may not have any number of vertices. Help Rudolf check if a snowflake with $n$ vertices can exist.</p></div><div class="input-specification"><p>The first line of the input contains an integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Then follow the descriptions of the test cases.</p><p>The first line of each test case contains an integer $n$ ($1 \le n \le 10^6$) — the number of vertices for which it is necessary to check the existence of a snowflake.</p></div><div class="output-specification"><p>Output $t$ lines, each of which is the answer to the corresponding test case — "YES" if there exists such $k &gt; 1$ for which a snowflake with the given number of vertices can be constructed; "NO" otherwise.</p></div>

## Input

<p>The first line of the input contains an integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Then follow the descriptions of the test cases.</p><p>The first line of each test case contains an integer $n$ ($1 \le n \le 10^6$) — the number of vertices for which it is necessary to check the existence of a snowflake.</p>

## Output

<p>Output $t$ lines, each of which is the answer to the corresponding test case — "YES" if there exists such $k &gt; 1$ for which a snowflake with the given number of vertices can be constructed; "NO" otherwise.</p>





```input1|2,4,6,8,10
9
1
2
3
6
13
15
255
10101
1000000
```




```output1
NO
NO
NO
NO
YES
YES
YES
YES
NO
```


