## Description

<div><p>There is a rectangular sheet of paper with initial height $n$ and width $m$. Let the current height and width be $h$ and $w$ respectively. We introduce a $xy$-coordinate system so that the four corners of the sheet are $(0, 0), (w, 0), (0, h)$, and $(w, h)$. The sheet can then be cut along the lines $x = 1,2,\ldots,w-1$ and the lines $y = 1,2,\ldots,h-1$. In each step, the paper is cut randomly along any one of these $h+w-2$ lines. After each vertical and horizontal cut, the right and bottom piece of paper respectively are discarded.</p><p>Find the expected number of steps required to make the area of the sheet of paper strictly less than $k$. It can be shown that this answer can always be expressed as a fraction $\dfrac{p}{q}$ where $p$ and $q$ are coprime integers. Calculate $p\cdot q^{-1} \bmod (10^9+7)$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 57000$). Description of the test cases follows.</p><p>The first line of each test case contains 3 integers $n$, $m$, and $k$ ($1 \le n, m \le 10^6$, $2 \le k \le 10^{12}$).</p><p>It is guaranteed that the sum of $n$ and the sum of $m$ over all test cases do not exceed $10^6$.</p></div><div class="output-specification"><p>For each test case, print one integer — the answer to the problem.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 57000$). Description of the test cases follows.</p><p>The first line of each test case contains 3 integers $n$, $m$, and $k$ ($1 \le n, m \le 10^6$, $2 \le k \le 10^{12}$).</p><p>It is guaranteed that the sum of $n$ and the sum of $m$ over all test cases do not exceed $10^6$.</p>

## Output

<p>For each test case, print one integer — the answer to the problem.</p>





```input1|2,4
4
2 4 10
2 4 8
2 4 2
2 4 6
```




```output1
0
1
833333342
250000003
```



## Note

<p>For the first test case, the area is already less than $10$ so no cuts are required.</p><p>For the second test case, the area is exactly $8$ so any one of the $4$ possible cuts would make the area strictly less than $8$.</p><p>For the third test case, the final answer is $\frac{17}{6} = 833\,333\,342\bmod (10^9+7)$.</p><p>For the fourth test case, the final answer is $\frac{5}{4} = 250\,000\,003\bmod (10^9+7)$.</p>
