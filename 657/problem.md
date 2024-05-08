## Description

<div><p>To thank Ian, Mary gifted an array $a$ of length $n$ to Ian. To make himself look smart, he wants to make the array in non-decreasing order by doing the following finitely many times: he chooses two adjacent elements $a_i$ and $a_{i+1}$ ($1\le i\le n-1$), and increases both of them by $1$ or decreases both of them by $1$. Note that, the elements of the array <span class="tex-font-style-bf">can</span> become negative.</p><p>As a smart person, you notice that, there are some arrays such that Ian cannot make it become non-decreasing order! Therefore, you decide to write a program to determine if it is possible to make the array in non-decreasing order.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case consists of a single integer $n$ ($2\le n\le 3\cdot10^5$) — the number of elements in the array.</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($1\le a_i\le 10^9$) — the elements of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $3\cdot10^5$. </p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if there exists a sequence of operations which make the array non-decreasing, else output "<span class="tex-font-style-tt">NO</span>".</p><p>You may print each letter in any case (for example, "<span class="tex-font-style-tt">YES</span>", "<span class="tex-font-style-tt">Yes</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">yEs</span>" will all be recognized as positive answer).</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case consists of a single integer $n$ ($2\le n\le 3\cdot10^5$) — the number of elements in the array.</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($1\le a_i\le 10^9$) — the elements of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $3\cdot10^5$. </p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if there exists a sequence of operations which make the array non-decreasing, else output "<span class="tex-font-style-tt">NO</span>".</p><p>You may print each letter in any case (for example, "<span class="tex-font-style-tt">YES</span>", "<span class="tex-font-style-tt">Yes</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">yEs</span>" will all be recognized as positive answer).</p>





```input1|2,3,6,7,10,11
5
3
1 3 2
2
2 1
4
1 3 5 7
4
2 1 4 3
5
5 4 3 2 1
```




```output1
YES
NO
YES
NO
YES
```



## Note

<p>For the first test case, we can increase $a_2$ and $a_3$ both by $1$. The array is now $[1, 4, 3]$.</p><p>Then we can decrease $a_1$ and $a_2$ both by $1$. The array is now $[0, 3, 3]$, which is sorted in non-decreasing order. So the answer is "<span class="tex-font-style-tt">YES</span>".</p><p>For the second test case, no matter how Ian perform the operations, $a_1$ will always be larger than $a_2$. So the answer is "<span class="tex-font-style-tt">NO</span>" and Ian cannot pretend to be smart.</p><p>For the third test case, the array is already in non-decreasing order, so Ian does not need to do anything.</p>
