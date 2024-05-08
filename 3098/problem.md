## Description

<div><p>Johnny has just found the new, great tutorial: "<span class="tex-font-style-it">How to become a grandmaster?</span>". The tutorial tells many strange and unexpected for Johnny things, such as you have to be patient or that very important is solving many harder and harder problems. </p><p>The boy has found an online judge with tasks divided by topics they cover. He has picked $p^{k_i}$ problems from $i$-th category ($p$ is his favorite number). He wants to solve them in two weeks (the patience condition is too hard for Johnny, so for simplicity, he looks only at easy tasks, which can be solved in such a period). Now our future grandmaster has to decide which topics to cover first and which the second week. Help him assign topics in such a way, that workload is balanced.</p><p>Formally, given $n$ numbers $p^{k_i}$, the boy wants to divide them into two disjoint sets, minimizing the absolute difference between sums of numbers in each set. Find the minimal absolute difference. Output the result modulo $10^{9}+7$.</p></div><div class="input-specification"><p>Input consists of multiple test cases. The first line contains one integer $t$ $(1 \leq t \leq 10^5)$&nbsp;— the number of test cases. Each test case is described as follows:</p><p>The first line contains two integers $n$ and $p$ $(1 \leq n, p \leq 10^6)$. The second line contains $n$ integers $k_i$ $(0 \leq k_i \leq 10^6)$.</p><p>The sum of $n$ over all test cases doesn't exceed $10^6$.</p></div><div class="output-specification"><p>Output one integer&nbsp;— the reminder of division the answer by $1\,000\,000\,007$.</p></div>

## Input

<p>Input consists of multiple test cases. The first line contains one integer $t$ $(1 \leq t \leq 10^5)$&nbsp;— the number of test cases. Each test case is described as follows:</p><p>The first line contains two integers $n$ and $p$ $(1 \leq n, p \leq 10^6)$. The second line contains $n$ integers $k_i$ $(0 \leq k_i \leq 10^6)$.</p><p>The sum of $n$ over all test cases doesn't exceed $10^6$.</p>

## Output

<p>Output one integer&nbsp;— the reminder of division the answer by $1\,000\,000\,007$.</p>





```input1
4
5 2
2 3 4 4 3
3 1
2 10 1000
4 5
0 1 1 100
1 8
89
```




```output1
4
1
146981438
747093407
```



## Note

<p>You have to minimize the difference, not it's remainder. For example, if the minimum difference is equal to $2$, but there is also a distribution where the difference is $10^9 + 8$, then the answer is $2$, not $1$.</p><p>In the first test case of the example, there're the following numbers: $4$, $8$, $16$, $16$, and $8$. We can divide them into such two sets: ${4, 8, 16}$ and ${8, 16}$. Then the difference between the sums of numbers in sets would be $4$.</p>
