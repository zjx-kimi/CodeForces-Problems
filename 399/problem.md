## Description

<div><p>You are playing a video game. The game has $n$ quests that need to be completed. However, the $j$-th quest can only be completed at the beginning of hour $h_j$ of a game day. The game day is $k$ hours long. The hours of each game day are numbered $0, 1, \ldots, k - 1$. After the first day ends, a new one starts, and so on.</p><p>Also, there are dependencies between the quests, that is, for some pairs $(a_i, b_i)$ the $b_i$-th quest can only be completed after the $a_i$-th quest. It is guaranteed that there are <span class="tex-font-style-bf">no circular dependencies</span>, as otherwise the game would be unbeatable and nobody would play it.</p><p>You are skilled enough to complete any number of quests in a negligible amount of time (i.&nbsp;e. you can complete any number of quests at the beginning of the same hour, even if there are dependencies between them). You want to complete all quests as fast as possible. To do this, you can complete the quests in any valid order. The completion time is equal to the difference between the time of completing the last quest and the time of completing the first quest in this order.</p><p>Find the least amount of time you need to complete the game.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1\le t\le 100\,000$). The description of the test cases follows.</p><p>The first line of each test case contains three integers $n$, $m$, and $k$ ($1\le n\le 200\,000$, $0\le m\le 200\,000$, $1\le k\le 10^9$)&nbsp;— the number of quests, the number of dependencies between them, and the number of hours in a game day, respectively.</p><p>The next line contains $n$ integers $h_1, h_2, \ldots, h_n$ ($0\le h_i &lt; k$).</p><p>The next $m$ lines describe the dependencies. The $i$-th of these lines contains two integers $a_i$ and $b_i$ ($1\le a_i &lt; b_i\le n$) meaning that quest $b_i$ can only be completed after quest $a_i$. It is guaranteed that all dependencies are pairwise distinct.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $200\,000$.</p><p>It is guaranteed that the sum of $m$ over all test cases does not exceed $200\,000$.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the minimum completion time.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1\le t\le 100\,000$). The description of the test cases follows.</p><p>The first line of each test case contains three integers $n$, $m$, and $k$ ($1\le n\le 200\,000$, $0\le m\le 200\,000$, $1\le k\le 10^9$)&nbsp;— the number of quests, the number of dependencies between them, and the number of hours in a game day, respectively.</p><p>The next line contains $n$ integers $h_1, h_2, \ldots, h_n$ ($0\le h_i &lt; k$).</p><p>The next $m$ lines describe the dependencies. The $i$-th of these lines contains two integers $a_i$ and $b_i$ ($1\le a_i &lt; b_i\le n$) meaning that quest $b_i$ can only be completed after quest $a_i$. It is guaranteed that all dependencies are pairwise distinct.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $200\,000$.</p><p>It is guaranteed that the sum of $m$ over all test cases does not exceed $200\,000$.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the minimum completion time.</p>





```input1|2,3,4,5,6,7,13,14,15,18,19
6
4 4 24
12 16 18 12
1 2
1 3
2 4
3 4
4 3 10
2 6 5 9
1 4
2 4
3 4
2 1 10
5 5
1 2
5 0 1000
8 800 555 35 35
5 0 10
3 2 5 4 7
3 2 5
4 3 2
1 2
2 3
```




```output1
24
7
0
480
5
8
```



## Note

<p>In the first test case, quests $1$ and $4$ must be completed at the beginning of the $12$-th hour of the day, but they cannot be completed during the same hour, because you also need to complete quests $2$ and $3$ between them. You can do all this in $24$ hours, though. To do so, you start at $12$ hours of the first game day by completing the first quest. At $16$ hours you complete quest $2$. At $18$ hours you complete quest $3$. Finally at $12$ hours of the second day you can complete quest $4$. The total time elapsed (from the moment you completed the first quest and the moment you completed the last) is $24$ hours.</p><p>In the third test case, you can complete the first quest and then complete the remaining quest right after. You start at $5$ hours of the first day by completing the first quest. After this the second quest becomes available, you complete it as well. The total time elapsed is $0$.</p><p>In the fourth test case, you can start with the third quest. You start at $555$ hours of the first day and you can finish at $35$ hours of the second day. The total time elapsed is $1035-555=480$.</p>
