## Description

<div><p>You are given a permutation of length $n$. Recall that the permutation is an array consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. For example, $[2, 3, 1, 5, 4]$ is a permutation, but $[1, 2, 2]$ is not a permutation ($2$ appears twice in the array) and $[1, 3, 4]$ is also not a permutation ($n=3$ but there is $4$ in the array).</p><p>You can perform at most $n-1$ operations with the given permutation (it is possible that you don't perform any operations at all). The $i$-th operation allows you to swap elements of the given permutation on positions $i$ and $i+1$. <span class="tex-font-style-bf">Each operation can be performed at most once</span>. The operations can be performed in arbitrary order.</p><p>Your task is to find the lexicographically minimum possible permutation obtained by performing some of the given operations in some order.</p><p>You can see the definition of the lexicographical order in the notes section.</p><p>You have to answer $q$ independent test cases.</p><p>For example, let's consider the permutation $[5, 4, 1, 3, 2]$. The minimum possible permutation we can obtain is $[1, 5, 2, 4, 3]$ and we can do it in the following way:</p><ol> <li> perform the second operation (swap the second and the third elements) and obtain the permutation $[5, 1, 4, 3, 2]$; </li><li> perform the fourth operation (swap the fourth and the fifth elements) and obtain the permutation $[5, 1, 4, 2, 3]$; </li><li> perform the third operation (swap the third and the fourth elements) and obtain the permutation $[5, 1, 2, 4, 3]$. </li><li> perform the first operation (swap the first and the second elements) and obtain the permutation $[1, 5, 2, 4, 3]$; </li></ol><p>Another example is $[1, 2, 4, 3]$. The minimum possible permutation we can obtain is $[1, 2, 3, 4]$ by performing the third operation (swap the third and the fourth elements).</p></div><div class="input-specification"><p>The first line of the input contains one integer $q$ ($1 \le q \le 100$) — the number of test cases. Then $q$ test cases follow.</p><p>The first line of the test case contains one integer $n$ ($1 \le n \le 100$) — the number of elements in the permutation.</p><p>The second line of the test case contains $n$ distinct integers from $1$ to $n$ — the given permutation.</p></div><div class="output-specification"><p>For each test case, print the answer on it — the lexicograhically minimum possible permutation obtained by performing some of the given operations in some order.</p></div>

## Input

<p>The first line of the input contains one integer $q$ ($1 \le q \le 100$) — the number of test cases. Then $q$ test cases follow.</p><p>The first line of the test case contains one integer $n$ ($1 \le n \le 100$) — the number of elements in the permutation.</p><p>The second line of the test case contains $n$ distinct integers from $1$ to $n$ — the given permutation.</p>

## Output

<p>For each test case, print the answer on it — the lexicograhically minimum possible permutation obtained by performing some of the given operations in some order.</p>





```input1
4
5
5 4 1 3 2
4
1 2 4 3
1
1
4
4 3 2 1
```




```output1
1 5 2 4 3 
1 2 3 4 
1 
1 4 3 2
```



## Note

<p>Recall that the permutation $p$ of length $n$ is lexicographically less than the permutation $q$ of length $n$ if there is such index $i \le n$ that for all $j$ from $1$ to $i - 1$ the condition $p_j = q_j$ is satisfied, and $p_i &lt; q_i$. For example:</p><ul> <li> $p = [1, 3, 5, 2, 4]$ is less than $q = [1, 3, 5, 4, 2]$ (such $i=4$ exists, that $p_i &lt; q_i$ and for each $j &lt; i$ holds $p_j = q_j$), </li><li> $p = [1, 2]$ is less than $q = [2, 1]$ (such $i=1$ exists, that $p_i &lt; q_i$ and for each $j &lt; i$ holds $p_j = q_j$). </li></ul>
