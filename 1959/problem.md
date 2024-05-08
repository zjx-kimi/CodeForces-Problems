## Description

<div><p>Petya has a rooted tree with an integer written on each vertex. The vertex $1$ is the root. You are to answer some questions about the tree.</p><p>A tree is a connected graph without cycles. A rooted tree has a special vertex called the root. The parent of a node $v$ is the next vertex on the shortest path from $v$ to the root.</p><p>Each question is defined by three integers $v$, $l$, and $k$. To get the answer to the question, you need to perform the following steps: </p><ul> <li> First, write down the sequence of all integers written on the shortest path from the vertex $v$ to the root (including those written in the $v$ and the root). </li><li> Count the number of times each integer occurs. Remove all integers with less than $l$ occurrences. </li><li> Replace the sequence, removing all duplicates and ordering the elements by the number of occurrences in the original list in increasing order. In case of a tie, you can choose the order of these elements arbitrary. </li><li> The answer to the question is the $k$-th number in the remaining sequence. Note that the answer is not always uniquely determined, because there could be several orderings. Also, it is possible that the length of the sequence on this step is less than $k$, in this case the answer is $-1$. </li></ul><p>For example, if the sequence of integers on the path from $v$ to the root is $[2, 2, 1, 7, 1, 1, 4, 4, 4, 4]$, $l = 2$ and $k = 2$, then the answer is $1$.</p><p>Please answer all questions about the tree.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 10^6$). Description of the test cases follows.</p><p>The first line of each test case contains two integers $n$, $q$ ($1 \leq n, q \leq 10^6$) — the number of vertices in the tree and the number of questions.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq n$), where $a_i$ is the number written on the $i$-th vertex.</p><p>The third line contains $n-1$ integers $p_2, p_3, \ldots, p_n$ ($1 \leq p_i \leq n$), where $p_i$ is the parent of node $i$. It's guaranteed that the values $p$ define a correct tree.</p><p>Each of the next $q$ lines contains three integers $v$, $l$, $k$ ($1 \leq v, l, k \leq n$) — descriptions of questions.</p><p>It is guaranteed that the sum of $n$ and the sum of $q$ over all test cases do not exceed $10^6$.</p></div><div class="output-specification"><p>For each question of each test case print the answer to the question. In case of multiple answers, print any.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 10^6$). Description of the test cases follows.</p><p>The first line of each test case contains two integers $n$, $q$ ($1 \leq n, q \leq 10^6$) — the number of vertices in the tree and the number of questions.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq n$), where $a_i$ is the number written on the $i$-th vertex.</p><p>The third line contains $n-1$ integers $p_2, p_3, \ldots, p_n$ ($1 \leq p_i \leq n$), where $p_i$ is the parent of node $i$. It's guaranteed that the values $p$ define a correct tree.</p><p>Each of the next $q$ lines contains three integers $v$, $l$, $k$ ($1 \leq v, l, k \leq n$) — descriptions of questions.</p><p>It is guaranteed that the sum of $n$ and the sum of $q$ over all test cases do not exceed $10^6$.</p>

## Output

<p>For each question of each test case print the answer to the question. In case of multiple answers, print any.</p>





```input1
2
3 3
1 1 1
1 2
3 1 1
3 1 2
3 2 1
5 5
1 2 1 1 2
1 1 2 2
3 1 1
2 1 2
4 1 1
4 2 1
4 2 2
```




```output1
1 -1 1 
1 1 2 1 -1
```


