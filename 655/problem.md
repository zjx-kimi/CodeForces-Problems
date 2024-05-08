## Description

<div><p>You are given an integer $n$, as well as $m$ pairs of integers $(a_i,b_i)$, where $1\leq a_i , b_i \leq n$, $a_i \ne b_i$.</p><p>You want to construct a sequence satisfying the following requirements:</p><ul> <li> All elements in the sequence are integers between $1$ and $n$. </li><li> There is exactly one element with value $1$ in the sequence. </li><li> For each $i$ ($1 \le i \le m$), between any two elements (on different positions) in the sequence with value $a_i$, there is at least one element with value $b_i$. </li><li> The sequence constructed has the <span class="tex-font-style-bf">maximum</span> length among all possible sequences satisfying the above properties. </li></ul><p>Sometimes, it is possible that such a sequence can be arbitrarily long, in which case you should output "<span class="tex-font-style-tt">INFINITE</span>". Otherwise, you should output "<span class="tex-font-style-tt">FINITE</span>" and the sequence itself. If there are multiple possible constructions that yield the maximum length, output any.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 300$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \le n \le 1500$, $0 \le m \le 5000$) — the maximum possible value of the element of the sequence and the number of pairs.</p><p>The $i$-th of the next $m$ lines contain two integers $a_i$ and $b_i$ ($1 \le a_i , b_i \le n$, $a_i \ne b_i$).</p><p>$(a_i, b_i) \ne (a_j, b_j)$ for all $1 \le i &lt; j \le m$.</p><p>It is guaranteed that sum of $n$ over all test cases doesn't exceed $1500$ and the sum of $m$ over all test cases doesn't exceed $5000$.</p></div><div class="output-specification"><p>For each test case, on the first line output "<span class="tex-font-style-tt">INFINITE</span>" if the sequence can be arbitrarily long, and "<span class="tex-font-style-tt">FINITE</span>" otherwise.</p><p>If you have outputted "<span class="tex-font-style-tt">FINITE</span>", then your output should be followed by $2$ lines.</p><p>The first line contains an integer $s$, the maximum length of the sequence.</p><p>The second line contains $s$ integers, each are between $1$ and $n$ inclusive, representing the elements of the sequence.</p><p>If there are multiple sequences with the maximum length, output any of them.</p><p>It can be shown that, for all test cases with answer "<span class="tex-font-style-tt">FINITE</span>", then under the constraints, the maximum possible sum of sequence lengths of those test cases does not exceed $2\cdot10^6$.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 300$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \le n \le 1500$, $0 \le m \le 5000$) — the maximum possible value of the element of the sequence and the number of pairs.</p><p>The $i$-th of the next $m$ lines contain two integers $a_i$ and $b_i$ ($1 \le a_i , b_i \le n$, $a_i \ne b_i$).</p><p>$(a_i, b_i) \ne (a_j, b_j)$ for all $1 \le i &lt; j \le m$.</p><p>It is guaranteed that sum of $n$ over all test cases doesn't exceed $1500$ and the sum of $m$ over all test cases doesn't exceed $5000$.</p>

## Output

<p>For each test case, on the first line output "<span class="tex-font-style-tt">INFINITE</span>" if the sequence can be arbitrarily long, and "<span class="tex-font-style-tt">FINITE</span>" otherwise.</p><p>If you have outputted "<span class="tex-font-style-tt">FINITE</span>", then your output should be followed by $2$ lines.</p><p>The first line contains an integer $s$, the maximum length of the sequence.</p><p>The second line contains $s$ integers, each are between $1$ and $n$ inclusive, representing the elements of the sequence.</p><p>If there are multiple sequences with the maximum length, output any of them.</p><p>It can be shown that, for all test cases with answer "<span class="tex-font-style-tt">FINITE</span>", then under the constraints, the maximum possible sum of sequence lengths of those test cases does not exceed $2\cdot10^6$.</p>





```input1|2,3,4,6,10,11,12,13,14,15
5
3 2
3 1
2 1
1 0
2 0
2 2
1 2
2 1
5 5
2 1
3 1
4 2
4 5
5 1
```




```output1
FINITE
5
2 3 1 2 3 
FINITE
1
1 
INFINITE
FINITE
3
2 1 2 
FINITE
10
4 2 3 5 4 1 3 2 5 4
```



## Note

<p>In the first test case, there is an element $1$ between two elements with value $3$ and an element $1$ between two elements with value $2$. It can be shown that there is no suitable sequences of length more than $5$.</p><p>In the second case, $[1]$ is the only possible sequence because there should be exactly one element with value $1$ in the sequence.</p><p>In the third case, we can get an arbitrary long sequence like $1, 2, 2, 2, \ldots$.</p>
