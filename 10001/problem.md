## Description

<div><p>Vladislav has a son who really wanted to go to MIT. The college dormitory at MIT (Moldova Institute of Technology) can be represented as a tree with $n$ vertices, each vertex being a room with exactly one student. A <span class="tex-font-style-it">tree</span> is a connected undirected graph with $n$ vertices and $n-1$ edges.</p><p>Tonight, there are three types of students: </p><ul> <li> students who want to party and play music (marked with $\texttt{P}$), </li><li> students who wish to sleep and enjoy silence (marked with $\texttt{S}$), and </li><li> students who don't care (marked with $\texttt{C}$). </li></ul><p>Initially, all the edges are <span class="tex-font-style-it">thin</span> walls which allow music to pass through, so when a partying student puts music on, it will be heard in every room. However, we can place some <span class="tex-font-style-it">thick</span> walls on any edges&nbsp;— thick walls don't allow music to pass through them.</p><p>The university wants to install some thick walls so that every partying student can play music, and no sleepy student can hear it.</p><p>Because the university lost a lot of money in a naming rights lawsuit, they ask you to find the minimum number of thick walls they will need to use.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains an integer $n$ ($2 \leq n \leq 10^5$)&nbsp;— the number of vertices in the tree.</p><p>The second line of each test case contains $n-1$ integers $a_2, \dots , a_n$ ($1 \leq a_i &lt; i$)&nbsp;— it means there is an edge between $i$ and $a_i$ in the tree.</p><p>The third line of each test case contains a string $s$ of length $n$ consisting of characters $\texttt{P}$, $\texttt{S}$, and $\texttt{C}$, denoting that student $i$ is of type $s_i$.</p><p>The sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the minimum number of thick walls needed.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains an integer $n$ ($2 \leq n \leq 10^5$)&nbsp;— the number of vertices in the tree.</p><p>The second line of each test case contains $n-1$ integers $a_2, \dots , a_n$ ($1 \leq a_i &lt; i$)&nbsp;— it means there is an edge between $i$ and $a_i$ in the tree.</p><p>The third line of each test case contains a string $s$ of length $n$ consisting of characters $\texttt{P}$, $\texttt{S}$, and $\texttt{C}$, denoting that student $i$ is of type $s_i$.</p><p>The sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the minimum number of thick walls needed.</p>





```input1|2,3,4,8,9,10
3
3
1 1
CSP
4
1 2 2
PCSS
4
1 2 2
PPSS
```




```output1
1
1
2
```



## Note

<p>In the first case, we can install one thick wall between rooms $1$ and $2$, as shown below. We cannot install $0$ walls, since then the music from room 3 will reach room 2 where a student wants to sleep, so the answer is $1$. There are other valid solutions. </p><center> <img class="tex-graphics" src="file://61P4oVXG.png" style="max-width: 100.0%;max-height: 100.0%;"> </center>
