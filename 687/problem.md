## Description

<div><p>A sequence of $m$ integers $a_{1}, a_{2}, \ldots, a_{m}$ is <span class="tex-font-style-it">good</span>, if and only if there exists at least one $i$ ($1 \le i \le m$) such that $a_{i} = i$. For example, $[3,2,3]$ is a good sequence, since $a_{2} = 2$, $a_{3} = 3$, while $[3,1,1]$ is not a good sequence, since there is no $i$ such that $a_{i} = i$.</p><p>A sequence $a$ is <span class="tex-font-style-it">beautiful</span>, if and only if there exists at least one subsequence of $a$ satisfying that this subsequence is good. For example, $[4,3,2]$ is a beautiful sequence, since its subsequence $[4,2]$ is good, while $[5,3,4]$ is not a beautiful sequence.</p><p>A sequence $b$ is a subsequence of a sequence $a$ if $b$ can be obtained from $a$ by the deletion of several (possibly, zero or all) elements. </p><p>Now you are given a sequence, check whether it is beautiful or not.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 500$) — the number of test cases. Their description follows.</p><p>The first line of each test case contains an integer $n$ ($1 \le n \le 100$) — the length of the given sequence.</p><p>The second line of each test case contains $n$ integers $a_{1}, a_{2}, \ldots, a_{n}$ ($1 \le a_{i} \le 10^9$), representing the sequence.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" or "<span class="tex-font-style-tt">NO</span>"(without quotes) in one line, representing whether the given sequence is beautiful.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 500$) — the number of test cases. Their description follows.</p><p>The first line of each test case contains an integer $n$ ($1 \le n \le 100$) — the length of the given sequence.</p><p>The second line of each test case contains $n$ integers $a_{1}, a_{2}, \ldots, a_{n}$ ($1 \le a_{i} \le 10^9$), representing the sequence.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" or "<span class="tex-font-style-tt">NO</span>"(without quotes) in one line, representing whether the given sequence is beautiful.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p>





```input1|2,3,6,7,10,11,14,15
7
3
3 2 1
4
2 4 3 5
5
2 3 5 5 6
2
3 1
5
2 4 5 2 3
4
5 6 7 8
6
6 5 4 3 2 1
```




```output1
YES
YES
NO
YES
YES
NO
YES
```



## Note

<p>In the first test case, the good subsequence is $b=[3,2]$, where $b_{2} = 2$.</p><p>In the second test case, the good subsequence is $b=[2,4,3]$, where $b_{3} = 3$.</p><p>In the fourth test case, the good subsequence is $b=[1]$, where $b_{1} = 1$.</p><p>In the fifth test case, the good subsequence is $b=[2,2]$, where $b_{2} = 2$.</p>
