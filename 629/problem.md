## Description

<div><p>There is a beautiful alley with trees in front of a shopping mall. Unfortunately, it has to go to make space for the parking lot.</p><p>The trees on the alley all grow in a single line. There are $n$ spots for trees, index $0$ is the shopping mall, index $n+1$ is the road and indices from $1$ to $n$ are the spots for trees. Some of them are taken&nbsp;— there grow trees of the same height $k$. No more than one tree grows in each spot.</p><p>When you chop down a tree in the spot $x$, you can make it fall either left or right. If it falls to the left, it takes up spots from $x-k$ to $x$, inclusive. If it falls to the right, it takes up spots from $x$ to $x+k$, inclusive.</p><p>Let $m$ trees on the alley grow in some spots $x_1, x_2, \dots, x_m$. Let an alley be called <span class="tex-font-style-it">unfortunate</span> if all $m$ trees can be chopped down in such a way that: </p><ul> <li> no tree falls on the shopping mall or the road; </li><li> each spot is taken up by no more than one fallen tree. </li></ul><p>Calculate the number of different <span class="tex-font-style-it">unfortunate</span> alleys with $m$ trees of height $k$. Two alleys are considered different if there is a spot $y$ such that a tree grows in $y$ on the first alley and doesn't grow in $y$ on the second alley.</p><p>Output the number modulo $998\,244\,353$.</p></div><div class="input-specification"><p>The only line contains three integers $n, m$ and $k$ ($1 \le m, k \le n \le 3 \cdot 10^5$)&nbsp;— the number of spots for the trees, the number of trees and the height of each tree.</p></div><div class="output-specification"><p>Print a single integer&nbsp;— the number of different <span class="tex-font-style-it">unfortunate</span> alleys with $m$ trees of height $k$, modulo $998\,244\,353$. </p></div>

## Input

<p>The only line contains three integers $n, m$ and $k$ ($1 \le m, k \le n \le 3 \cdot 10^5$)&nbsp;— the number of spots for the trees, the number of trees and the height of each tree.</p>

## Output

<p>Print a single integer&nbsp;— the number of different <span class="tex-font-style-it">unfortunate</span> alleys with $m$ trees of height $k$, modulo $998\,244\,353$. </p>





```input1
6 1 4
```




```input2
5 2 2
```




```input3
6 2 2
```




```input4
15 3 2
```




```output1
4
```




```output2
0
```




```output3
4
```




```output4
311
```


