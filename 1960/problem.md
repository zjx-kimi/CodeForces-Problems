## Description

<div><p>A total of $n$ depots are located on a number line. Depot $i$ lies at the point $x_i$ for $1 \le i \le n$.</p><p>You are a salesman with $n$ bags of goods, attempting to deliver one bag to each of the $n$ depots. You and the $n$ bags are initially at the origin $0$. You can carry up to $k$ bags at a time. You must collect the required number of goods from the origin, deliver them to the respective depots, and then return to the origin to collect your next batch of goods.</p><p>Calculate the minimum distance you need to cover to deliver all the bags of goods to the depots. You do <span class="tex-font-style-bf">not</span> have to return to the origin after you have delivered all the bags.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10\,500$). Description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le k \le n \le 2 \cdot 10^5$).</p><p>The second line of each test case contains $n$ integers $x_1, x_2, \ldots, x_n$ ($-10^9 \le x_i \le 10^9$). It is possible that some depots share the same position.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer denoting the minimum distance you need to cover to deliver all the bags of goods to the depots. </p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10\,500$). Description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le k \le n \le 2 \cdot 10^5$).</p><p>The second line of each test case contains $n$ integers $x_1, x_2, \ldots, x_n$ ($-10^9 \le x_i \le 10^9$). It is possible that some depots share the same position.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output a single integer denoting the minimum distance you need to cover to deliver all the bags of goods to the depots. </p>





```input1
4
5 1
1 2 3 4 5
9 3
-5 -10 -15 6 5 8 3 7 4
5 3
2 2 3 3 3
4 2
1000000000 1000000000 1000000000 1000000000
```




```output1
25
41
7
3000000000
```



## Note

<p>In the first test case, you can carry only one bag at a time. Thus, the following is a solution sequence that gives a minimum travel distance: $0 \to 2 \to 0 \to 4 \to 0 \to 3 \to 0 \to 1 \to 0 \to 5$, where each $0$ means you go the origin and grab one bag, and each positive integer means you deliver the bag to a depot at this coordinate, giving a total distance of $25$ units. It must be noted that there are other sequences that give the same distance.</p><p>In the second test case, you can follow the following sequence, among multiple such sequences, to travel minimum distance: $0 \to 6 \to 8 \to 7 \to 0 \to 5 \to 4 \to 3 \to 0 \to (-5) \to (-10) \to (-15)$, with distance $41$. It can be shown that $41$ is the optimal distance for this test case.</p>
