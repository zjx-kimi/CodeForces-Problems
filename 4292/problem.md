## Description

<div><p>Recently Evlampy installed one interesting computer game, one of aspects of which is to split army into several groups and then fight with enemy's groups. Let us consider a simplified version of the battle.</p><p>In the nearest battle Evlampy should fight an enemy army that consists of $m$ groups, the $i$-th of which has $hp_i$ health points.</p><p>Evlampy's army consists of $n$ equal soldiers. Before each battle he should split his army in exactly $m$ groups (possibly, empty) so that the total size of the groups is $n$. The battle is played step-by-step. On each step each of Evlampy's groups attacks exactly one enemy group. Thus, each step is described with an array of $m$ integers $a_1, a_2, \ldots, a_m$, meaning that the $i$-th Evlampy's group attacks the $a_i$-th enemy group. Different groups can attack same group, on each step the array $a$ is chosen independently.</p><p>After each step the health points of each enemy group decreases by the total number of soldiers in Evlampy's groups that attacked this enemy group at this step. Enemy group is destroyed once its health points are zero or negative. Evlampy's soldiers do not lose health.</p><center> <img class="tex-graphics" height="231px" src="file://oA14EZrm.png" style="max-width: 100.0%;max-height: 100.0%;" width="378px"> <span class="tex-font-size-small">An example of a step. The numbers in green circles represent the number of soldiers in Evlampy's groups, the arrows represent attacks, the numbers in red circles represent health points of enemy groups, the blue numbers represent how much the health points will decrease after the step.</span> </center><p>Evlampy understands that the upcoming battle will take the whole night. He became sad because this way he won't have enough time to finish his homework. Now Evlampy wants you to write a program that will help him win in the smallest possible number of steps. Can you help him?</p><p>In other words, find the smallest number of steps needed to destroy all enemy groups and show a possible way of doing this. Find the requires splitting of the army into $m$ groups and the arrays $a$ for each step.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $m$ ($1 \leq m \leq n \leq 10^{6}$)&nbsp;— the number of soldiers in Evlampy's army and the number of groups in enemy army. $m$ is also equal to the maximum possible number of groups Evlampy can split the army to.</p><p>The second line contains $m$ integers $hp_1, hp_2, \ldots, hp_m$ ($1 \leq hp_i \leq 10^{6}$)&nbsp;— the health points of each of the enemy groups.</p><p>It is guaranteed that the sum of $hp_i$ does not exceed $10^{6}$.</p></div><div class="output-specification"><p>Print a single integer $t$&nbsp;— the minimum possible number of steps needed to win the battle.</p><p>After that print $m$ integers $s_1, s_2, \ldots, s_m$ ($s_i \ge 0$, $s_1 + s_2 + \ldots + s_m = n$), meaning that the $i$-th group of Evlampy's army should contain $s_i$ soldiers.</p><p>In each of the next $t$ lines print $m$ integers $a_1, a_2, \ldots, a_m$ ($1 \le a_i \le m$)&nbsp;— the description of one step. The integers mean that on the corresponding step the $i$-th Evlampy's group should attack the $a_i$-th enemy group. It is allowed to attack an already destroyed group.</p></div>

## Input

<p>The first line contains two integers $n$ and $m$ ($1 \leq m \leq n \leq 10^{6}$)&nbsp;— the number of soldiers in Evlampy's army and the number of groups in enemy army. $m$ is also equal to the maximum possible number of groups Evlampy can split the army to.</p><p>The second line contains $m$ integers $hp_1, hp_2, \ldots, hp_m$ ($1 \leq hp_i \leq 10^{6}$)&nbsp;— the health points of each of the enemy groups.</p><p>It is guaranteed that the sum of $hp_i$ does not exceed $10^{6}$.</p>

## Output

<p>Print a single integer $t$&nbsp;— the minimum possible number of steps needed to win the battle.</p><p>After that print $m$ integers $s_1, s_2, \ldots, s_m$ ($s_i \ge 0$, $s_1 + s_2 + \ldots + s_m = n$), meaning that the $i$-th group of Evlampy's army should contain $s_i$ soldiers.</p><p>In each of the next $t$ lines print $m$ integers $a_1, a_2, \ldots, a_m$ ($1 \le a_i \le m$)&nbsp;— the description of one step. The integers mean that on the corresponding step the $i$-th Evlampy's group should attack the $a_i$-th enemy group. It is allowed to attack an already destroyed group.</p>





```input1
13 7
6 4 3 7 2 1 5
```




```input2
6 5
3 3 3 3 3
```




```input3
7 4
1 5 9 2
```




```output1
3
0 1 2 3 1 2 4
2 6 2 4 4 2 4
3 1 7 1 7 7 1
3 1 5 3 7 5 1
```




```output2
3
3 3 0 0 0
1 2 3 4 5
3 4 5 5 5
5 5 5 5 5
```




```output3
3
1 2 4 0
1 4 2 3
2 3 3 3
3 3 3 3
```



## Note

<p>The first example is shown below.</p><center> <img class="tex-graphics" height="300px" src="file://YaeTVpdj.png" style="max-width: 100.0%;max-height: 100.0%;" width="547px"> </center>
