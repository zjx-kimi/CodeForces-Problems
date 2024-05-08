## Description

<div><p>There are $n$ islands, numbered $1, 2, \ldots, n$. Initially, every pair of islands is connected by a bridge. Hence, there are a total of $\frac{n (n - 1)}{2}$ bridges. </p><p>Everule lives on island $1$ and enjoys visiting the other islands using bridges. Dominater has the power to destroy at most $k$ bridges to minimize the number of islands that Everule can reach using (possibly multiple) bridges.</p><p>Find the minimum number of islands (including island $1$) that Everule can visit if Dominater destroys bridges optimally.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^3$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first and only line of each test case contains two integers $n$ and $k$ ($1 \le n \le 100$, $0 \le k \le \frac{n \cdot (n - 1)}{2}$).</p></div><div class="output-specification"><p>For each test case, output the minimum number of islands that Everule can visit if Dominater destroys bridges optimally.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^3$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first and only line of each test case contains two integers $n$ and $k$ ($1 \le n \le 100$, $0 \le k \le \frac{n \cdot (n - 1)}{2}$).</p>

## Output

<p>For each test case, output the minimum number of islands that Everule can visit if Dominater destroys bridges optimally.</p>





```input1|2,4,6
6
2 0
2 1
4 1
5 10
5 3
4 4
```




```output1
2
1
4
1
5
1
```



## Note

<p>In the first test case, since no bridges can be destroyed, all the islands will be reachable.</p><p>In the second test case, you can destroy the bridge between islands $1$ and $2$. Everule will not be able to visit island $2$ but can still visit island $1$. Therefore, the total number of islands that Everule can visit is $1$.</p><p>In the third test case, Everule always has a way of reaching all islands despite what Dominater does. For example, if Dominater destroyed the bridge between islands $1$ and $2$, Everule can still visit island $2$ by traveling by $1 \to 3 \to 2$ as the bridges between $1$ and $3$, and between $3$ and $2$ are not destroyed.</p><p>In the fourth test case, you can destroy all bridges since $k = \frac{n \cdot (n - 1)}{2}$. Everule will be only able to visit $1$ island (island $1$).</p>
