## Description

<div><p>A squad of $n$ warriors is defending a castle from a dragon attack. There are $m$ barricades between the castle and the dragon.</p><p>The warriors are numbered from $1$ to $n$. The $i$-th warrior knows $k_i$ attacks: the $j$-th of them deals $a_{i,j}$ damage to the dragon and can only be applied if there are exactly $b_{i,j}$ barricades between the castle and the dragon.</p><p>The warriors make turns one after another, starting from warrior $1$. After warrior $n$ makes his turn, the total damage to the dragon is calculated. The $i$-th warrior performs exactly one of three possible moves in his turn:</p><ol> <li> destroys one barricade (if there are any left); </li><li> deploys one of his $k_i$ attacks; </li><li> skips a turn. </li></ol><p>The total damage is the sum of damages dealt by the warriors who chose to deploy their attacks in their turn. What is the maximum total damage the warriors can deal to the dragon?</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $m$ ($1 \le n, m \le 3 \cdot 10^5$)&nbsp;— the number of warriors and the initial number of barricades.</p><p>Then the descriptions of attacks for each warrior follow. The $i$-th description consists of three lines.</p><p>The first line contains a single integer $k_i$ ($1 \le k_i \le m + 1$)&nbsp;— the number of attacks the $i$-th warrior knows.</p><p>The second line contains $k_i$ integers $a_{i,1}, a_{i,2}, \dots, a_{i,k_i}$ ($1 \le a_{i,j} \le 10^9$)&nbsp;— the damage of each attack.</p><p>The third line contains $k_i$ integers $b_{i,1}, b_{i,2}, \dots, b_{i,k_i}$ ($0 \le b_{i,j} \le m$)&nbsp;— the required number of barricades for each attack. $b_{i,j}$ for the $i$-th warrior are pairwise distinct. The attacks are listed in the increasing order of the barricades requirement, so $b_{i,1} &lt; b_{i,2} &lt; \dots &lt; b_{i,k_i}$.</p><p>The sum of $k_i$ over all warriors doesn't exceed $3 \cdot 10^5$.</p></div><div class="output-specification"><p>Print a single integer&nbsp;— the maximum total damage the warriors can deal to the dragon.</p></div>

## Input

<p>The first line contains two integers $n$ and $m$ ($1 \le n, m \le 3 \cdot 10^5$)&nbsp;— the number of warriors and the initial number of barricades.</p><p>Then the descriptions of attacks for each warrior follow. The $i$-th description consists of three lines.</p><p>The first line contains a single integer $k_i$ ($1 \le k_i \le m + 1$)&nbsp;— the number of attacks the $i$-th warrior knows.</p><p>The second line contains $k_i$ integers $a_{i,1}, a_{i,2}, \dots, a_{i,k_i}$ ($1 \le a_{i,j} \le 10^9$)&nbsp;— the damage of each attack.</p><p>The third line contains $k_i$ integers $b_{i,1}, b_{i,2}, \dots, b_{i,k_i}$ ($0 \le b_{i,j} \le m$)&nbsp;— the required number of barricades for each attack. $b_{i,j}$ for the $i$-th warrior are pairwise distinct. The attacks are listed in the increasing order of the barricades requirement, so $b_{i,1} &lt; b_{i,2} &lt; \dots &lt; b_{i,k_i}$.</p><p>The sum of $k_i$ over all warriors doesn't exceed $3 \cdot 10^5$.</p>

## Output

<p>Print a single integer&nbsp;— the maximum total damage the warriors can deal to the dragon.</p>





```input1
2 4
1
2
4
2
10 5
3 4
```




```input2
3 3
1
1
0
1
20
2
1
100
3
```




```input3
2 1
2
10 10
0 1
2
30 20
0 1
```




```output1
10
```




```output2
100
```




```output3
30
```



## Note

<p>In the first example, the optimal choice is the following: </p><ul> <li> warrior $1$ destroys a barricade, now there are $3$ barricades left; </li><li> warrior $2$ deploys his first attack (he can do it because $b_{1,1}=3$, which is the current number of barricades). </li></ul><p>The total damage is $10$.</p><p>If the first warrior used his attack or skipped his turn, then the second warrior would only be able to deploy his second attack. Thus, the total damage would be $2+5=7$ or $5$.</p><p>In the second example, the first warrior skips his move, the second warrior skips his move and the third warrior deploys his only attack.</p><p>In the third example, two equivalent options are: </p><ul> <li> both warriors deploy their second attacks; </li><li> the first warrior destroys one barricade and the second warrior deploys his first attack. </li></ul><p>Both options yield $30$ total damage.</p>
