## Description

<div><p>You are given two integers $x$ and $k$. Grasshopper starts in a point $0$ on an OX axis. In one move, it can jump some integer distance, <span class="tex-font-style-bf">that is not divisible by $k$</span>, to the left or to the right.</p><p>What's the smallest number of moves it takes the grasshopper to reach point $x$? What are these moves? If there are multiple answers, print any of them.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of testcases.</p><p>The only line of each testcase contains two integers $x$ and $k$ ($1 \le x \le 100$; $2 \le k \le 100$)&nbsp;— the endpoint and the constraint on the jumps, respectively.</p></div><div class="output-specification"><p>For each testcase, in the first line, print a single integer $n$&nbsp;— the smallest number of moves it takes the grasshopper to reach point $x$.</p><p>In the second line, print $n$ integers, each of them not divisible by $k$. A positive integer would mean jumping to the right, a negative integer would mean jumping to the left. The endpoint after the jumps should be exactly $x$.</p><p>Each jump distance should be from $-10^9$ to $10^9$. In can be shown that, for any solution with the smallest number of jumps, there exists a solution with the same number of jumps such that each jump is from $-10^9$ to $10^9$.</p><p>It can be shown that the answer always exists under the given constraints. If there are multiple answers, print any of them.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of testcases.</p><p>The only line of each testcase contains two integers $x$ and $k$ ($1 \le x \le 100$; $2 \le k \le 100$)&nbsp;— the endpoint and the constraint on the jumps, respectively.</p>

## Output

<p>For each testcase, in the first line, print a single integer $n$&nbsp;— the smallest number of moves it takes the grasshopper to reach point $x$.</p><p>In the second line, print $n$ integers, each of them not divisible by $k$. A positive integer would mean jumping to the right, a negative integer would mean jumping to the left. The endpoint after the jumps should be exactly $x$.</p><p>Each jump distance should be from $-10^9$ to $10^9$. In can be shown that, for any solution with the smallest number of jumps, there exists a solution with the same number of jumps such that each jump is from $-10^9$ to $10^9$.</p><p>It can be shown that the answer always exists under the given constraints. If there are multiple answers, print any of them.</p>





```input1|2,4
3
10 2
10 3
3 4
```




```output1
2
7 3
1
10
1
3
```


