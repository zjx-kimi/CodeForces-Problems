## Description

<div><p>There are $n$ railway stations in Berland. They are connected to each other by $n-1$ railway sections. The railway network is connected, i.e. can be represented as an undirected tree.</p><p>You have a map of that network, so for each railway section you know which stations it connects.</p><p>Each of the $n-1$ sections has some integer value of the <span class="tex-font-style-it">scenery beauty</span>. However, these values are not marked on the map and you don't know them. All these values are from $1$ to $10^6$ inclusive.</p><p>You asked $m$ passengers some questions: the $j$-th one told you three values:</p><ul> <li> his departure station $a_j$; </li><li> his arrival station $b_j$; </li><li> minimum scenery beauty along the path from $a_j$ to $b_j$ (the train is moving along the shortest path from $a_j$ to $b_j$). </li></ul><p>You are planning to update the map and set some value $f_i$ on each railway section — the <span class="tex-font-style-it">scenery beauty</span>. The passengers' answers should be consistent with these values.</p><p>Print any valid set of values $f_1, f_2, \dots, f_{n-1}$, which the passengers' answer is consistent with or report that it doesn't exist.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($2 \le n \le 5000$) — the number of railway stations in Berland.</p><p>The next $n-1$ lines contain descriptions of the railway sections: the $i$-th section description is two integers $x_i$ and $y_i$ ($1 \le x_i, y_i \le n, x_i \ne y_i$), where $x_i$ and $y_i$ are the indices of the stations which are connected by the $i$-th railway section. All the railway sections are bidirected. Each station can be reached from any other station by the railway.</p><p>The next line contains a single integer $m$ ($1 \le m \le 5000$) — the number of passengers which were asked questions. Then $m$ lines follow, the $j$-th line contains three integers $a_j$, $b_j$ and $g_j$ ($1 \le a_j, b_j \le n$; $a_j \ne b_j$; $1 \le g_j \le 10^6$) — the departure station, the arrival station and the minimum scenery beauty along his path.</p></div><div class="output-specification"><p>If there is no answer then print a single integer <span class="tex-font-style-tt">-1</span>.</p><p>Otherwise, print $n-1$ integers $f_1, f_2, \dots, f_{n-1}$ ($1 \le f_i \le 10^6$), where $f_i$ is some valid scenery beauty along the $i$-th railway section.</p><p>If there are multiple answers, you can print any of them.</p></div>

## Input

<p>The first line contains a single integer $n$ ($2 \le n \le 5000$) — the number of railway stations in Berland.</p><p>The next $n-1$ lines contain descriptions of the railway sections: the $i$-th section description is two integers $x_i$ and $y_i$ ($1 \le x_i, y_i \le n, x_i \ne y_i$), where $x_i$ and $y_i$ are the indices of the stations which are connected by the $i$-th railway section. All the railway sections are bidirected. Each station can be reached from any other station by the railway.</p><p>The next line contains a single integer $m$ ($1 \le m \le 5000$) — the number of passengers which were asked questions. Then $m$ lines follow, the $j$-th line contains three integers $a_j$, $b_j$ and $g_j$ ($1 \le a_j, b_j \le n$; $a_j \ne b_j$; $1 \le g_j \le 10^6$) — the departure station, the arrival station and the minimum scenery beauty along his path.</p>

## Output

<p>If there is no answer then print a single integer <span class="tex-font-style-tt">-1</span>.</p><p>Otherwise, print $n-1$ integers $f_1, f_2, \dots, f_{n-1}$ ($1 \le f_i \le 10^6$), where $f_i$ is some valid scenery beauty along the $i$-th railway section.</p><p>If there are multiple answers, you can print any of them.</p>





```input1
4
1 2
3 2
3 4
2
1 2 5
1 3 3
```




```input2
6
1 2
1 6
3 1
1 5
4 1
4
6 1 3
3 4 1
6 5 2
1 2 5
```




```input3
6
1 2
1 6
3 1
1 5
4 1
4
6 1 1
3 4 3
6 5 3
1 2 4
```




```output1
5 3 5
```




```output2
5 3 1 2 1
```




```output3
-1
```


