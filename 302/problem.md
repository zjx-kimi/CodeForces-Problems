## Description

<div><p>There are $n$ heroes in a videogame. Each hero has some health value $h$ and initial armor value $a$. Let the current value of armor be $a_{\mathit{cur}}$, initially equal to $a$.</p><p>When $x$ points of damage are inflicted on a hero, the following happens: if $x &lt; a_{\mathit{cur}}$, then $x$ gets subtracted from $a_{\mathit{cur}}$; otherwise, $1$ gets subtracted from $h$ and $a_{\mathit{cur}}$ gets assigned back to $a$.</p><p>In the start of the game, you choose the value $x$ (an integer strictly greater than $0$, arbitrarily large). Then you keep attacking all heroes in rounds: in one round, you inflict $x$ points of damage to all alive heroes. A hero dies when his health becomes $0$. The game ends when all heroes are dead.</p><p>The last hero to die earns the number of points, equal to the number of rounds he was the only hero alive. The other heroes get $0$ points. In particular, if the last round ends with multiple heroes dying, then every hero gets $0$ points.</p><p>The game is played for every possible $x$ (from $1$ to infinity). The points are reset between the games. What's the maximum number of points each hero has had?</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of heroes.</p><p>The second line contains $n$ integers $h_1, h_2, \dots, h_n$ ($1 \le h_i \le 2 \cdot 10^5$)&nbsp;— the health value of each hero.</p><p>The third line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 2 \cdot 10^5$)&nbsp;— the initial armor value of each hero.</p></div><div class="output-specification"><p>For each testcase, print $n$ integers&nbsp;— the maximum number of points each hero has had over the games played for every possible $x$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of heroes.</p><p>The second line contains $n$ integers $h_1, h_2, \dots, h_n$ ($1 \le h_i \le 2 \cdot 10^5$)&nbsp;— the health value of each hero.</p><p>The third line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 2 \cdot 10^5$)&nbsp;— the initial armor value of each hero.</p>

## Output

<p>For each testcase, print $n$ integers&nbsp;— the maximum number of points each hero has had over the games played for every possible $x$.</p>





```input1|2,3,4,8,9,10
3
3
3 1 2
3 11 5
1
100
200
4
5 9 5 1
9 2 9 10
```




```output1
1 1 1 
20000 
0 4 0 0
```



## Note

<p>In the first testcase, the game for $x = 1$ is played as follows: </p><ul> <li> before all rounds: the heroes have $h = [3, 1, 2]$, $a_{\mathit{cur}} = [3, 11, 5]$; </li><li> round $1$: $1$ damage is inflicted on every hero: $h$ remains $[3, 1, 2]$, $a_{\mathit{cur}}$ becomes $[2, 10, 4]$; </li><li> round $2$: $h = [3, 1, 2]$, $a_{\mathit{cur}} = [1, 9, 3]$; </li><li> round $3$: the first hero runs out of armor, so he loses a health point: $h = [2, 1, 2]$, $a_{\mathit{cur}} = [3, 8, 2]$; </li><li> ... </li><li> round $9$: the first hero dies, since his health reaches $0$: $h = [0, 1, 1]$, $a_{\mathit{cur}} = [0, 2, 1]$; </li><li> round $10$: the third hero dies: $h = [0, 1, 0]$, $a_{\mathit{cur}} = [0, 1, 0]$; </li><li> round $11$: the second hero dies: $h = [0, 0, 0]$, $a_{\mathit{cur}} = [0, 0, 0]$. </li></ul><p>The second hero was the last hero to die, and he was the only hero alive during one round. Thus, he gets $1$ point for that game.</p><p>The game for $x = 4$ is played as follows: </p><ul> <li> round $1$: $h = [2, 1, 2]$, $a_{\mathit{cur}} = [3, 7, 1]$; </li><li> round $2$: $h = [1, 1, 1]$, $a_{\mathit{cur}} = [3, 3, 5]$; </li><li> round $3$: $h = [0, 0, 1]$, $a_{\mathit{cur}} = [0, 0, 1]$; </li><li> round $4$: $h = [0, 0, 0]$, $a_{\mathit{cur}} = [0, 0, 0]$; </li></ul><p>The third hero was the last hero to die, and he was the only hero alive during one round.</p>
