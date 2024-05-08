## Description

<div><p>Monocarp is playing a strategy game. In the game, he recruits a squad to fight monsters. Before each battle, Monocarp has $C$ coins to spend on his squad.</p><p>Before each battle starts, his squad is empty. Monocarp chooses <span class="tex-font-style-bf">one type of units</span> and recruits no more units of that type than he can recruit with $C$ coins.</p><p>There are $n$ types of units. Every unit type has three parameters: </p><ul> <li> $c_i$&nbsp;— the cost of recruiting one unit of the $i$-th type; </li><li> $d_i$&nbsp;— the damage that one unit of the $i$-th type deals in a second; </li><li> $h_i$&nbsp;— the amount of health of one unit of the $i$-th type. </li></ul><p>Monocarp has to face $m$ monsters. Every monster has two parameters: </p><ul> <li> $D_j$&nbsp;— the damage that the $j$-th monster deals in a second; </li><li> $H_j$&nbsp;— the amount of health the $j$-th monster has. </li></ul><p>Monocarp has to fight only the $j$-th monster during the $j$-th battle. He wants all his recruited units to stay alive. Both Monocarp's squad and the monster attack continuously (not once per second) and at the same time. Thus, Monocarp wins the battle if and only if his squad kills the monster strictly faster than the monster kills one of his units. The time is compared with no rounding.</p><p>For each monster, Monocarp wants to know the minimum amount of coins he has to spend to kill that monster. If this amount is greater than $C$, then report that it's impossible to kill that monster.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $C$ ($1 \le n \le 3 \cdot 10^5$; $1 \le C \le 10^6$)&nbsp;— the number of types of units and the amount of coins Monocarp has before each battle.</p><p>The $i$-th of the next $n$ lines contains three integers $c_i, d_i$ and $h_i$ ($1 \le c_i \le C$; $1 \le d_i, h_i \le 10^6$).</p><p>The next line contains a single integer $m$ ($1 \le m \le 3 \cdot 10^5$)&nbsp;— the number of monsters that Monocarp has to face.</p><p>The $j$-th of the next $m$ lines contains two integers $D_j$ and $H_j$ ($1 \le D_j \le 10^6$; $1 \le H_j \le 10^{12}$).</p></div><div class="output-specification"><p>Print $m$ integers. For each monster, print the minimum amount of coins Monocarp has to spend to kill that monster. If this amount is greater than $C$, then print $-1$.</p></div>

## Input

<p>The first line contains two integers $n$ and $C$ ($1 \le n \le 3 \cdot 10^5$; $1 \le C \le 10^6$)&nbsp;— the number of types of units and the amount of coins Monocarp has before each battle.</p><p>The $i$-th of the next $n$ lines contains three integers $c_i, d_i$ and $h_i$ ($1 \le c_i \le C$; $1 \le d_i, h_i \le 10^6$).</p><p>The next line contains a single integer $m$ ($1 \le m \le 3 \cdot 10^5$)&nbsp;— the number of monsters that Monocarp has to face.</p><p>The $j$-th of the next $m$ lines contains two integers $D_j$ and $H_j$ ($1 \le D_j \le 10^6$; $1 \le H_j \le 10^{12}$).</p>

## Output

<p>Print $m$ integers. For each monster, print the minimum amount of coins Monocarp has to spend to kill that monster. If this amount is greater than $C$, then print $-1$.</p>





```input1
3 10
3 4 6
5 5 5
10 3 4
3
8 3
5 4
10 15
```




```input2
5 15
14 10 3
9 2 2
10 4 3
7 3 5
4 3 1
6
11 2
1 1
4 7
2 1
1 14
3 3
```




```input3
5 13
13 1 9
6 4 5
12 18 4
9 13 2
5 4 5
2
16 3
6 2
```




```output1
5 3 -1
```




```output2
14 4 14 4 7 7
```




```output3
12 5
```



## Note

<p>Consider the first monster of the first example.</p><p>Monocarp can't recruit one unit of the first type, because it will take both him and the monster $0.75$ seconds to kill each other. He can recruit two units for the cost of $6$ coins and kill the monster in $0.375$ second.</p><p>Monocarp can recruit one unit of the second type, because he kills the monster in $0.6$ seconds, and the monster kills him in $0.625$ seconds. The unit is faster. Thus, $5$ coins is enough.</p><p>Monocarp will need at least three units of the third type to kill the first monster, that will cost $30$ coins.</p><p>Monocarp will spend the least coins if he chooses the second type of units and recruits one unit of that type.</p>
