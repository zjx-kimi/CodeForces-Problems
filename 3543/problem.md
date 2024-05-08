## Description

<div><p>Let $a$ be a matrix of size $r \times c$ containing positive integers, not necessarily distinct. Rows of the matrix are numbered from $1$ to $r$, columns are numbered from $1$ to $c$. We can construct an array $b$ consisting of $r + c$ integers as follows: for each $i \in [1, r]$, let $b_i$ be the greatest common divisor of integers in the $i$-th row, and for each $j \in [1, c]$ let $b_{r+j}$ be the greatest common divisor of integers in the $j$-th column. </p><p>We call the matrix <span class="tex-font-style-bf">diverse</span> if all $r + c$ numbers $b_k$ ($k \in [1, r + c]$) are pairwise distinct. </p><p>The <span class="tex-font-style-bf">magnitude</span> of a matrix equals to the maximum of $b_k$.</p><p>For example, suppose we have the following matrix:</p><center> $\begin{pmatrix} 2 &amp; 9 &amp; 7\\ 4 &amp; 144 &amp; 84 \end{pmatrix}$ </center><p>We construct the array $b$:</p><ol> <li> $b_1$ is the greatest common divisor of $2$, $9$, and $7$, that is $1$; </li><li> $b_2$ is the greatest common divisor of $4$, $144$, and $84$, that is $4$; </li><li> $b_3$ is the greatest common divisor of $2$ and $4$, that is $2$; </li><li> $b_4$ is the greatest common divisor of $9$ and $144$, that is $9$; </li><li> $b_5$ is the greatest common divisor of $7$ and $84$, that is $7$. </li></ol><p>So $b = [1, 4, 2, 9, 7]$. All values in this array are distinct, so the matrix is diverse. The magnitude is equal to $9$.</p><p>For a given $r$ and $c$, find a diverse matrix that minimises the magnitude. If there are multiple solutions, you may output any of them. If there are no solutions, output a single integer $0$. </p></div><div class="input-specification"><p>The only line in the input contains two space separated integers $r$ and $c$ ($1 \leq r,c \leq 500$)&nbsp;— the number of rows and the number of columns of the matrix to be found.</p></div><div class="output-specification"><p>If there is no solution, output a single integer $0$.</p><p>Otherwise, output $r$ rows. The $i$-th of them should contain $c$ space-separated integers, the $j$-th of which is $a_{i,j}$ — the positive integer in the $i$-th row and $j$-th column of a diverse matrix minimizing the magnitude.</p><p>Furthermore, it must hold that $1 \leq a_{i,j} \leq 10^9$. It can be shown that if a solution exists, there is also a solution with this additional constraint (still having minimum possible magnitude).</p></div>

## Input

<p>The only line in the input contains two space separated integers $r$ and $c$ ($1 \leq r,c \leq 500$)&nbsp;— the number of rows and the number of columns of the matrix to be found.</p>

## Output

<p>If there is no solution, output a single integer $0$.</p><p>Otherwise, output $r$ rows. The $i$-th of them should contain $c$ space-separated integers, the $j$-th of which is $a_{i,j}$ — the positive integer in the $i$-th row and $j$-th column of a diverse matrix minimizing the magnitude.</p><p>Furthermore, it must hold that $1 \leq a_{i,j} \leq 10^9$. It can be shown that if a solution exists, there is also a solution with this additional constraint (still having minimum possible magnitude).</p>





```input1
2 2
```




```input2
1 1
```




```output1
4 12
2 9
```




```output2
0
```



## Note

<p>In the first example, the GCDs of rows are $b_1 = 4$ and $b_2 = 1$, and the GCDs of columns are $b_3 = 2$ and $b_4 = 3$. All GCDs are pairwise distinct and the maximum of them is $4$. Since the GCDs have to be distinct and at least $1$, it is clear that there are no diverse matrices of size $2 \times 2$ with magnitude smaller than $4$.</p><p>In the second example, no matter what $a_{1,1}$ is, $b_1 = b_2$ will always hold, so there are no diverse matrices.</p>
