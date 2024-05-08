## Description

<div><p>Iulia has $n$ glasses arranged in a line. The $i$-th glass has $a_i$ units of juice in it. Iulia drinks only from odd-numbered glasses, while her date drinks only from even-numbered glasses.</p><p>To impress her date, Iulia wants to find a contiguous subarray of these glasses such that both Iulia and her date will have the same amount of juice in total if only the glasses in this subarray are considered. Please help her to do that.</p><p>More formally, find out if there exists two indices $l$, $r$ such that $1 \leq l \leq r \leq n$, and $a_l + a_{l + 2} + a_{l + 4} + \dots + a_{r} = a_{l + 1} + a_{l + 3} + \dots + a_{r-1}$ if $l$ and $r$ have the same parity and $a_l + a_{l + 2} + a_{l + 4} + \dots + a_{r - 1} = a_{l + 1} + a_{l + 3} + \dots + a_{r}$ otherwise.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 2 \cdot 10^5$)&nbsp;— the total number of glasses.</p><p>The second line of each test case contains $n$ integers $a_1, \ldots, a_n$ ($1 \leq a_i \leq 10^9$)&nbsp;— the amount of juice in each glass.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if there exists a subarray satisfying the condition, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 2 \cdot 10^5$)&nbsp;— the total number of glasses.</p><p>The second line of each test case contains $n$ integers $a_1, \ldots, a_n$ ($1 \leq a_i \leq 10^9$)&nbsp;— the amount of juice in each glass.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if there exists a subarray satisfying the condition, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p>





```input1|2,3,6,7,10,11
6
3
1 3 2
6
1 1 1 1 1 1
10
1 6 9 8 55 3 14 2 7 2
8
1 2 11 4 1 5 1 2
6
2 6 1 5 7 8
9
2 5 10 4 4 9 6 7 8
```




```output1
YES
YES
NO
YES
NO
YES
```



## Note

<p>In the first test case, Iulia can pick $l=1$ and $r=3$. Then she drinks $a_1+a_3=1+2=3$ units and her date drinks $a_2=3$ units of juice.</p><p>In the second test case, Iulia can pick $l=2$ and $r=5$. Then she drinks $a_3+a_5=1+1=2$ units and her date drinks $a_2+a_4=1+1=2$ units of juice.</p><p>In the third test case no such contiguous subarray works.</p><p>In the fourth test case, Iulia can pick $l=2$ and $r=8$. Then she drinks $a_3+a_5+a_7=11+1+1=13$ units and her date drinks $a_2+a_4+a_6+a_8=2+4+5+2=13$ units of juice.</p>
