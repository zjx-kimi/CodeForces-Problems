## Description

<div><p>Initially, you have an empty multiset of segments. You need to process $q$ operations of two types:</p><ul><li> $+$ $l$ $r$ — Add the segment $(l, r)$ to the multiset,</li><li> $-$ $l$ $r$ — Remove <span class="tex-font-style-bf">exactly</span> one segment $(l, r)$ from the multiset. It is guaranteed that this segment exists in the multiset.</li></ul><p>After each operation, you need to determine if there exists a pair of segments in the multiset that do not intersect. A pair of segments $(l, r)$ and $(a, b)$ do not intersect if there does not exist a point $x$ such that $l \leq x \leq r$ and $a \leq x \leq b$.</p></div><div class="input-specification"><p>The first line of each test case contains an integer $q$ ($1 \leq q \leq 10^5$) — the number of operations.</p><p>The next $q$ lines describe two types of operations. If it is an addition operation, it is given in the format $+$ $l$ $r$. If it is a deletion operation, it is given in the format $-$ $l$ $r$ ($1 \leq l \leq r \leq 10^9$).</p></div><div class="output-specification"><p>After each operation, print "<span class="tex-font-style-tt">YES</span>" if there exists a pair of segments in the multiset that do not intersect, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can print the answer in any case (uppercase or lowercase). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive answers.</p></div>

## Input

<p>The first line of each test case contains an integer $q$ ($1 \leq q \leq 10^5$) — the number of operations.</p><p>The next $q$ lines describe two types of operations. If it is an addition operation, it is given in the format $+$ $l$ $r$. If it is a deletion operation, it is given in the format $-$ $l$ $r$ ($1 \leq l \leq r \leq 10^9$).</p>

## Output

<p>After each operation, print "<span class="tex-font-style-tt">YES</span>" if there exists a pair of segments in the multiset that do not intersect, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can print the answer in any case (uppercase or lowercase). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive answers.</p>





```input1|
12
+ 1 2
+ 3 4
+ 2 3
+ 2 2
+ 3 4
- 3 4
- 3 4
- 1 2
+ 3 4
- 2 2
- 2 3
- 3 4
```




```output1
NO
YES
YES
YES
YES
YES
NO
NO
YES
NO
NO
NO
```



## Note

<p>In the example, after the second, third, fourth, and fifth operations, there exists a pair of segments $(1, 2)$ and $(3, 4)$ that do not intersect.</p><p>Then we remove exactly one segment $(3, 4)$, and by that time we had two segments. Therefore, the answer after this operation also exists.</p>
