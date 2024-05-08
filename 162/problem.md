## Description

<div><p><span class="tex-font-style-bf">This is the hard version of the problem. The only differences between the two versions of this problem are the constraints on $n$ and the time limit. You can make hacks only if all versions of the problem are solved.</span></p><p>You are given two arrays $a$ and $b$ of length $n$.</p><p>You can perform the following operation some (possibly zero) times: </p><ol> <li> choose $l$ and $r$ such that $1 \leq l \leq r \leq n$. </li><li> let $x=\max(a_l,a_{l+1},\ldots,a_r)$. </li><li> for all $l \leq i \leq r$, set $a_i := x$. </li></ol><p>Determine if you can make array $a$ equal to array $b$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the arrays.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le n$)&nbsp;— the elements of array $a$.</p><p>The third line contains $n$ integers $b_1, b_2, \ldots, b_n$ ($1 \le b_i \le n$)&nbsp;— the elements of array $b$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" (without quotes) if you can make $a$ into $b$ using any number of operations, and "<span class="tex-font-style-tt">NO</span>" (without quotes) otherwise.</p><p>You can output "<span class="tex-font-style-tt">YES</span>" and "<span class="tex-font-style-tt">NO</span>" in any case (for example, strings "<span class="tex-font-style-tt">yES</span>", "<span class="tex-font-style-tt">yes</span>" and "<span class="tex-font-style-tt">Yes</span>" will be recognized as a positive response).</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the arrays.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le n$)&nbsp;— the elements of array $a$.</p><p>The third line contains $n$ integers $b_1, b_2, \ldots, b_n$ ($1 \le b_i \le n$)&nbsp;— the elements of array $b$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" (without quotes) if you can make $a$ into $b$ using any number of operations, and "<span class="tex-font-style-tt">NO</span>" (without quotes) otherwise.</p><p>You can output "<span class="tex-font-style-tt">YES</span>" and "<span class="tex-font-style-tt">NO</span>" in any case (for example, strings "<span class="tex-font-style-tt">yES</span>", "<span class="tex-font-style-tt">yes</span>" and "<span class="tex-font-style-tt">Yes</span>" will be recognized as a positive response).</p>





```input1|2,3,4,8,9,10,14,15,16
5
5
1 2 3 2 4
1 3 3 2 4
5
3 4 2 2 4
3 4 3 4 4
5
3 2 1 1 1
3 3 3 2 2
2
1 1
1 2
3
1 1 2
2 1 2
```




```output1
YES
NO
YES
NO
NO
```



## Note

<p>In the first test case, we can achieve array $b$ by applying a single operation: $(l,r)=(2,3)$.</p><p>In the second test case, it can be shown we cannot achieve array $b$ in any amount of operations.</p><p>In the third test case, we can achieve array $b$ by applying two operations: $(l,r)=(2,5)$. followed by $(l,r)=(1,3)$.</p><p>In the fourth and fifth test cases, it can be shown we cannot achieve array $b$ in any amount of operations.</p>
