## Description

<div><p>You are given a sequence of integers $a$ of length $2n$. You have to split these $2n$ integers into $n$ pairs; each pair will represent the coordinates of a point on a plane. Each number from the sequence $a$ should become the $x$ or $y$ coordinate of exactly one point. Note that some points can be equal.</p><p>After the points are formed, you have to choose a path $s$ that starts from one of these points, ends at one of these points, and visits all $n$ points at least once.</p><p>The length of path $s$ is the sum of distances between all adjacent points on the path. In this problem, the distance between two points $(x_1, y_1)$ and $(x_2, y_2)$ is defined as $|x_1-x_2| + |y_1-y_2|$.</p><p>Your task is to form $n$ points and choose a path $s$ in such a way that the length of path $s$ is minimized.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 100$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a single integer $n$ ($2 \le n \le 100$)&nbsp;— the number of points to be formed.</p><p>The next line contains $2n$ integers $a_1, a_2, \dots, a_{2n}$ ($0 \le a_i \le 1\,000$)&nbsp;— the description of the sequence $a$.</p></div><div class="output-specification"><p>For each testcase, print the minimum possible length of path $s$ in the first line.</p><p>In the $i$-th of the following $n$ lines, print two integers $x_i$ and $y_i$ — the coordinates of the point that needs to be visited at the $i$-th position.</p><p>If there are multiple answers, print any of them.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 100$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a single integer $n$ ($2 \le n \le 100$)&nbsp;— the number of points to be formed.</p><p>The next line contains $2n$ integers $a_1, a_2, \dots, a_{2n}$ ($0 \le a_i \le 1\,000$)&nbsp;— the description of the sequence $a$.</p>

## Output

<p>For each testcase, print the minimum possible length of path $s$ in the first line.</p><p>In the $i$-th of the following $n$ lines, print two integers $x_i$ and $y_i$ — the coordinates of the point that needs to be visited at the $i$-th position.</p><p>If there are multiple answers, print any of them.</p>





```input1|2,3
2
2
15 1 10 5
3
10 30 20 20 30 10
```




```output1
9
10 1
15 5
20
20 20
10 30
10 30
```



## Note

<p>In the first testcase, for instance, you can form points $(10, 1)$ and $(15, 5)$ and start the path $s$ from the first point and end it at the second point. Then the length of the path will be $|10 - 15| + |1 - 5| = 5 + 4 = 9$.</p><p>In the second testcase, you can form points $(20, 20)$, $(10, 30)$, and $(10, 30)$, and visit them in that exact order. Then the length of the path will be $|20 - 10| + |20 - 30| + |10 - 10| + |30 - 30| = 10 + 10 + 0 + 0 = 20$.</p>
