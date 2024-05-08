## Description

<div><p>You had a sequence $a_1, a_2, \ldots, a_n$ consisting of integers from $1$ to $n$, not necessarily distinct. For some unknown reason, you decided to calculate the following <span class="tex-font-style-it">characteristic</span> of the sequence: </p><ul> <li> Let $r_i$ ($1 \le i \le n$) be the smallest $j \ge i$ such that on the subsegment $a_i, a_{i+1}, \ldots, a_j$ all distinct numbers from the sequence $a$ appear. More formally, for any $k \in [1, n]$, there exists $l \in [i, j]$ such that $a_k = a_l$. If such $j$ does not exist, $r_i$ is considered to be equal to $n+1$. </li><li> The characteristic of the sequence $a$ is defined as the sequence $r_1, r_2, \ldots, r_n$. </li></ul> Unfortunately, the sequence $a$ got lost, but you still have its characteristic $r$. You want to reconstruct any sequence $a$ that matches the characteristic, or determine that there is an error in the characteristic and such a sequence does not exist.</div><div class="input-specification"><p>Each test consist of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the lost sequence $a$.</p><p>The second line of each test case contains $n$ integers $r_1, r_2, \ldots, r_n$ ($i \le r_i \le n+1$)&nbsp;— the characteristic of the lost sequence $a$. </p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output the following: </p><ul> <li> If there is no sequence $a$ with the characteristic $r$, print "<span class="tex-font-style-tt">No</span>". </li><li> Otherwise, print "<span class="tex-font-style-tt">Yes</span>" on the first line, and on the second line, print any sequence of integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le n$) that matches the characteristic $r$. </li></ul> You can output "<span class="tex-font-style-tt">YES</span>" and "<span class="tex-font-style-tt">NO</span>" in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</div>

## Input

<p>Each test consist of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the lost sequence $a$.</p><p>The second line of each test case contains $n$ integers $r_1, r_2, \ldots, r_n$ ($i \le r_i \le n+1$)&nbsp;— the characteristic of the lost sequence $a$. </p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output the following: </p><ul> <li> If there is no sequence $a$ with the characteristic $r$, print "<span class="tex-font-style-tt">No</span>". </li><li> Otherwise, print "<span class="tex-font-style-tt">Yes</span>" on the first line, and on the second line, print any sequence of integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le n$) that matches the characteristic $r$. </li></ul> You can output "<span class="tex-font-style-tt">YES</span>" and "<span class="tex-font-style-tt">NO</span>" in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).





```input1|2,3,6,7,10,11
5
3
2 3 4
5
2 3 5 4 6
1
1
3
1 3 4
8
3 6 6 6 8 9 9 9
```




```output1
Yes
1 2 1
No
Yes
1 
No
Yes
1 3 5 3 5 1 1 3
```



## Note

<p>In the first test case, the sequence $a = [1, 2, 1]$ is suitable. The integers $1$ and $2$ appear on the subsegments $[1, 2]$ and $[2, 3]$.</p><p>In the second test case, it can be proved that there is no suitable sequence $a$.</p>
