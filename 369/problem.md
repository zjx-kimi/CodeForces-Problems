## Description

<div><p>Egor has an array $a$ of length $n$, initially consisting of zeros. However, he wanted to turn it into another array $b$ of length $n$.</p><p>Since Egor doesn't take easy paths, only the following operation can be used (possibly zero or several times):</p><ul> <li> choose an array $l$ of length $k$ ($1 \leq l_i \leq n$, all $l_i$ are <span class="tex-font-style-bf">distinct</span>) and change each element $a_{l_i}$ to $l_{(i\%k)+1}$ ($1 \leq i \leq k$). </li></ul><p>He became interested in whether it is possible to get the array $b$ using only these operations. Since Egor is still a beginner programmer, he asked you to help him solve this problem.</p><p>The operation $\%$ means taking the remainder, that is, $a\%b$ is equal to the remainder of dividing the number $a$ by the number $b$.</p></div><div class="input-specification"><p>The first line of the input contains an integer $t$ ($1 \leq t \leq 10^5$) - the number of test cases.</p><p>Each test case consists of two lines. The first line contains two integers $n$ and $k$ ($1 \leq k \leq n \leq 10^5$).</p><p>The second line contains the array $b_1, b_2, \ldots, b_n$ ($1 \leq b_i \leq n$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output <span class="tex-font-style-tt">"YES"</span> (without quotes) if there is a way to get the array $b$ using only the given operation. Otherwise, output <span class="tex-font-style-tt">"NO"</span> (without quotes). You can output each letter in any case (lowercase or uppercase). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be accepted as a positive answer.</p></div>

## Input

<p>The first line of the input contains an integer $t$ ($1 \leq t \leq 10^5$) - the number of test cases.</p><p>Each test case consists of two lines. The first line contains two integers $n$ and $k$ ($1 \leq k \leq n \leq 10^5$).</p><p>The second line contains the array $b_1, b_2, \ldots, b_n$ ($1 \leq b_i \leq n$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output <span class="tex-font-style-tt">"YES"</span> (without quotes) if there is a way to get the array $b$ using only the given operation. Otherwise, output <span class="tex-font-style-tt">"NO"</span> (without quotes). You can output each letter in any case (lowercase or uppercase). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be accepted as a positive answer.</p>





```input1|2,3,6,7,10,11
6
5 3
2 3 5 3 4
4 2
2 4 3 1
1 1
1
3 1
1 2 3
5 3
5 4 3 2 1
6 1
1 2 3 1 5 6
```




```output1
YES
NO
YES
YES
NO
NO
```



## Note

<p>Let's consider the first example: </p><ul> <li> Apply the operation with $l$ = $[1,2,3]$. Now $a$ = $[2,3,1,0,0]$. </li><li> Apply the operation with $l$ = $[3,5,4]$. Now $a$ = $[2,3,5,3,4]$ = $b$. </li></ul> We see that it is possible to get the array $b$. Therefore, the answer is <span class="tex-font-style-tt">YES</span>.<p>In the second example, it can be proven that the array $b$ cannot be obtained, therefore the answer is <span class="tex-font-style-tt">NO</span>.</p>
