## Description

<div><p>Calin has $n$ buckets, the $i$-th of which contains $a_i$ wooden squares of side length $1$.</p><p>Can Calin build a square using <span class="tex-font-style-bf">all</span> the given squares?</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 2 \cdot 10^5$)&nbsp;— the number of buckets.</p><p>The second line of each test case contains $n$ integers $a_1, \ldots, a_n$ ($1 \leq a_i \leq 10^9$)&nbsp;— the number of squares in each bucket.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if Calin can build a square using <span class="tex-font-style-bf">all</span> of the given $1 \times 1$ squares, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 2 \cdot 10^5$)&nbsp;— the number of buckets.</p><p>The second line of each test case contains $n$ integers $a_1, \ldots, a_n$ ($1 \leq a_i \leq 10^9$)&nbsp;— the number of squares in each bucket.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if Calin can build a square using <span class="tex-font-style-bf">all</span> of the given $1 \times 1$ squares, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p>





```input1|2,3,6,7,10,11
5
1
9
2
14 2
7
1 2 3 4 5 6 7
6
1 3 5 7 9 11
4
2 2 2 2
```




```output1
YES
YES
NO
YES
NO
```



## Note

<p>In the first test case, Calin can build a $3 \times 3$ square.</p><p>In the second test case, Calin can build a $4 \times 4$ square.</p><p>In the third test case, Calin cannot build a square using all the given squares.</p>
