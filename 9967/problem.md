## Description

<div><p>Bob has a rectangle of size $a \times b$. He tries to cut this rectangle into two rectangles with integer sides by making a cut parallel to one of the sides of the original rectangle. Then Bob tries to form some <span class="tex-font-style-bf">other</span> rectangle from the two resulting rectangles, and he can rotate and move these two rectangles as he wishes.</p><p>Note that if two rectangles differ only by a $90^{\circ}$ rotation, they are considered <span class="tex-font-style-bf">the same</span>. For example, the rectangles $6 \times 4$ and $4 \times 6$ are considered the same.</p><p>Thus, from the $2 \times 6$ rectangle, another rectangle can be formed, because it can be cut into two $2 \times 3$ rectangles, and then these two rectangles can be used to form the $4 \times 3$ rectangle, which is different from the $2 \times 6$ rectangle.</p><center> <img class="tex-graphics" src="file://iLsbweBN.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>However, from the $2 \times 1$ rectangle, another rectangle cannot be formed, because it can only be cut into two rectangles of $1 \times 1$, and from these, only the $1 \times 2$ and $2 \times 1$ rectangles can be formed, which are considered the same.</p><center> <img class="tex-graphics" src="file://NF0RG5oP.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>Help Bob determine if he can obtain some other rectangle, or if he is just wasting his time.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. This is followed by the description of the test cases.</p><p>The single line of each test case contains two integers $a$ and $b$ ($1 \le a, b \le 10^9$) — the size of Bob's rectangle.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">Yes</span>" if Bob can obtain another rectangle from the $a \times b$ rectangle. Otherwise, output "<span class="tex-font-style-tt">No</span>".</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive answers.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. This is followed by the description of the test cases.</p><p>The single line of each test case contains two integers $a$ and $b$ ($1 \le a, b \le 10^9$) — the size of Bob's rectangle.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">Yes</span>" if Bob can obtain another rectangle from the $a \times b$ rectangle. Otherwise, output "<span class="tex-font-style-tt">No</span>".</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive answers.</p>





```input1|2,4,6,8
7
1 1
2 1
2 6
3 2
2 2
2 4
6 3
```




```output1
No
No
Yes
Yes
Yes
Yes
No
```



## Note

<p>In the first test case, the $1 \times 1$ rectangle cannot be cut into two rectangles, so another rectangle cannot be obtained from it.</p><p>In the fourth test case, the $3 \times 2$ rectangle can be cut into two $3 \times 1$ rectangles, and from these, the $1 \times 6$ rectangle can be formed.</p><p>In the fifth test case, the $2 \times 2$ rectangle can be cut into two $1 \times 2$ rectangles, and from these, the $1 \times 4$ rectangle can be formed.</p>
