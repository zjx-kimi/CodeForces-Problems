## Description

<div><p>Monocarp had a sequence $a$ consisting of $n + m$ integers $a_1, a_2, \dots, a_{n + m}$. He painted the elements into two colors, red and blue; $n$ elements were painted red, all other $m$ elements were painted blue.</p><p>After painting the elements, he has written two sequences $r_1, r_2, \dots, r_n$ and $b_1, b_2, \dots, b_m$. The sequence $r$ consisted of all red elements of $a$ <span class="tex-font-style-bf">in the order they appeared in $a$</span>; similarly, the sequence $b$ consisted of all blue elements of $a$ <span class="tex-font-style-bf">in the order they appeared in $a$ as well</span>.</p><p>Unfortunately, the original sequence was lost, and Monocarp only has the sequences $r$ and $b$. He wants to restore the original sequence. In case there are multiple ways to restore it, he wants to choose a way to restore that maximizes the value of </p><p>$$f(a) = \max(0, a_1, (a_1 + a_2), (a_1 + a_2 + a_3), \dots, (a_1 + a_2 + a_3 + \dots + a_{n + m}))$$</p><p>Help Monocarp to calculate the maximum possible value of $f(a)$.</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 1000$) — the number of test cases. Then the test cases follow. Each test case consists of four lines.</p><p>The first line of each test case contains one integer $n$ ($1 \le n \le 100$).</p><p>The second line contains $n$ integers $r_1, r_2, \dots, r_n$ ($-100 \le r_i \le 100$).</p><p>The third line contains one integer $m$ ($1 \le m \le 100$).</p><p>The fourth line contains $m$ integers $b_1, b_2, \dots, b_m$ ($-100 \le b_i \le 100$).</p></div><div class="output-specification"><p>For each test case, print one integer — the maximum possible value of $f(a)$.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 1000$) — the number of test cases. Then the test cases follow. Each test case consists of four lines.</p><p>The first line of each test case contains one integer $n$ ($1 \le n \le 100$).</p><p>The second line contains $n$ integers $r_1, r_2, \dots, r_n$ ($-100 \le r_i \le 100$).</p><p>The third line contains one integer $m$ ($1 \le m \le 100$).</p><p>The fourth line contains $m$ integers $b_1, b_2, \dots, b_m$ ($-100 \le b_i \le 100$).</p>

## Output

<p>For each test case, print one integer — the maximum possible value of $f(a)$.</p>





```input1
4
4
6 -5 7 -3
3
2 3 -4
2
1 1
4
10 -3 2 2
5
-1 -2 -3 -4 -5
5
-1 -2 -3 -4 -5
1
0
1
0
```




```output1
13
13
0
0
```



## Note

<p>In the explanations for the sample test cases, red elements are marked as <span class="tex-font-style-bf">bold</span>.</p><p>In the first test case, one of the possible sequences $a$ is $[\mathbf{6}, 2, \mathbf{-5}, 3, \mathbf{7}, \mathbf{-3}, -4]$.</p><p>In the second test case, one of the possible sequences $a$ is $[10, \mathbf{1}, -3, \mathbf{1}, 2, 2]$.</p><p>In the third test case, one of the possible sequences $a$ is $[\mathbf{-1}, -1, -2, -3, \mathbf{-2}, -4, -5, \mathbf{-3}, \mathbf{-4}, \mathbf{-5}]$.</p><p>In the fourth test case, one of the possible sequences $a$ is $[0, \mathbf{0}]$.</p>
