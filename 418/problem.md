## Description

<div><p>You are given a string $s$, consisting of lowercase Latin letters.</p><p>There's a cursor, initially placed between two adjacent letters of the string. The cursor can't be placed before the first or after the last letter.</p><p>In one move, you can perform one of three actions: </p><ul> <li> move a cursor one position to the left (if that doesn't place it before the first letter); </li><li> move a cursor one position to the right (if that doesn't place it after the last letter); </li><li> let $x$ be the letter immediately to the left of the cursor, and $y$ be the letter immediately to the right of the cursor. Choose any pair of <span class="tex-font-style-bf">adjacent</span> letters in the string such that the <span class="tex-font-style-bf">left</span> of them is $x$ and the <span class="tex-font-style-bf">right</span> of them is $y$, and move the cursor to the position between these two letters. </li></ul><p>You are asked $m$ queries. In each query, you are given two integers $f$ and $t$, which correspond to two valid positions of the cursor in the string. In response to the query, you have to calculate the minimum number of operations required to move the cursor from position $f$ to position $t$.</p></div><div class="input-specification"><p>The first line contains a string $s$ ($2 \le |s| \le 5 \cdot 10^4$), consisting of lowercase Latin letters.</p><p>The second line contains a single integer $m$ ($1 \le m \le 5 \cdot 10^4$)&nbsp;— the number of queries.</p><p>The $i$-th of the next $m$ lines contains two integers $f$ and $t$ ($1 \le f, t \le |s| - 1$)&nbsp;— the initial and the target positions of the cursor in the $i$-th query. Position $x$ means that the cursor is between the $x$-th and the $(x+1)$-st letters of the string ($1$-indexed).</p></div><div class="output-specification"><p>For each query, print the minimum number of actions required to move the cursor from position $f$ to position $t$.</p></div>

## Input

<p>The first line contains a string $s$ ($2 \le |s| \le 5 \cdot 10^4$), consisting of lowercase Latin letters.</p><p>The second line contains a single integer $m$ ($1 \le m \le 5 \cdot 10^4$)&nbsp;— the number of queries.</p><p>The $i$-th of the next $m$ lines contains two integers $f$ and $t$ ($1 \le f, t \le |s| - 1$)&nbsp;— the initial and the target positions of the cursor in the $i$-th query. Position $x$ means that the cursor is between the $x$-th and the $(x+1)$-st letters of the string ($1$-indexed).</p>

## Output

<p>For each query, print the minimum number of actions required to move the cursor from position $f$ to position $t$.</p>





```input1
codecode
3
1 7
3 5
3 6
```




```input2
abcdefghij
3
1 9
9 1
5 5
```




```input3
aaaaaaaaaaaa
4
10 8
3 7
6 1
11 11
```




```output1
3
2
2
```




```output2
8
8
0
```




```output3
1
1
1
0
```


