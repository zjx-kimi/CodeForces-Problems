## Description

<div><p>Eric has an array $b$ of length $m$, then he generates $n$ additional arrays $c_1, c_2, \dots, c_n$, each of length $m$, from the array $b$, by the following way:</p><p>Initially, $c_i = b$ for every $1 \le i \le n$. Eric secretly chooses an integer $k$ $(1 \le k \le n)$ and chooses $c_k$ to be the special array.</p><p>There are two operations that Eric can perform on an array $c_t$:</p><ul><li> <span class="tex-font-style-it">Operation 1</span>: Choose two integers $i$ and $j$ ($2 \leq i &lt; j \leq m-1$), subtract $1$ from both $c_t[i]$ and $c_t[j]$, and add $1$ to both $c_t[i-1]$ and $c_t[j+1]$. <span class="tex-font-style-bf">That operation can only be used on a non-special array, that is when $t \neq k$.</span>;</li><li> <span class="tex-font-style-it">Operation 2</span>: Choose two integers $i$ and $j$ ($2 \leq i &lt; j \leq m-2$), subtract $1$ from both $c_t[i]$ and $c_t[j]$, and add $1$ to both $c_t[i-1]$ and $c_t[j+2]$. <span class="tex-font-style-bf">That operation can only be used on a special array, that is when $t = k$.</span><p><span class="tex-font-style-it">Note that Eric can't perform an operation if any element of the array will become less than $0$ after that operation.</span></p></li></ul><p>Now, Eric does the following:</p><ul> <li> For every <span class="tex-font-style-bf">non-special</span> array $c_i$ ($i \neq k$), Eric uses <span class="tex-font-style-bf">only operation 1</span> on it <span class="tex-font-style-bf">at least once</span>.</li><li> For the <span class="tex-font-style-bf">special</span> array $c_k$, Eric uses <span class="tex-font-style-bf">only operation 2</span> on it <span class="tex-font-style-bf">at least once</span>.</li></ul><p>Lastly, Eric discards the array $b$.</p><p>For given arrays $c_1, c_2, \dots, c_n$, your task is to find out the special array, i.e. the value $k$. Also, you need to find the number of times of operation $2$ was used on it.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. Description of test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($3 \leq n \leq 10^5$, $7 \leq m \leq 3 \cdot 10^5$) — the number of arrays given to you, and the length of each array.</p><p>The next $n$ lines contains $m$ integers each, $c_{i,1}, c_{i,2}, \dots , c_{i,m}$.</p><p>It is guaranteed that each element of the discarded array $b$ is in the range $[0,10^6]$, and therefore $0 \leq c_{i,j} \leq 3 \cdot 10^{11}$ for all possible pairs of $(i,j)$.</p><p>It is guaranteed that the sum of $n \cdot m$ over all test cases does not exceed $10^6$.</p><p>It is guaranteed that the input is generated according to the procedure above.</p></div><div class="output-specification"><p>For each test case, output one line containing two integers — the index of the special array, and the number of times that <span class="tex-font-style-it">Operation 2</span> was performed on it. It can be shown that under the constraints given in the problem, this value is unique and won't exceed $10^{18}$, so you can represent it as a $64$-bit integer. It can also be shown that the index of the special array is uniquely determined.</p><p>In this problem, <span class="tex-font-style-bf">hacks are disabled</span>.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. Description of test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($3 \leq n \leq 10^5$, $7 \leq m \leq 3 \cdot 10^5$) — the number of arrays given to you, and the length of each array.</p><p>The next $n$ lines contains $m$ integers each, $c_{i,1}, c_{i,2}, \dots , c_{i,m}$.</p><p>It is guaranteed that each element of the discarded array $b$ is in the range $[0,10^6]$, and therefore $0 \leq c_{i,j} \leq 3 \cdot 10^{11}$ for all possible pairs of $(i,j)$.</p><p>It is guaranteed that the sum of $n \cdot m$ over all test cases does not exceed $10^6$.</p><p>It is guaranteed that the input is generated according to the procedure above.</p>

## Output

<p>For each test case, output one line containing two integers — the index of the special array, and the number of times that <span class="tex-font-style-it">Operation 2</span> was performed on it. It can be shown that under the constraints given in the problem, this value is unique and won't exceed $10^{18}$, so you can represent it as a $64$-bit integer. It can also be shown that the index of the special array is uniquely determined.</p><p>In this problem, <span class="tex-font-style-bf">hacks are disabled</span>.</p>





```input1
7
3 9
0 1 2 0 0 2 1 1 0
0 1 1 1 2 0 0 2 0
0 1 2 0 0 1 2 1 0
3 7
25 15 20 15 25 20 20
26 14 20 14 26 20 20
25 15 20 15 20 20 25
3 9
25 15 20 15 25 20 20 20 20
26 14 20 14 26 20 20 20 20
25 15 20 15 25 15 20 20 25
3 11
25 15 20 15 25 20 20 20 20 20 20
26 14 20 14 26 20 20 20 20 20 20
25 15 20 15 25 20 15 20 20 20 25
3 13
25 15 20 15 25 20 20 20 20 20 20 20 20
26 14 20 14 26 20 20 20 20 20 20 20 20
25 15 20 15 25 20 20 15 20 20 20 20 25
3 15
25 15 20 15 25 20 20 20 20 20 20 20 20 20 20
26 14 20 14 26 20 20 20 20 20 20 20 20 20 20
25 15 20 15 25 20 20 20 15 20 20 20 20 20 25
3 9
909459 479492 676924 224197 162866 164495 193268 742456 728277
948845 455424 731850 327890 304150 237351 251763 225845 798316
975446 401170 792914 272263 300770 242037 236619 334316 725899
```




```output1
3 1
3 10
3 15
3 20
3 25
3 30
1 1378716
```



## Note

<p>In the first test case, the secret array $b$ is $[0, 1, 1, 1, 1, 1, 1, 1, 0]$. Array $c_1$ and array $c_2$ are generated by using operation 1. Array $c_3$ is generated by using operation 2.</p><p>For Array $c_1$,you can choose $i=4$ and $j=5$ perform <span class="tex-font-style-it">Operation 1</span> one time to generate it. For Array $c_2$, you can choose $i=6$ and $j=7$ perform <span class="tex-font-style-it">Operation 1</span> one time to generate it. For Array $c_3$,you can choose $i=4$ and $j=5$ perform <span class="tex-font-style-it">Operation 2</span> one time to generate it.</p><p>In the second test case, the secret array $b$ is $[20, 20, 20, 20, 20, 20, 20]$. You can also find that array $c_1$ and array $c_2$ are generated by using <span class="tex-font-style-it">Operation 1</span>. Array $c_3$ is generated by using <span class="tex-font-style-it">Operation 2</span>.</p><p>In the third test case, the secret array $b$ is $[20, 20, 20, 20, 20, 20, 20, 20, 20]$. You can also find that array $c_1$ and array $c_2$ are generated by using <span class="tex-font-style-it">Operation 1</span>. Array $c_3$ is generated by using <span class="tex-font-style-it">Operation 2</span>.</p>
