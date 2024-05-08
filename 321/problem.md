## Description

<div><p>Chaneka writes down an array $a$ of $n$ positive integer elements. Initially, all elements are not circled. In one operation, Chaneka can circle an element. It is possible to circle the same element more than once.</p><p>After doing all operations, Chaneka makes a sequence $r$ consisting of all <span class="tex-font-style-bf">uncircled</span> elements of $a$ following the order of their indices.</p><p>Chaneka also makes another sequence $p$ such that its length is equal to the number of operations performed and $p_i$ is the <span class="tex-font-style-bf">index</span> of the element that is circled in the $i$-th operation.</p><p>Chaneka wants to do several operations such that sequence $r$ is equal to sequence $p$. Help her achieve this, or report if it is impossible! Note that if there are multiple solutions, you can print any of them.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($1 \leq n \leq 2\cdot10^5$) — the size of array $a$.</p><p>The second line contains $n$ integers $a_1,a_2,a_3,\ldots,a_n$ ($1\leq a_i\leq n$).</p></div><div class="output-specification"><p>A single line containing $-1$ if it is impossible.</p><p>Otherwise, the output consists of two lines. The first line contains an integer $z$ representing the number of operations performed. The second line contains $z$ integers, the $i$-th integer represents the index of the element circled in the $i$-th operation. If there are multiple solutions, you can print any of them.</p></div>

## Input

<p>The first line contains a single integer $n$ ($1 \leq n \leq 2\cdot10^5$) — the size of array $a$.</p><p>The second line contains $n$ integers $a_1,a_2,a_3,\ldots,a_n$ ($1\leq a_i\leq n$).</p>

## Output

<p>A single line containing $-1$ if it is impossible.</p><p>Otherwise, the output consists of two lines. The first line contains an integer $z$ representing the number of operations performed. The second line contains $z$ integers, the $i$-th integer represents the index of the element circled in the $i$-th operation. If there are multiple solutions, you can print any of them.</p>





```input1
5
3 4 2 2 3
```




```input2
3
1 2 3
```




```output1
3
3 2 3
```




```output2
-1
```



## Note

<p>In the first example, doing the operations like the example output gives the following results: </p><ul> <li> Element $a_2$ gets circled $1$ time. </li><li> Element $a_3$ gets circled $2$ times. </li><li> The uncircled elements (ordered by their indices) are $a_1$, $a_4$, and $a_5$. So $r=[3,2,3]$. </li><li> $p=[3,2,3]$ </li></ul><p>Therefore, $r=p$.</p><p>In the second example, it is impossible.</p>
