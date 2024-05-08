## Description

<div><p>Jonathan is fighting against DIO's Vampire minions. There are $n$ of them with strengths $a_1, a_2, \dots, a_n$. $\def\and {{\,\texttt{&amp;}\,}}$</p><p>Denote $(l, r)$ as the group consisting of the vampires with indices from $l$ to $r$. Jonathan realizes that the <span class="tex-font-style-it">strength</span> of any such group is in its weakest link, that is, the bitwise AND. More formally, the <span class="tex-font-style-it">strength</span> level of the group $(l, r)$ is defined as $$f(l,r) = a_l \and a_{l+1} \and a_{l+2} \and \ldots \and a_r.$$ Here, $\and$ denotes the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#AND">bitwise AND operation</a>. </p><p>Because Jonathan would like to defeat the vampire minions fast, he will divide the vampires into contiguous groups, such that each vampire is in <span class="tex-font-style-bf">exactly</span> one group, and the <span class="tex-font-style-bf">sum</span> of <span class="tex-font-style-it">strengths</span> of the groups is <span class="tex-font-style-bf">minimized</span>. Among all ways to divide the vampires, he would like to find the way with the <span class="tex-font-style-bf">maximum</span> number of groups.</p><p>Given the strengths of each of the $n$ vampires, find the <span class="tex-font-style-bf">maximum number</span> of groups among all possible ways to divide the vampires with the smallest sum of <span class="tex-font-style-it">strengths</span>.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ $(1 \leq t \leq 10^4)$ — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 2 \cdot 10^5$)&nbsp;— the number of vampires.</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($0 \leq a_i \leq 10^9$)&nbsp;— the individual strength of each vampire.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the maximum number of groups among all possible ways to divide the vampires with the smallest sum of <span class="tex-font-style-it">strengths</span>.</p></div>

## Input

<p>The first line contains a single integer $t$ $(1 \leq t \leq 10^4)$ — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 2 \cdot 10^5$)&nbsp;— the number of vampires.</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($0 \leq a_i \leq 10^9$)&nbsp;— the individual strength of each vampire.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the maximum number of groups among all possible ways to divide the vampires with the smallest sum of <span class="tex-font-style-it">strengths</span>.</p>





```input1|2,3,6,7
3
3
1 2 3
5
2 3 1 5 2
4
5 7 12 6
```




```output1
1
2
1
```



## Note

<p>In the first test case, the optimal way is to take all the $n$ vampires as a group. So, $f(1,3) = 1 \and 2 \and 3 = 0$.</p><p>In the second test case, the optimal way is to make $2$ groups, $(2,3,1)$ and $(5,2)$. So, $f(1,3) + f(4,5) = (2 \and 3 \and 1) + (5 \and 2) = 0 + 0 = 0$.</p>
