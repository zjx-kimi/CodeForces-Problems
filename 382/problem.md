## Description

<div><p>There are $N$ arrays, each array has $M$ positive integer elements The $j$-th element of the $i$-th array is $A_{i,j}$.</p><p>Initially, Chaneka's digital wallet contains $0$ money. Given an integer $K$. Chaneka will do $M-K+1$ operations. In the $p$-th operation, Chaneka does the following procedure: </p><ol> <li> Choose any array. Let's say Chaneka chooses the $x$-th array. </li><li> Choose an index $y$ in that array such that $p \leq y \leq p+K-1$. </li><li> Add the value of $A_{x, y}$ to the total money in the wallet. </li><li> Change the value of $A_{x, y}$ into $0$. </li></ol><p>Determine the maximum total money that can be earned!</p></div><div class="input-specification"><p>The first line contains three integers $N$, $M$, and $K$ ($1 \leq N \leq 10$; $1 \leq M \leq 10^5$; $1 \leq K \leq \min(10, M)$) — the number of arrays, the size of each array, and the constant that describes the operation constraints.</p><p>The $i$-th of the next $N$ lines contains $M$ integers $A_{i,1}, A_{i,2}, \ldots, A_{i,M}$ ($1 \leq A_{i,j} \leq 10^6$) — the elements of the $i$-th array.</p></div><div class="output-specification"><p>Output an integer representing the maximum total money that can be earned.</p></div>

## Input

<p>The first line contains three integers $N$, $M$, and $K$ ($1 \leq N \leq 10$; $1 \leq M \leq 10^5$; $1 \leq K \leq \min(10, M)$) — the number of arrays, the size of each array, and the constant that describes the operation constraints.</p><p>The $i$-th of the next $N$ lines contains $M$ integers $A_{i,1}, A_{i,2}, \ldots, A_{i,M}$ ($1 \leq A_{i,j} \leq 10^6$) — the elements of the $i$-th array.</p>

## Output

<p>Output an integer representing the maximum total money that can be earned.</p>





```input1
3 3 1
10 4 2
8 1 9
4 8 2
```




```input2
3 3 2
5 9 4
1 3 1
2 8 7
```




```input3
3 4 3
5 9 10 1
1 3 1 5
2 5 7 2
```




```output1
27
```




```output2
17
```




```output3
19
```



## Note

<p>In the first example, the following is a sequence of operations of one optimal strategy:</p><ol> <li> Choosing element $A_{1, 1}$ with a value of $10$. </li><li> Choosing element $A_{3, 2}$ with a value of $8$. </li><li> Choosing element $A_{2, 3}$ with a value of $9$. </li></ol><p>So the total money earned is $10+8+9=27$.</p><p>In the second example, the following is a sequence of operations of one optimal strategy:</p><ol> <li> Choosing element $A_{3, 2}$ with a value of $8$. </li><li> Choosing element $A_{1, 2}$ with a value of $9$. </li></ol><p>So the total money earned is $8+9=17$.</p><p>In the third example, the following is a sequence of operations of one optimal strategy:</p><ol> <li> Choosing element $A_{1, 3}$ with a value of $10$. </li><li> Choosing element $A_{1, 2}$ with a value of $9$. </li></ol><p>So the total money earned is $10+9=19$.</p>
