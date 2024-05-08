## Description

<div><p>Since astronauts from BubbleCup XI mission finished their mission on the Moon and are big fans of famous singer, they decided to spend some fun time before returning to the Earth and hence created a so called "Moonwalk challenge" game.</p><p>Teams of astronauts are given the map of craters on the Moon and direct bidirectional paths from some craters to others that are safe for "Moonwalking". Each of those direct paths is colored in one color and there is unique path between each two craters. Goal of the game is to find two craters such that given array of colors appears most times as continuous subarray on the path between those two craters (overlapping appearances should be counted).</p><p>To help your favorite team win, you should make a program that, given the map, answers the queries of the following type: For two craters and array of colors answer how many times given array appears as continuous subarray on the path from the first crater to the second.</p><p>Colors are represented as lowercase English alphabet letters.</p></div><div class="input-specification"><p>In the first line, integer $N$ $(2 \leq N \leq 10^5)$ — number of craters on the Moon. Craters are numerated with numbers $1$ to $N$.</p><p>In next $N-1$ lines, three values $u, v, L$ $(1 \leq u, v \leq N, L \in \{a, ..., z\})$ — denoting that there is a direct path with color $L$ between craters $u$ and $v$.</p><p>Next line contains integer $Q$ $(1 \leq Q \leq 10^5)$ — number of queries.</p><p>Next $Q$ lines contain three values $u, v$ $(1 \leq u, v \leq N)$ and $S$ $(|S| \leq 100)$, where $u$ and $v$ are the two cratersfor which you should find how many times array of colors $S$ (represented as string) appears on the path from $u$ to $v$. </p></div><div class="output-specification"><p>For each query output one number that represents number of occurrences of array S on the path from $u$ to $v$.</p></div>

## Input

<p>In the first line, integer $N$ $(2 \leq N \leq 10^5)$ — number of craters on the Moon. Craters are numerated with numbers $1$ to $N$.</p><p>In next $N-1$ lines, three values $u, v, L$ $(1 \leq u, v \leq N, L \in \{a, ..., z\})$ — denoting that there is a direct path with color $L$ between craters $u$ and $v$.</p><p>Next line contains integer $Q$ $(1 \leq Q \leq 10^5)$ — number of queries.</p><p>Next $Q$ lines contain three values $u, v$ $(1 \leq u, v \leq N)$ and $S$ $(|S| \leq 100)$, where $u$ and $v$ are the two cratersfor which you should find how many times array of colors $S$ (represented as string) appears on the path from $u$ to $v$. </p>

## Output

<p>For each query output one number that represents number of occurrences of array S on the path from $u$ to $v$.</p>





```input1
6
2 3 g
3 4 n
5 3 o
6 1 n
1 2 d
7
1 6 n
6 4 dg
6 4 n
2 5 og
1 2 d
6 5 go
2 3 g

```




```output1
1
1
2
0
1
1
1

```


