## Description

<div><p>Suneet has three digits $a$, $b$, and $c$. </p><p>Since math isn't his strongest point, he asks you to determine if you can choose any two digits to make a sum greater or equal to $10$.</p><p>Output "<span class="tex-font-style-tt">YES</span>" if there is such a pair, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains three digits $a$, $b$, $c$ ($0 \leq a, b, c \leq 9$).</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if such a pair exists, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains three digits $a$, $b$, $c$ ($0 \leq a, b, c \leq 9$).</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if such a pair exists, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p>





```input1|2,4,6
5
8 1 2
4 4 5
9 9 9
0 0 0
8 5 3
```




```output1
YES
NO
YES
NO
YES
```



## Note

<p>For the first test case, by choosing the digits $8$ and $2$ we can obtain a sum of $8 + 2 = 10$ which satisfies the condition, thus the output should be "<span class="tex-font-style-tt">YES</span>".</p><p>For the second test case, any combination of chosen digits won't be at least $10$, thus the output should be "<span class="tex-font-style-tt">NO</span>" (note that we can not choose the digit on the same position twice).</p><p>For the third test case, any combination of chosen digits will have a sum equal to $18$, thus the output should be "<span class="tex-font-style-tt">YES</span>".</p>
