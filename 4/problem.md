## Description

<div><p>Jay managed to create a problem of difficulty $x$ and decided to make it the second problem for Codeforces Round #921. </p><p>But Yash fears that this problem will make the contest highly unbalanced, and the coordinator will reject it. So, he decided to break it up into a problemset of $n$ sub-problems such that the difficulties of all the sub-problems are a positive integer and their sum is equal to $x$. </p><p>The coordinator, Aleksey, defines the balance of a problemset as the <a href="https://en.wikipedia.org/wiki/Greatest_common_divisor">GCD</a> of the difficulties of all sub-problems in the problemset. </p><p>Find the maximum balance that Yash can achieve if he chooses the difficulties of the sub-problems optimally.</p></div><div class="input-specification"><p>The first line of input contains a single integer $t$ ($1\leq t\leq 10^3$) denoting the number of test cases.</p><p>Each test case contains a single line of input containing two integers $x$ ($1\leq x\leq 10^8$) and $n$ ($1\leq n\leq x$).</p></div><div class="output-specification"><p>For each test case, print a single line containing a single integer denoting the maximum balance of the problemset Yash can achieve.</p></div>

## Input

<p>The first line of input contains a single integer $t$ ($1\leq t\leq 10^3$) denoting the number of test cases.</p><p>Each test case contains a single line of input containing two integers $x$ ($1\leq x\leq 10^8$) and $n$ ($1\leq n\leq x$).</p>

## Output

<p>For each test case, print a single line containing a single integer denoting the maximum balance of the problemset Yash can achieve.</p>





```input1|2,4
3
10 3
5 5
420 69
```




```output1
2
1
6
```



## Note

<p>For the first test case, one possible way is to break up the problem of difficulty $10$ into a problemset having three problems of difficulties $4$, $2$ and $4$ respectively, giving a balance equal to $2$.</p><p>For the second test case, there is only one way to break up the problem of difficulty $5$ into a problemset of $5$ problems with each problem having a difficulty $1$ giving a balance equal to $1$.</p>
