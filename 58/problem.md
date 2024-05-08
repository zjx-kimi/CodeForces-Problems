## Description

<div><p>You were given only one number, $n$. It didn't seem interesting to you, so you wondered if it's possible to come up with an array of length $n$ consisting of non-zero integers, such that if each element of the array is replaced by the sum of its neighbors (the elements on the ends are replaced by their only neighbors), you obtain a permutation of the numbers in the original array.</p></div><div class="input-specification"><p>Each test case contains only one number, $n$ ($2 \leq n \leq 10^6$).</p></div><div class="output-specification"><p>If a solution exists, output <span class="tex-font-style-tt">"YES"</span> (without quotes), followed by an array $a$ ($-10^9 \leq a_i \leq 10^9, a_i \neq 0$) that satisfies the condition of the problem. If there are multiple possible answers, output any of them.</p><p>If there is no suitable array, output <span class="tex-font-style-tt">"NO"</span> (without quotes).</p><p>The words <span class="tex-font-style-tt">"YES"</span> and <span class="tex-font-style-tt">"NO"</span> can be output in any case, for example, <span class="tex-font-style-tt">"YES"</span>, <span class="tex-font-style-tt">"Yes"</span>, <span class="tex-font-style-tt">"yEs"</span>, and so on.</p></div>

## Input

<p>Each test case contains only one number, $n$ ($2 \leq n \leq 10^6$).</p>

## Output

<p>If a solution exists, output <span class="tex-font-style-tt">"YES"</span> (without quotes), followed by an array $a$ ($-10^9 \leq a_i \leq 10^9, a_i \neq 0$) that satisfies the condition of the problem. If there are multiple possible answers, output any of them.</p><p>If there is no suitable array, output <span class="tex-font-style-tt">"NO"</span> (without quotes).</p><p>The words <span class="tex-font-style-tt">"YES"</span> and <span class="tex-font-style-tt">"NO"</span> can be output in any case, for example, <span class="tex-font-style-tt">"YES"</span>, <span class="tex-font-style-tt">"Yes"</span>, <span class="tex-font-style-tt">"yEs"</span>, and so on.</p>





```input1|
4
```




```input2|
5
```




```output1
YES
1 2 -2 -1
```




```output2
NO
```



## Note

<p>In the first test, the array [$1, 2, -2, -1$] is suitable, because if each element is replaced by the sum of its neighbors, the resulting array is [$2, -1, 1, -2$], which is a permutation of the original array.</p><p>In the second test, it can be shown that there is no solution.</p>
