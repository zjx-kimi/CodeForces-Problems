## Description

<div><p>There is a game where you need to move through a labyrinth. The labyrinth consists of $n$ platforms, connected by $m$ passages. </p><p>Each platform is at some level $l_i$, an integer number from $0$ to $H - 1$. In a single step, if you are currently on platform $i$, you can stay on it, or move to another platform $j$. To move to platform $j$ they have to be connected by the passage, and their levels have to be the same, namely $l_i = l_j$.</p><p>After each step, the levels of all platforms change. The new level of platform $i$ is calculated as $l'_i = (l_i + s_i) \bmod H$, for all $i$. </p><p>You start on platform $1$. Find the minimum number of steps you need to get to platform $n$.</p></div><div class="input-specification"><p>The first line of input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then the descriptions of the test cases follow.</p><p>The first line of each test case contains three integers $n$, $m$, and $H$ ($2 \le n \le 10^5$, $1 \le m \le 10^5$, $1 \le H \le 10^9$).</p><p>The second line contains $n$ integers $l_i$, the initial level of each platform ($0 \le l_i \le H-1$). </p><p>The third line contains $n$ integers $s_i$, the change of level for each platform ($0 \le s_i \le H-1$).</p><p>Next $m$ lines contain a description of the passages. Each passage is described as a pair of integers&nbsp;— the platforms, connected by the passage. There is at most one passage connecting each pair of platforms, and there is no passage connecting a platform to itself.</p><p>The sum of $n$ for all tests does not exceed $10^5$, the sum of $m$ for all tests does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, print a single integer, the minimum number of steps needed to get from platform $1$ to platform $n$.</p><p>If it is impossible to get to platform $n$, print $-1$.</p></div>

## Input

<p>The first line of input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then the descriptions of the test cases follow.</p><p>The first line of each test case contains three integers $n$, $m$, and $H$ ($2 \le n \le 10^5$, $1 \le m \le 10^5$, $1 \le H \le 10^9$).</p><p>The second line contains $n$ integers $l_i$, the initial level of each platform ($0 \le l_i \le H-1$). </p><p>The third line contains $n$ integers $s_i$, the change of level for each platform ($0 \le s_i \le H-1$).</p><p>Next $m$ lines contain a description of the passages. Each passage is described as a pair of integers&nbsp;— the platforms, connected by the passage. There is at most one passage connecting each pair of platforms, and there is no passage connecting a platform to itself.</p><p>The sum of $n$ for all tests does not exceed $10^5$, the sum of $m$ for all tests does not exceed $10^5$.</p>

## Output

<p>For each test case, print a single integer, the minimum number of steps needed to get from platform $1$ to platform $n$.</p><p>If it is impossible to get to platform $n$, print $-1$.</p>





```input1|2,3,4,5,6,7,12,13,14,15,16,17,18,19,20,21
3
3 3 10
1 9 4
2 3 0
1 2
3 2
1 3
2 1 10
1 2
4 6
1 2
8 7 25
22 14 5 3 10 14 11 1
9 5 4 10 7 16 18 18
2 8
6 3
3 5
7 5
2 6
1 4
4 7
```




```output1
6
-1
52
```



## Note

<p>This is how levels of the platforms change, and what actions we need to perform in the first example.</p><p></p><table class="tex-tabular"><tbody><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-bottom"></td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-bottom"><span class="tex-font-style-bf">Platform 1</span></td><td class="tex-tabular-text-align-center tex-tabular-border-bottom"><span class="tex-font-style-bf">Platform 2</span></td><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-bottom"><span class="tex-font-style-bf">Platform 3</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-bottom"><span class="tex-font-style-bf">Action</span></td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top"><span class="tex-font-style-bf">Step 1</span></td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-top">1</td><td class="tex-tabular-text-align-center tex-tabular-border-top">9</td><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top">4</td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-top">Stay on the platform 1</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right"><span class="tex-font-style-bf">Step 2</span></td><td class="tex-tabular-border-left tex-tabular-text-align-center">3</td><td class="tex-tabular-text-align-center">2</td><td class="tex-tabular-text-align-center tex-tabular-border-right">4</td><td class="tex-tabular-border-left tex-tabular-text-align-left">Stay on the platform 1</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right"><span class="tex-font-style-bf">Step 3</span></td><td class="tex-tabular-border-left tex-tabular-text-align-center"><span class="tex-font-style-bf">5</span></td><td class="tex-tabular-text-align-center"><span class="tex-font-style-bf">5</span></td><td class="tex-tabular-text-align-center tex-tabular-border-right">4</td><td class="tex-tabular-border-left tex-tabular-text-align-left">Move to the platform 2</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right"><span class="tex-font-style-bf">Step 4</span></td><td class="tex-tabular-border-left tex-tabular-text-align-center">7</td><td class="tex-tabular-text-align-center">8</td><td class="tex-tabular-text-align-center tex-tabular-border-right">4</td><td class="tex-tabular-border-left tex-tabular-text-align-left">Stay on the platform 2</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right"><span class="tex-font-style-bf">Step 5</span></td><td class="tex-tabular-border-left tex-tabular-text-align-center">9</td><td class="tex-tabular-text-align-center">1</td><td class="tex-tabular-text-align-center tex-tabular-border-right">4</td><td class="tex-tabular-border-left tex-tabular-text-align-left">Stay on the platform 2</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right"><span class="tex-font-style-bf">Step 6</span></td><td class="tex-tabular-border-left tex-tabular-text-align-center">1</td><td class="tex-tabular-text-align-center"><span class="tex-font-style-bf">4</span></td><td class="tex-tabular-text-align-center tex-tabular-border-right"><span class="tex-font-style-bf">4</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left">Move to the platform 3</td></tr></tbody></table><p></p>
