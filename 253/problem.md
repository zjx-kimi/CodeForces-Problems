## Description

<div><p>You have $n$ stacks $r_1,r_2,\ldots,r_n$. Each stack contains some positive integers ranging from $1$ to $n$.</p><p>Define the following functions:</p><pre class="lstlisting"><code class="prettyprint">function init(pos):<br>    stacks := an array that contains n stacks r[1], r[2], ..., r[n]<br>    return get(stacks, pos)<br><br>function get(stacks, pos):<br>    if stacks[pos] is empty:<br>        return pos<br>    else:<br>        new_pos := the top element of stacks[pos]<br>        pop the top element of stacks[pos]<br>        return get(stacks, new_pos)<br></code></pre><p>You want to know the values returned by $\texttt{init(1)}, \texttt{init(2)}, \ldots, \texttt{init(n)}$.</p><p>Note that, during these calls, the stacks $r_1,r_2,\ldots,r_n$ don't change, so the calls $\texttt{init(1)}, \texttt{init(2)}, \ldots, \texttt{init(n)}$ are independent.</p></div><div class="input-specification"><p>The first line of the input contains one integer $n$ ($1\le n\le 10^5$)&nbsp;— the length of the array $r$.</p><p>Each of the following $n$ lines contains several integers. The first integer $k_i$ ($0\le k_i\le 10^5$) represents the number of elements in the $i$-th stack, and the following $k_i$ positive integers $c_{i,1},c_{i,2},\ldots,c_{i,k_i}$ ($1\le c_{i,j}\le n$) represent the elements in the $i$-th stack. $c_{i,1}$ is the bottom element.</p><p>In each test, $\sum k_i\le 10^6$.</p></div><div class="output-specification"><p>You need to output $n$ values, the $i$-th of which is the value returned by $\texttt{init(i)}$.</p></div>

## Input

<p>The first line of the input contains one integer $n$ ($1\le n\le 10^5$)&nbsp;— the length of the array $r$.</p><p>Each of the following $n$ lines contains several integers. The first integer $k_i$ ($0\le k_i\le 10^5$) represents the number of elements in the $i$-th stack, and the following $k_i$ positive integers $c_{i,1},c_{i,2},\ldots,c_{i,k_i}$ ($1\le c_{i,j}\le n$) represent the elements in the $i$-th stack. $c_{i,1}$ is the bottom element.</p><p>In each test, $\sum k_i\le 10^6$.</p>

## Output

<p>You need to output $n$ values, the $i$-th of which is the value returned by $\texttt{init(i)}$.</p>





```input1
3
3 1 2 2
3 3 1 2
3 1 2 1
```




```input2
5
5 1 2 4 3 4
6 1 2 5 3 3 4
6 1 1 4 4 4 2
9 3 1 4 2 3 5 5 1 2
4 4 4 1 3
```




```output1
1 2 2
```




```output2
1 1 1 1 1
```



## Note

