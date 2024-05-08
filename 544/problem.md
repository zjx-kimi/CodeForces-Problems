## Description

<div><p>Two integers were written on a blackboard. After that, the following step was carried out $n-2$ times:</p><ul> <li> Select any two integers on the board, and write the absolute value of their difference on the board. </li></ul><p>After this process was complete, the list of $n$ integers was shuffled. You are given the final list. Recover <span class="tex-font-style-bf">one</span> of the initial two numbers. You do <span class="tex-font-style-bf">not</span> need to recover the other one.</p><p>You are guaranteed that the input can be generated using the above process.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 100$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($3 \le n \le 100$)&nbsp;— the size of the final list.</p><p>The next line of each test case contains $n$ integers $a_1, a_2, \ldots a_n$ ($-10^9 \le a_i \le 10^9$)&nbsp;— the shuffled list of numbers written on the blackboard.</p><p>It is guaranteed that the input was generated using the process described above.</p></div><div class="output-specification"><p>For each test case, output a single integer $x$&nbsp;— one of the two initial numbers on the blackboard.</p><p>If there are multiple solutions, print any of them.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 100$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($3 \le n \le 100$)&nbsp;— the size of the final list.</p><p>The next line of each test case contains $n$ integers $a_1, a_2, \ldots a_n$ ($-10^9 \le a_i \le 10^9$)&nbsp;— the shuffled list of numbers written on the blackboard.</p><p>It is guaranteed that the input was generated using the process described above.</p>

## Output

<p>For each test case, output a single integer $x$&nbsp;— one of the two initial numbers on the blackboard.</p><p>If there are multiple solutions, print any of them.</p>





```input1|2,3,6,7,10,11,14,15,18,19
9
3
9 2 7
3
15 -4 11
4
-9 1 11 -10
5
3 0 0 0 3
7
8 16 8 0 8 16 8
4
0 0 0 0
10
27 1 24 28 2 -1 26 25 28 27
6
600000000 800000000 0 -200000000 1000000000 800000000
3
0 -1000000000 1000000000
```




```output1
9
11
-9
3
8
0
-1
600000000
0
```



## Note

<p>For the first test case, $a$ can be produced by starting with either $9$ and $2$, and then writing down $|9-2|=7$, or starting with $9$ and $7$ and writing down $|9-7|=2$. So $2$, $7$, and $9$ are all valid answers, because they all appear in at least one valid pair.</p><p>For the second test case, we can show that the two initial numbers must have been $-4$ and $11$.</p><p>For the fourth test case, the starting numbers could have been either $3$ and $3$, or $3$ and $0$, so $3$ and $0$ are both valid answers.</p><p>For the fifth test case, we can show that the starting numbers were $8$ and $16$.</p>
