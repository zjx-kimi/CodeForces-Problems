## Description

<div><p>You are given an array $a$ consisting of $n$ positive integers. You have to choose a positive integer $d$ and paint all elements into two colors. All elements which are divisible by $d$ will be painted red, and all other elements will be painted blue.</p><p>The coloring is called beautiful if there are no pairs of adjacent elements with the same color in the array. Your task is to find any value of $d$ which yields a beautiful coloring, or report that it is impossible.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains one integer $n$ ($2 \le n \le 100$) — the number of elements of the array.</p><p>The second line of each testcase contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^{18}$).</p></div><div class="output-specification"><p>For each testcase print a single integer. If there is no such value of $d$ that yields a beautiful coloring, print $0$. Otherwise, print any suitable value of $d$ ($1 \le d \le 10^{18}$).</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains one integer $n$ ($2 \le n \le 100$) — the number of elements of the array.</p><p>The second line of each testcase contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^{18}$).</p>

## Output

<p>For each testcase print a single integer. If there is no such value of $d$ that yields a beautiful coloring, print $0$. Otherwise, print any suitable value of $d$ ($1 \le d \le 10^{18}$).</p>





```input1
5
5
1 2 3 4 5
3
10 5 15
3
100 10 200
10
9 8 2 6 6 2 8 6 5 4
2
1 3
```




```output1
2
0
100
0
3
```