<p>In the first example: </p><ul> <li> When you call $\texttt{init(1)}$, set $\texttt{stacks := [[1,2,2],[3,1,2],[1,2,1]]}$, and then call $\texttt{get(stacks, 1)}$. <ul> <li> $\texttt{stacks[1]}$ is not empty, set $\texttt{new_pos := 2}$, and pop the top element of $\texttt{stacks[1]}$, which makes $\texttt{stacks}$ become $[[1,2],[3,1,2],[1,2,1]]$, and then call $\texttt{get(stacks, 2)}$. </li><li> $\texttt{stacks[2]}$ is not empty, set $\texttt{new_pos := 2}$, and pop the top element of $\texttt{stacks[2]}$, which makes $\texttt{stacks}$ become $[[1,2],[3,1],[1,2,1]]$, and then call $\texttt{get(stacks, 2)}$. </li><li> $\texttt{stacks[2]}$ is not empty, set $\texttt{new_pos := 1}$, and pop the top element of $\texttt{stacks[2]}$, which makes $\texttt{stacks}$ become $[[1,2],[3],[1,2,1]]$, and then call $\texttt{get(stacks, 1)}$. </li><li> $\texttt{stacks[1]}$ is not empty, set $\texttt{new_pos := 2}$, and pop the top element of $\texttt{stacks[1]}$, which makes $\texttt{stacks}$ become $[[1],[3],[1,2,1]]$, and then call $\texttt{get(stacks, 2)}$. </li><li> $\texttt{stacks[2]}$ is not empty, set $\texttt{new_pos := 3}$, and pop the top element of $\texttt{stacks[2]}$, which makes $\texttt{stacks}$ become $[[1],[],[1,2,1]]$, and then call $\texttt{get(stacks, 3)}$. </li><li> $\texttt{stacks[3]}$ is not empty, set $\texttt{new_pos := 1}$, and pop the top element of $\texttt{stacks[3]}$, which makes $\texttt{stacks}$ become $[[1],[],[1,2]]$, and then call $\texttt{get(stacks, 1)}$. </li><li> $\texttt{stacks[1]}$ is not empty, set $\texttt{new_pos := 1}$, and pop the top element of $\texttt{stacks[1]}$, which makes $\texttt{stacks}$ become $[[],[],[1,2]]$, and then call $\texttt{get(stacks, 1)}$. </li><li> $\texttt{stacks[1]}$ is empty, return $1$. </li></ul> </li><li> When you call $\texttt{init(2)}$, set $\texttt{stacks := [[1,2,2],[3,1,2],[1,2,1]]}$, and then call $\texttt{get(stacks, 2)}$. <ul> <li> $\texttt{stacks[2]}$ is not empty, set $\texttt{new_pos := 2}$, and pop the top element of $\texttt{stacks[2]}$, which makes $\texttt{stacks}$ become $[[1,2,2],[3,1],[1,2,1]]$, and then call $\texttt{get(stacks, 2)}$. </li><li> $\texttt{stacks[2]}$ is not empty, set $\texttt{new_pos := 1}$, and pop the top element of $\texttt{stacks[2]}$, which makes $\texttt{stacks}$ become $[[1,2,2],[3],[1,2,1]]$, and then call $\texttt{get(stacks, 1)}$. </li><li> $\texttt{stacks[1]}$ is not empty, set $\texttt{new_pos := 2}$, and pop the top element of $\texttt{stacks[1]}$, which makes $\texttt{stacks}$ become $[[1,2],[3],[1,2,1]]$, and then call $\texttt{get(stacks, 2)}$. </li><li> $\texttt{stacks[2]}$ is not empty, set $\texttt{new_pos := 3}$, and pop the top element of $\texttt{stacks[2]}$, which makes $\texttt{stacks}$ become $[[1,2],[],[1,2,1]]$, and then call $\texttt{get(stacks, 3)}$. </li><li> $\texttt{stacks[3]}$ is not empty, set $\texttt{new_pos := 1}$, and pop the top element of $\texttt{stacks[3]}$, which makes $\texttt{stacks}$ become $[[1,2],[],[1,2]]$, and then call $\texttt{get(stacks, 1)}$. </li><li> $\texttt{stacks[1]}$ is not empty, set $\texttt{new_pos := 2}$, and pop the top element of $\texttt{stacks[1]}$, which makes $\texttt{stacks}$ become $[[1],[],[1,2]]$, and then call $\texttt{get(stacks, 2)}$. </li><li> $\texttt{stacks[2]}$ is empty, return $2$. </li></ul> </li><li> When you call $\texttt{init(3)}$, set $\texttt{stacks := [[1,2,2],[3,1,2],[1,2,1]]}$, and then call $\texttt{get(stacks, 3)}$. <ul> <li> $\texttt{stacks[3]}$ is not empty, set $\texttt{new_pos := 1}$, and pop the top element of $\texttt{stacks[3]}$, which makes $\texttt{stacks}$ become $[[1,2,2],[3,1,2],[1,2]]$, and then call $\texttt{get(stacks, 1)}$. </li><li> $\texttt{stacks[1]}$ is not empty, set $\texttt{new_pos := 2}$, and pop the top element of $\texttt{stacks[1]}$, which makes $\texttt{stacks}$ become $[[1,2],[3,1,2],[1,2]]$, and then call $\texttt{get(stacks, 2)}$. </li><li> $\texttt{stacks[2]}$ is not empty, set $\texttt{new_pos := 2}$, and pop the top element of $\texttt{stacks[2]}$, which makes $\texttt{stacks}$ become $[[1,2],[3,1],[1,2]]$, and then call $\texttt{get(stacks, 2)}$. </li><li> $\texttt{stacks[2]}$ is not empty, set $\texttt{new_pos := 1}$, and pop the top element of $\texttt{stacks[2]}$, which makes $\texttt{stacks}$ become $[[1,2],[3],[1,2]]$, and then call $\texttt{get(stacks, 1)}$. </li><li> $\texttt{stacks[1]}$ is not empty, set $\texttt{new_pos := 2}$, and pop the top element of $\texttt{stacks[1]}$, which makes $\texttt{stacks}$ become $[[1],[3],[1,2]]$, and then call $\texttt{get(stacks, 2)}$. </li><li> $\texttt{stacks[2]}$ is not empty, set $\texttt{new_pos := 3}$, and pop the top element of $\texttt{stacks[2]}$, which makes $\texttt{stacks}$ become $[[1],[],[1,2]]$, and then call $\texttt{get(stacks, 3)}$. </li><li> $\texttt{stacks[3]}$ is not empty, set $\texttt{new_pos := 2}$, and pop the top element of $\texttt{stacks[3]}$, which makes $\texttt{stacks}$ become $[[1],[],[1]]$, and then call $\texttt{get(stacks, 2)}$. </li><li> $\texttt{stacks[2]}$ is empty, return $2$. </li></ul> </li></ul>
