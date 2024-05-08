## Description

<div><p>You are beta testing the new secret Terraria update. This update will add quests to the game!</p><p>Simply, the world map can be represented as an array of length $n$, where the $i$-th column of the world has height $a_i$.</p><p>There are $m$ quests you have to test. The $j$-th of them is represented by two integers $s_j$ and $t_j$. In this quest, you have to go from the column $s_j$ to the column $t_j$. At the start of the quest, you are appearing at the column $s_j$.</p><p>In one move, you can go from the column $x$ to the column $x-1$ or to the column $x+1$. In this version, you have Spectre Boots, which allow you to fly. Since it is a beta version, they are bugged, so they only allow you to fly when you are going up and have infinite fly duration. When you are moving from the column with the height $p$ to the column with the height $q$, then you get some amount of fall damage. If the height $p$ is greater than the height $q$, you get $p - q$ fall damage, otherwise you fly up and get $0$ damage.</p><p>For each of the given quests, determine the minimum amount of fall damage you can get during this quest.</p></div><div class="input-specification"><p>The first line of the input contains two integers $n$ and $m$ ($2 \le n \le 10^5; 1 \le m \le 10^5$)&nbsp;— the number of columns in the world and the number of quests you have to test, respectively.</p><p>The second line of the input contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$), where $a_i$ is the height of the $i$-th column of the world.</p><p>The next $m$ lines describe quests. The $j$-th of them contains two integers $s_j$ and $t_j$ ($1 \le s_j, t_j \le n; s_j \ne t_j$), which means you have to move from the column $s_j$ to the column $t_j$ during the $j$-th quest.</p><p>Note that $s_j$ can be greater than $t_j$.</p></div><div class="output-specification"><p>Print $m$ integers. The $j$-th of them should be the minimum amount of fall damage you can get during the $j$-th quest completion.</p></div>

## Input

<p>The first line of the input contains two integers $n$ and $m$ ($2 \le n \le 10^5; 1 \le m \le 10^5$)&nbsp;— the number of columns in the world and the number of quests you have to test, respectively.</p><p>The second line of the input contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$), where $a_i$ is the height of the $i$-th column of the world.</p><p>The next $m$ lines describe quests. The $j$-th of them contains two integers $s_j$ and $t_j$ ($1 \le s_j, t_j \le n; s_j \ne t_j$), which means you have to move from the column $s_j$ to the column $t_j$ during the $j$-th quest.</p><p>Note that $s_j$ can be greater than $t_j$.</p>

## Output

<p>Print $m$ integers. The $j$-th of them should be the minimum amount of fall damage you can get during the $j$-th quest completion.</p>





```input1
7 6
10 8 9 6 8 12 7
1 2
1 7
4 6
7 1
3 5
4 2
```




```output1
2
10
0
7
3
1
```


