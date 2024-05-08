## Description

<div><p>Monocarp has an integer $n$.</p><p>He wants to represent his number as a sum of three <span class="tex-font-style-bf">distinct</span> positive integers $x$, $y$, and $z$. Additionally, Monocarp wants none of the numbers $x$, $y$, and $z$ to be divisible by $3$.</p><p>Your task is to help Monocarp to find any valid triplet of distinct positive integers $x$, $y$, and $z$, or report that such a triplet does not exist.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The only line of each testcase contains a single integer $n$ ($1 \le n \le 10^{9}$).</p></div><div class="output-specification"><p>For each testcase, if there is no valid triplet $x$, $y$, and $z$, print <span class="tex-font-style-tt">NO</span> on the first line.</p><p>Otherwise, print <span class="tex-font-style-tt">YES</span> on the first line. On the second line, print any valid triplet of distinct positive integers $x$, $y$, and $z$ such that $x + y + z = n$, and none of the printed numbers are divisible by $3$. If there are multiple valid triplets, you can print any of them.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The only line of each testcase contains a single integer $n$ ($1 \le n \le 10^{9}$).</p>

## Output

<p>For each testcase, if there is no valid triplet $x$, $y$, and $z$, print <span class="tex-font-style-tt">NO</span> on the first line.</p><p>Otherwise, print <span class="tex-font-style-tt">YES</span> on the first line. On the second line, print any valid triplet of distinct positive integers $x$, $y$, and $z$ such that $x + y + z = n$, and none of the printed numbers are divisible by $3$. If there are multiple valid triplets, you can print any of them.</p>





```input1|2,4
4
10
4
15
9
```




```output1
YES
4 5 1
NO
YES
2 8 5
NO
```



## Note

<p>In the first testcase, one of the valid triplets is $x = 4$, $y = 5$, $z = 1$. None of these numbers are divisible by three, and $4 + 5 + 1 = 10$.</p><p>In the second testcase, there is no valid triplet.</p><p>In the third testcase, one of the valid triplets is $x = 2$, $y = 8$, $z = 5$. None of these numbers are divisible by three, and $2 + 8 + 5 = 15$.</p><p>In the fourth testcase, there is no valid triplet.</p>
