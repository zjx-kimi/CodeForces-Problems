## Description

<div><p>After the first successful edition, Gabriella has been asked to organize a second wine tasting event. There will be $2n - 1$ bottles of wine arranged in a row, each of which is either red wine or white wine.</p><p>This time, Gabriella has already chosen the type and order of all the bottles. The types of the wines are represented by a string $s$ of length $2n - 1$. For each $1 \le i \le 2n - 1$, it holds that $s_i = \texttt{R}$ if the $i$-th bottle is red wine, and $s_i = \texttt{W}$ if the $i$-th bottle is white wine.</p><p>Exactly $n$ critics have been invited to attend. The critics are numbered from $1$ to $n$. Just like last year, each critic $j$ wants to taste an interval of wines, that is, the bottles at positions $a_j, \, a_j + 1, \, \dots, \, b_j$ for some $1 \le a_j \le b_j \le 2n - 1$. Moreover, they have the following additional requirements:</p><ul> <li> each of them wants to taste at least $n$ wines, that is, it must hold that $b_j - a_j + 1 \ge n$; </li><li> no two critics must taste exactly the same wines, that is, if $j \ne k$ it must hold that $a_j \ne a_k$ or $b_j \ne b_k$. </li></ul><p>Gabriella knows that, since the event is held in a coastal region of Italy, critics are especially interested in the white wines, and don't care much about the red ones. (Indeed, white wine is perfect to accompany seafood.) Thus, to ensure fairness, she would like that all critics taste the same number of white wines.</p><p>Help Gabriella find an integer $x$ (with $0 \le x \le 2n - 1$) such that there exists a valid assignment of intervals to critics where each critic tastes exactly $x$ white wines. It can be proved that at least one such $x$ always exists.</p></div><div class="input-specification"><p>The first line contains the integer $n$ ($1 \le n \le 10^6$) — where $2n - 1$ is the number of bottles, and $n$ is the number of critics.</p><p>The second line contains a string $s$ of length $2n - 1$ that represents the arrangement of the wines — the $i$-th character of $s$ ($1 \le i \le 2n - 1$) is $\texttt{R}$ for a red wine and $\texttt{W}$ for a white wine.</p></div><div class="output-specification"><p>Print an integer $x$ — the number of white wines that each critic will taste.</p><p>It can be proved that at least one solution exists. If multiple solutions exist, any of them will be accepted.</p></div>

## Input

<p>The first line contains the integer $n$ ($1 \le n \le 10^6$) — where $2n - 1$ is the number of bottles, and $n$ is the number of critics.</p><p>The second line contains a string $s$ of length $2n - 1$ that represents the arrangement of the wines — the $i$-th character of $s$ ($1 \le i \le 2n - 1$) is $\texttt{R}$ for a red wine and $\texttt{W}$ for a white wine.</p>

## Output

<p>Print an integer $x$ — the number of white wines that each critic will taste.</p><p>It can be proved that at least one solution exists. If multiple solutions exist, any of them will be accepted.</p>





```input1
5
RWWRRRWWW
```




```input2
1
R
```




```output1
2
```




```output2
0
```



## Note

<p>In the <span class="tex-font-style-bf">first sample</span>, there are $5$ critics and $2 \cdot 5 - 1 = 9$ bottles of wine. A possible set of intervals that makes each critic taste $2$ white wines is the following: $[2, 6],$ $[1, 6],$ $[4, 8],$ $[1, 5],$ $[3, 7]$. Note that all intervals contain at least $5$ bottles.</p><p>In the <span class="tex-font-style-bf">second sample</span>, there is $1$ critic and $2 \cdot 1 - 1 = 1$ bottle of wine. The only possible interval is $[1, 1]$, which gives $x = 0$.</p>
