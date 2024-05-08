## Description

<div><p>Dalaran is a flying city of magic. It consists of $n$ floating islands connected by $m$ bridges (each bridge can be traversed in both directions). Every island is reachable from every other along these bridges. It would be a shame if some magic experiment went horribly wrong and this magnificent city got destroyed, right?</p><p>Well, just guess what happened. A portal to demons' realm was opened at the island $1$. This is the start of day $1$ of the catastrophe, and all $k$ mages have gathered at the island $1$ (they were trying to close the portal, but found out that it was impossible). At the start of day $2$, a gigantic horde of demons will emerge from the portal, capture the island $1$ and kill every mage staying at that island. During each day $i$, if the island $v$ was captured by demons by the start of the day, the horde of demons will travel across all bridges connected <span class="tex-font-style-bf">directly to $v$</span>, capture every island they reach, and kill every mage they meet along the way.</p><p>Each bridge contains exactly one magic stone. Each mage at the start of the day can do one of the following actions:</p><ul> <li> Spend one day travelling along one of the bridges connected to the island where the mage currently is. When passing through a bridge, the mage can pick up the magic stone from it (if there is any; each magic stone can be picked up by at most one mage). If the bridge is passed by the demons during the same day, or by the start of the next day, the island where the mage goes is already captured by the demonic horde (even if they arrive there at the same moment), the mage is killed. </li><li> Perform a teleportation ritual to get to safety outside Dalaran. This ritual consumes two magic stones (and cannot be performed if the mage has less than two stones). </li></ul><p>Each magic stone decays in $2$ days, so if is picked up in the middle of day $i$, it decays in the middle of day $i + 2$. Decayed stones cannot be used in teleportation ritual.</p><p>Calculate the maximum number of mages that can get to safety.</p></div><div class="input-specification"><p>The first line contains three integers $n$, $m$ and $k$ ($2 \le n \le 10^5$; $n - 1 \le m \le 10^5$; $1 \le k \le 10^5$) — the number of islands, the number of bridges and the number of mages.</p><p>Then $m$ lines follow, the $i$-th line contains two integers $x_i$ and $y_i$ ($1 \le x_i, y_i \le n$; $x_i \ne y_i$) denoting a bridge between the islands $x_i$ and $y_i$.</p><p>Each pair of islands has at most one bridge connecting them. Every island is reachable from every other island along the bridges.</p></div><div class="output-specification"><p>Print one integer — the maximum number of mages that can get to safety.</p></div>

## Input

<p>The first line contains three integers $n$, $m$ and $k$ ($2 \le n \le 10^5$; $n - 1 \le m \le 10^5$; $1 \le k \le 10^5$) — the number of islands, the number of bridges and the number of mages.</p><p>Then $m$ lines follow, the $i$-th line contains two integers $x_i$ and $y_i$ ($1 \le x_i, y_i \le n$; $x_i \ne y_i$) denoting a bridge between the islands $x_i$ and $y_i$.</p><p>Each pair of islands has at most one bridge connecting them. Every island is reachable from every other island along the bridges.</p>

## Output

<p>Print one integer — the maximum number of mages that can get to safety.</p>





```input1
4 4 1
1 2
2 3
3 4
4 1
```




```input2
4 4 4
1 2
2 3
3 4
4 1
```




```input3
3 2 10
1 2
2 3
```




```input4
4 5 1
1 2
2 3
3 4
4 1
3 1
```




```output1
1
```




```output2
2
```




```output3
1
```




```output4
0
```


