## Description

<div><p>In Homer's country, there are $n$ cities numbered $1$ to $n$ and they form a tree. That is, there are $(n-1)$ undirected roads between these $n$ cities and every two cities can reach each other through these roads. </p><p>Homer's country is an industrial country, and each of the $n$ cities in it contains some mineral resource. The mineral resource of city $i$ is labeled $a_i$. </p><p>Homer is given the plans of the country in the following $q$ years. The plan of the $i$-th year is described by four parameters $u_i, v_i, l_i$ and $r_i$, and he is asked to find any mineral resource $c_i$ such that the following two conditions hold: </p><ul> <li> mineral resource $c_i$ appears an <span class="tex-font-style-bf">odd</span> number of times between city $u_i$ and city $v_i$; and </li><li> $l_i \leq c_i \leq r_i$. </li></ul><p>As the best friend of Homer, he asks you for help. For every plan, find any such mineral resource $c_i$, or tell him that there doesn't exist one.</p></div><div class="input-specification"><p>The first line contains two integers $n$ ($1 \leq n \leq 3 \cdot 10^5$) and $q$ ($1 \leq q \leq 3 \cdot 10^5$), indicating the number of cities and the number of plans.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \leq a_i \leq n$).</p><p>Then the $i$-th line of the following $(n-1)$ lines contains two integers $x_i$ and $y_i$ ($1 \leq x_i, y_i \leq n$) with $x_i \neq y_i$, indicating that there is a bidirectional road between city $x_i$ and city $y_i$. It is guaranteed that the given roads form a tree.</p><p>Then the $i$-th line of the following $q$ lines contains four integers $u_i$, $v_i$, $l_i$, $r_i$ ($1 \leq u_i \leq n$, $1 \leq v_i \leq n$, $1 \leq l_i \leq r_i \leq n$), indicating the plan of the $i$-th year.</p></div><div class="output-specification"><p>Print $q$ lines, the $i$-th of which contains an integer $c_i$ such that </p><ul> <li> $c_i = {-1}$ if there is no such mineral resource that meets the required condition; or </li><li> $c_i$ is the label of the chosen mineral resource of the $i$-th year. The chosen mineral resource $c_i$ should meet those conditions in the $i$-th year described above in the problem statement. If there are multiple choices of $c_i$, you can print any of them. </li></ul></div>

## Input

<p>The first line contains two integers $n$ ($1 \leq n \leq 3 \cdot 10^5$) and $q$ ($1 \leq q \leq 3 \cdot 10^5$), indicating the number of cities and the number of plans.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \leq a_i \leq n$).</p><p>Then the $i$-th line of the following $(n-1)$ lines contains two integers $x_i$ and $y_i$ ($1 \leq x_i, y_i \leq n$) with $x_i \neq y_i$, indicating that there is a bidirectional road between city $x_i$ and city $y_i$. It is guaranteed that the given roads form a tree.</p><p>Then the $i$-th line of the following $q$ lines contains four integers $u_i$, $v_i$, $l_i$, $r_i$ ($1 \leq u_i \leq n$, $1 \leq v_i \leq n$, $1 \leq l_i \leq r_i \leq n$), indicating the plan of the $i$-th year.</p>

## Output

<p>Print $q$ lines, the $i$-th of which contains an integer $c_i$ such that </p><ul> <li> $c_i = {-1}$ if there is no such mineral resource that meets the required condition; or </li><li> $c_i$ is the label of the chosen mineral resource of the $i$-th year. The chosen mineral resource $c_i$ should meet those conditions in the $i$-th year described above in the problem statement. If there are multiple choices of $c_i$, you can print any of them. </li></ul>





```input1
6 8
3 2 1 3 1 3
1 2
1 3
2 4
2 5
4 6
3 5 1 1
3 5 1 3
3 5 1 3
1 1 2 2
1 1 3 3
1 4 1 5
1 6 1 3
1 6 1 3
```




```output1
-1
2
3
-1
3
2
2
3
```



## Note

<p>In the first three queries, there are four cities between city $3$ and city $5$, which are city $1$, city $2$, city $3$ and city $5$. The mineral resources appear in them are mineral resources $1$ (appears in city $3$ and city $5$), $2$ (appears in city $2$) and $3$ (appears in city $1$). It is noted that </p><ul> <li> The first query is only to check whether mineral source $1$ appears an odd number of times between city $3$ and city $5$. The answer is no, because mineral source $1$ appears twice (an even number of times) between city $3$ and city $5$. </li><li> The second and the third queries are the same but they can choose different mineral resources. Both mineral resources $2$ and $3$ are available. </li></ul>
