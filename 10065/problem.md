## Description

<div><p>You are given an integer array $a$ of length $n$.</p><p>You can perform the following operation any number of times (possibly zero): take any element of the array $a$, which is at least $10$, delete it, and instead insert the digits that element consisted of in the same position, in order they appear in that element.</p><p>For example:</p><ul> <li> if we apply this operation to the $3$-rd element of the array $[12, 3, 45, 67]$, then the array becomes $[12, 3, 4, 5, 67]$. </li><li> if we apply this operation to the $2$-nd element of the array $[2, 10]$, then the array becomes $[2, 1, 0]$. </li></ul><p>Your task is to determine whether it is possible to make $a$ sorted in non-descending order using the aforementioned operation <span class="tex-font-style-bf">any number of times (possibly zero)</span>. In other words, you have to determine if it is possible to transform the array $a$ in such a way that $a_1 \le a_2 \le \dots \le a_k$, where $k$ is the current length of the array $a$.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^3$)&nbsp;— the number of test cases.</p><p>Each test case consists of two lines:</p><ul> <li> the first line contains a single integer $n$ ($2 \le n \le 50$). </li><li> the second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($0 \le a_i \le 99$). </li></ul></div><div class="output-specification"><p>For each test case, print <span class="tex-font-style-tt">YES</span> if it is possible to make $a$ sorted in non-decreasing order using the aforementioned operation; otherwise, print <span class="tex-font-style-tt">NO</span>.</p><p>You can print each letter in any case. For example, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span>, <span class="tex-font-style-tt">YeS</span> will all be recognized as a positive answer.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^3$)&nbsp;— the number of test cases.</p><p>Each test case consists of two lines:</p><ul> <li> the first line contains a single integer $n$ ($2 \le n \le 50$). </li><li> the second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($0 \le a_i \le 99$). </li></ul>

## Output

<p>For each test case, print <span class="tex-font-style-tt">YES</span> if it is possible to make $a$ sorted in non-decreasing order using the aforementioned operation; otherwise, print <span class="tex-font-style-tt">NO</span>.</p><p>You can print each letter in any case. For example, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span>, <span class="tex-font-style-tt">YeS</span> will all be recognized as a positive answer.</p>





```input1|2,3,6,7
3
4
12 3 45 67
3
12 28 5
2
0 0
```




```output1
YES
NO
YES
```



## Note

<p>In the first example, you can split the first element, then the array becomes $[1, 2, 3, 45, 67]$.</p><p>In the second example, there is no way to get a sorted array.</p><p>In the third example, the array is already sorted.</p>
