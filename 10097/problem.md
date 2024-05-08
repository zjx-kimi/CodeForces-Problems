## Description

<div><p>Deep within a forest lies an ancient tree, home to $n$ ants living in $n$ tiny houses, indexed from $1$ to $n$, connected by the branches of the tree.</p><center> <img class="tex-graphics" src="file://O6AcLfQ1.png" style="max-width: 100.0%;max-height: 100.0%;" width="340px"> </center><p>Once a year, all the ants need to gather to watch the EUC. For this, all ants move along the $n-1$ branches of the tree they live on to meet at the home of one ant.</p><p>However, this year the ants could not agree on where to meet and need your help to gather up. You can tell all the ants currently at house $u$ to move to house $v$ if there is a branch directly connecting those two houses. However, the ants ignore your command if there are fewer ants gathered in house $v$ than in house $u$, i.e., if it would be easier for the ants from house $v$ to move. This even holds true if no ant at all is currently in house $v$. You can give this kind of commands as many times as you want.</p><p>Is it possible for you to gather all the ants in a single house?</p></div><div class="input-specification"><p>The first line contains one integer $n$ ($1\leq n\leq 200\,000$) — the number of ant homes.</p><p>Each of the following $n-1$ lines contains two integers $u$ and $v$ ($1\leq u, v\leq n$) — there is a branch directly connecting the house $u$ and house $v$. It is guaranteed that every ant can reach the house of any other ant just by following the branches of the tree.</p></div><div class="output-specification"><p>Print $\texttt{YES}$ if it is possible to gather all the ants in a single house. Otherwise, print $\texttt{NO}$.</p></div>

## Input

<p>The first line contains one integer $n$ ($1\leq n\leq 200\,000$) — the number of ant homes.</p><p>Each of the following $n-1$ lines contains two integers $u$ and $v$ ($1\leq u, v\leq n$) — there is a branch directly connecting the house $u$ and house $v$. It is guaranteed that every ant can reach the house of any other ant just by following the branches of the tree.</p>

## Output

<p>Print $\texttt{YES}$ if it is possible to gather all the ants in a single house. Otherwise, print $\texttt{NO}$.</p>





```input1|
7
5 1
3 2
4 6
3 6
7 1
1 3
```




```input2|
5
1 4
4 2
3 2
5 3
```




```input3|
6
4 5
5 6
6 1
2 6
3 2
```




```output1
YES
```




```output2
NO
```




```output3
YES
```



## Note

<p>In the <span class="tex-font-style-bf">first sample</span>, you can gather all the ants at house $3$ as follows: </p><ul> <li> You tell to the ant at house $4$ to move to house $6$. </li><li> You tell to the ant at house $2$ to move to house $3$. </li><li> You tell to the two ants at house $6$ to move to house $3$ (which already contains two ants). </li><li> You tell to the ant at house $5$ to move to house $1$. </li><li> You tell to the ant at house $7$ to move to house $1$ (which already contains two ants). </li><li> You tell to the three ants at house $1$ to move to house $3$ (which already contains four ants). </li></ul><p>In the <span class="tex-font-style-bf">second sample</span>, it is impossible to gather all the ants in a single house.</p>
