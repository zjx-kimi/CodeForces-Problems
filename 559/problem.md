## Description

<div><p>Recently, Polycarp was given an unusual typewriter as a gift! Unfortunately, the typewriter was defective and had a rather strange design.</p><p>The typewriter consists of $n$ cells numbered from left to right from $1$ to $n$, and a carriage that moves over them. The typewriter cells contain $n$ <span class="tex-font-style-bf">distinct</span> integers from $1$ to $n$, and each cell $i$ initially contains the integer $p_i$. Before all actions, the carriage is at cell number $1$ and there is nothing in its buffer storage. The cell on which the carriage is located is called the <span class="tex-font-style-bf">current</span> cell. </p><p>The carriage can perform five types of operations:</p><ul> <li> Take the integer from the current cell, if it is not empty, and put it in the carriage buffer, if it is empty (this buffer can contain <span class="tex-font-style-bf">no more than one</span> integer). </li><li> Put the integer from the carriage buffer, if it is not empty, into the current cell, if it is empty. </li><li> Swap the number in the carriage buffer with the number in the current cell, if both the buffer and the cell contain integers. </li><li> Move the carriage from the current cell $i$ to cell $i + 1$ (if $i &lt; n$), while the integer in the buffer is preserved. </li><li> Reset the carriage, i.e. move it to cell number $1$, while the integer in the buffer is preserved. </li></ul><p>Polycarp was very interested in this typewriter, so he asks you to help him understand it and will ask you $q$ queries of three types:</p><ol> <li> Perform a cyclic shift of the sequence $p$ to the left by $k_j$. </li><li> Perform a cyclic shift of the sequence $p$ to the right by $k_j$. </li><li> Reverse the sequence $p$. </li></ol><p>Before and after each query, Polycarp wants to know what <span class="tex-font-style-bf">minimum</span> number of carriage resets is needed for the current sequence in order to distribute the numbers to their cells (so that the number $i$ ends up in cell number $i$).</p><p>Note that Polycarp only wants to know the minimum number of carriage resets required to arrange the numbers in their places, but <span class="tex-font-style-bf">he does not actually distribute them</span>.</p><p>Help Polycarp find the answers to his queries!</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($1 \le n \le 4 \cdot 10^5$)&nbsp;— the number of cells.</p><p>The second line contains $n$ distinct integers $p_1, p_2, \ldots, p_n$ ($1 \le p_i \le n$)&nbsp;— the initial arrangement of integers in the cells.</p><p>The third line contains a single integer $q$ ($0 \le q \le 4 \cdot 10^5$)&nbsp;— the number of queries.</p><p>Each of the next $q$ lines describes a query from Polycarp:</p><p>The $j$-th line, at first, contains the integer $t_j$ ($1 \le t_j \le 3$) &nbsp;— the type of query.</p><p>If the query is of type $t_j = 1$ or $t_j = 2$, then the integer $k_j$ ($1 \le k_j \le n$) &nbsp;— the length of the shift &nbsp;— follows in the same line.</p></div><div class="output-specification"><p>Output $q + 1$ numbers&nbsp;— the minimum number of carriage resets required before and after each of Polycarp's queries.</p></div>

## Input

<p>The first line contains a single integer $n$ ($1 \le n \le 4 \cdot 10^5$)&nbsp;— the number of cells.</p><p>The second line contains $n$ distinct integers $p_1, p_2, \ldots, p_n$ ($1 \le p_i \le n$)&nbsp;— the initial arrangement of integers in the cells.</p><p>The third line contains a single integer $q$ ($0 \le q \le 4 \cdot 10^5$)&nbsp;— the number of queries.</p><p>Each of the next $q$ lines describes a query from Polycarp:</p><p>The $j$-th line, at first, contains the integer $t_j$ ($1 \le t_j \le 3$) &nbsp;— the type of query.</p><p>If the query is of type $t_j = 1$ or $t_j = 2$, then the integer $k_j$ ($1 \le k_j \le n$) &nbsp;— the length of the shift &nbsp;— follows in the same line.</p>

## Output

<p>Output $q + 1$ numbers&nbsp;— the minimum number of carriage resets required before and after each of Polycarp's queries.</p>





```input1
3
2 3 1
0
```




```input2
3
1 2 3
2
2 1
3
```




```input3
5
3 1 2 5 4
5
1 3
3
2 3
1 4
3
```




```output1
1
```




```output2
0
2
1
```




```output3
3
2
1
2
1
2
```



## Note

<p>In the first example, the answer is $1$. You can understand how the carriage works using this example.</p><center> <img class="tex-graphics" src="file://dJvwvxGF.png" style="max-width: 100.0%;max-height: 100.0%;" width="756px"> </center><p>In the second example, the sequences for which the answer needs to be calculated look like this:</p><ol> <li> Before all queries: $1\ 2\ 3$&nbsp;— the answer is $0$.</li><li> After shifting to the right by $1$: $3\ 1\ 2$&nbsp;— the answer is $2$.</li><li> After reversing the sequence: $2\ 1\ 3$&nbsp;— the answer is $1$. </li></ol><p>In the third example, the sequences before and after each query look like this:</p><ol> <li> $3\ 1\ 2\ 5\ 4$&nbsp;— the answer is $3$.</li><li> $5\ 4\ 3\ 1\ 2$&nbsp;— the answer is $2$.</li><li> $2\ 1\ 3\ 4\ 5$&nbsp;— the answer is $1$.</li><li> $3\ 4\ 5\ 2\ 1$&nbsp;— the answer is $2$.</li><li> $1\ 3\ 4\ 5\ 2$&nbsp;— the answer is $1$.</li><li> $2\ 5\ 4\ 3\ 1$&nbsp;— the answer is $2$. </li></ol>
