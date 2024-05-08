## Description

<div><p>An array $b_1, b_2, \ldots, b_n$ of positive integers is good if all the sums of two adjacent elements are equal to the same value. More formally, the array is good if there exists a $k$ such that $b_1 + b_2 = b_2 + b_3 = \ldots = b_{n-1} + b_n = k$.</p><p>Doremy has an array $a$ of length $n$. Now Doremy can permute its elements (change their order) however she wants. Determine if she can make the array good.</p></div><div class="input-specification"><p>The input consists of multiple test cases. The first line contains a single integer $t$ ($1\le t\le 100$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 100$)&nbsp;— the length of the array $a$.</p><p>The second line of each test case contains $ n $ integers $ a_1,a_2,\ldots,a_n $ ($1 \le a_i \le 10^5$).</p><p>There are no constraints on the sum of $n$ over all test cases.</p></div><div class="output-specification"><p>For each test case, print "<span class="tex-font-style-tt">Yes</span>" (without quotes), if it is possible to make the array good, and "<span class="tex-font-style-tt">No</span>" (without quotes) otherwise.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p></div>

## Input

<p>The input consists of multiple test cases. The first line contains a single integer $t$ ($1\le t\le 100$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 100$)&nbsp;— the length of the array $a$.</p><p>The second line of each test case contains $ n $ integers $ a_1,a_2,\ldots,a_n $ ($1 \le a_i \le 10^5$).</p><p>There are no constraints on the sum of $n$ over all test cases.</p>

## Output

<p>For each test case, print "<span class="tex-font-style-tt">Yes</span>" (without quotes), if it is possible to make the array good, and "<span class="tex-font-style-tt">No</span>" (without quotes) otherwise.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p>





```input1|2,3,6,7,10,11
5
2
8 9
3
1 1 2
4
1 1 4 5
5
2 3 3 3 3
4
100000 100000 100000 100000
```




```output1
Yes
Yes
No
No
Yes
```



## Note

<p>In the first test case, $[8,9]$ and $[9,8]$ are good.</p><p>In the second test case, $[1,2,1]$ is good because $a_1+a_2=a_2+a_3=3$.</p><p>In the third test case, it can be shown that no permutation is good.</p>
