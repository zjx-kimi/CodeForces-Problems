## Description

<div><p>You are given a permutation$^\dagger$ $a$ of size $n$. You can do the following operation </p><ul> <li> Select an index $i$ from $2$ to $n - 1$ such that $a_{i - 1} &lt; a_i$ and $a_i &gt; a_{i+1}$. Swap $a_i$ and $a_{i+1}$. </li></ul><p>Determine whether it is possible to sort the permutation after a finite number of operations.</p><p>$^\dagger$ A permutation is an array consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation ($2$ appears twice in the array) and $[1,3,4]$ is also not a permutation ($n=3$ but there is $4$ in the array).</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 5000$). Description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($3 \le n \le 10$)&nbsp;— the size of the permutation.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le n$)&nbsp;— the elements of permutation $a$.</p></div><div class="output-specification"><p>For each test case, print "<span class="tex-font-style-tt">YES</span>" if it is possible to sort the permutation, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You may print each letter in any case (for example, "<span class="tex-font-style-tt">YES</span>", "<span class="tex-font-style-tt">Yes</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">yEs</span>" will all be recognized as positive answer).</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 5000$). Description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($3 \le n \le 10$)&nbsp;— the size of the permutation.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le n$)&nbsp;— the elements of permutation $a$.</p>

## Output

<p>For each test case, print "<span class="tex-font-style-tt">YES</span>" if it is possible to sort the permutation, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You may print each letter in any case (for example, "<span class="tex-font-style-tt">YES</span>", "<span class="tex-font-style-tt">Yes</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">yEs</span>" will all be recognized as positive answer).</p>





```input1|2,3,6,7,10,11
6
3
1 2 3
5
1 3 2 5 4
5
5 4 3 2 1
3
3 1 2
4
2 3 1 4
5
5 1 2 3 4
```




```output1
YES
YES
NO
NO
NO
NO
```



## Note

<p>In the first test case, the permutation is already sorted.</p><p>In the second test case, we can choose index $i=2$ as $1&lt;3$ and $3&gt;2$ to form $[1, 2, 3, 5, 4]$. Then, we can choose index $i=4$ as $3&lt;5$ and $5&gt;4$ to form $[1, 2, 3, 4, 5]$.</p><p>In the third test case, it can be proven that it is impossible to sort the permutation.</p>
