## Description

<div><p>Chaneka, Pak Chanek's child, is an ambitious kid, so Pak Chanek gives her the following problem to test her ambition.</p><p>Given an array of integers $[A_1, A_2, A_3, \ldots, A_N]$. In one operation, Chaneka can choose one element, then increase or decrease the element's value by $1$. Chaneka can do that operation multiple times, even for different elements.</p><p>What is the minimum number of operations that must be done to make it such that $A_1 \times A_2 \times A_3 \times \ldots \times A_N = 0$?</p></div><div class="input-specification"><p>The first line contains a single integer $N$ ($1 \leq N \leq 10^5$).</p><p>The second line contains $N$ integers $A_1, A_2, A_3, \ldots, A_N$ ($-10^5 \leq A_i \leq 10^5$).</p></div><div class="output-specification"><p>An integer representing the minimum number of operations that must be done to make it such that $A_1 \times A_2 \times A_3 \times \ldots \times A_N = 0$.</p></div>

## Input

<p>The first line contains a single integer $N$ ($1 \leq N \leq 10^5$).</p><p>The second line contains $N$ integers $A_1, A_2, A_3, \ldots, A_N$ ($-10^5 \leq A_i \leq 10^5$).</p>

## Output

<p>An integer representing the minimum number of operations that must be done to make it such that $A_1 \times A_2 \times A_3 \times \ldots \times A_N = 0$.</p>





```input1
3
2 -6 5
```




```input2
1
-3
```




```input3
5
0 -1 0 1 0
```




```output1
2
```




```output2
3
```




```output3
0
```



## Note

<p>In the first example, initially, $A_1\times A_2\times A_3=2\times(-6)\times5=-60$. Chaneka can do the following sequence of operations:</p><ol> <li> Decrease the value of $A_1$ by $1$. Then, $A_1\times A_2\times A_3=1\times(-6)\times5=-30$ </li><li> Decrease the value of $A_1$ by $1$. Then, $A_1\times A_2\times A_3=0\times(-6)\times5=0$ </li></ol><p>In the third example, Chaneka does not have to do any operations, because from the start, it already holds that $A_1\times A_2\times A_3\times A_4\times A_5=0\times(-1)\times0\times1\times0=0$</p>
