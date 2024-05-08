## Description

<div><p><span class="tex-font-style-it">To prepare her "Takodachi" dumbo octopuses for world domination, Ninomae Ina'nis, a.k.a. Ina of the Mountain, orders Hoshimachi Suisei to throw boulders at them. Ina asks you, Kiryu Coco, to help choose where the boulders are thrown.</span></p><p>There are $n$ octopuses on a single-file trail on Ina's mountain, numbered $1, 2, \ldots, n$. The $i$-th octopus has a certain initial health value $a_i$, where $1 \leq a_i \leq k$.</p><p>Each boulder crushes consecutive octopuses with indexes $l, l+1, \ldots, r$, where $1 \leq l \leq r \leq n$. You can choose the numbers $l$ and $r$ arbitrarily for each boulder.</p><p>For each boulder, the health value of each octopus the boulder crushes is reduced by $1$. However, as octopuses are immortal, once they reach a health value of $0$, they will immediately regenerate to a health value of $k$. </p><p>Given the octopuses' initial health values, find the <span class="tex-font-style-bf">minimum</span> number of boulders that need to be thrown to make the health of all octopuses equal to $k$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le n \le 2 \cdot 10^5$, $1 \le k \le 10^9$)&nbsp;– the number of octopuses, and the upper bound of a octopus's health value.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le k$)&nbsp;– the initial health values of the octopuses.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output the <span class="tex-font-style-bf">minimum</span> number of boulders that need to be thrown to make the health values of all octopuses equal to $k$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le n \le 2 \cdot 10^5$, $1 \le k \le 10^9$)&nbsp;– the number of octopuses, and the upper bound of a octopus's health value.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le k$)&nbsp;– the initial health values of the octopuses.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output the <span class="tex-font-style-bf">minimum</span> number of boulders that need to be thrown to make the health values of all octopuses equal to $k$.</p>





```input1|2,3
2
4 3
1 2 1 3
7 3
1 2 3 1 3 2 1
```




```output1
2
4
```



## Note

<p>In the first test case, the minimum number of boulders thrown is $2$: </p><ul> <li> Throw the first boulder between $[l,r] = [1,3]$. Then, the octopuses' health values become $[3, 1, 3, 3]$. </li><li> Throw the second boulder between $[l,r] = [2,2]$. Then, the octopuses' health values become $[3, 3, 3, 3]$. </li></ul><p>In the second test case, the minimum number of boulders thrown is $4$. The $[l,r]$ ranges are $[1,7], [2, 6], [3, 5], [4, 4]$.</p>
