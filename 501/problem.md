## Description

<div><p>You have discovered $n$ mysterious particles on a line with integer charges of $c_1,\dots,c_n$. You have a device that allows you to perform the following operation: </p><ul> <li> Choose a particle and remove it from the line. The remaining particles will shift to fill in the gap that is created. If there were particles with charges $x$ and $y$ directly to the left and right of the removed particle, they combine into a single particle of charge $x+y$. </li></ul><p>For example, if the line of particles had charges of $[-3,1,4,-1,5,-9]$, performing the operation on the $4$th particle will transform the line into $[-3,1,9,-9]$.</p><center> <img class="tex-graphics" src="file://BheWdFho.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>If we then use the device on the $1$st particle in this new line, the line will turn into $[1,9,-9]$. </p><p>You will perform operations until there is only one particle left. What is the maximum charge of this remaining particle that you can obtain?</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$).</p><p>The second line of each test case contains $n$ integers $c_1,\dots,c_n$ ($-10^9 \le c_i \le 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output one integer, the maximum charge of the remaining particle.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$).</p><p>The second line of each test case contains $n$ integers $c_1,\dots,c_n$ ($-10^9 \le c_i \le 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output one integer, the maximum charge of the remaining particle.</p>





```input1|2,3,6,7
3
6
-3 1 4 -1 5 -9
5
998244353 998244353 998244353 998244353 998244353
1
-2718
```




```output1
9
2994733059
-2718
```



## Note

<p>In the first test case, the best strategy is to use the device on the $4$th particle, then on the $1$st particle (as described in the statement), and finally use the device on the new $3$rd particle followed by the $1$st particle.</p><p>In the second test case, the best strategy is to use the device on the $4$th particle to transform the line into $[998244353,998244353,1996488706]$, then on the $2$nd particle to transform the line into $[2994733059]$. Be wary of integer overflow.</p><p>In the third test case, there is only one particle, so no operations can be performed.</p>
