## Description

<div><p>You have an array of integers $a$ of length $n$. You can apply the following operation to the given array: </p><ul> <li> Swap two elements $a_i$ and $a_j$ such that $i \neq j$, $a_i$ and $a_j$ are either <span class="tex-font-style-bf">both</span> even or <span class="tex-font-style-bf">both</span> odd. </li></ul><p> Determine whether it is possible to sort the array in non-decreasing order by performing the operation any number of times (possibly zero).</p><p>For example, let $a$ = [$7, 10, 1, 3, 2$]. Then we can perform $3$ operations to sort the array: </p><ol> <li> Swap $a_3 = 1$ and $a_1 = 7$, since $1$ and $7$ are odd. We get $a$ = [$1, 10, 7, 3, 2$]; </li><li> Swap $a_2 = 10$ and $a_5 = 2$, since $10$ and $2$ are even. We get $a$ = [$1, 2, 7, 3, 10$]; </li><li> Swap $a_4 = 3$ and $a_3 = 7$, since $3$ and $7$ are odd. We get $a$ = [$1, 2, 3, 7, 10$]. </li></ol></div><div class="input-specification"><p>The first line of input data contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The description of the test cases follows.</p><p>The first line of each test case contains one integer $n$ ($1 \le n \le 2 \cdot 10^5$) — the length of array $a$.</p><p>The second line of each test case contains exactly $n$ positive integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the elements of array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output on a separate line: </p><ul> <li> <span class="tex-font-style-tt">YES</span> if the array can be sorted by applying the operation to it some number of times; </li><li> <span class="tex-font-style-tt">NO</span> otherwise. </li></ul><p>You can output <span class="tex-font-style-tt">YES</span> and <span class="tex-font-style-tt">NO</span> in any case (for example, strings <span class="tex-font-style-tt">yEs</span>, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span> and <span class="tex-font-style-tt">YES</span> will be recognized as positive response).</p></div>

## Input

<p>The first line of input data contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The description of the test cases follows.</p><p>The first line of each test case contains one integer $n$ ($1 \le n \le 2 \cdot 10^5$) — the length of array $a$.</p><p>The second line of each test case contains exactly $n$ positive integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the elements of array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output on a separate line: </p><ul> <li> <span class="tex-font-style-tt">YES</span> if the array can be sorted by applying the operation to it some number of times; </li><li> <span class="tex-font-style-tt">NO</span> otherwise. </li></ul><p>You can output <span class="tex-font-style-tt">YES</span> and <span class="tex-font-style-tt">NO</span> in any case (for example, strings <span class="tex-font-style-tt">yEs</span>, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span> and <span class="tex-font-style-tt">YES</span> will be recognized as positive response).</p>





```input1|2,3,6,7,10,11
6
5
7 10 1 3 2
4
11 9 3 5
5
11 3 15 3 2
6
10 7 8 1 2 3
1
10
5
6 6 4 1 6
```




```output1
YES
YES
NO
NO
YES
NO
```



## Note

<p>The first test case is explained in the problem statement.</p>
