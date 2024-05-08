## Description

<div><p>green_gold_dog has an array $a$ of length $n$, and he wants to find a permutation $b$ of length $n$ such that the number of distinct numbers in the element-wise difference between array $a$ and permutation $b$ is maximized.</p><p>A permutation of length $n$ is an array consisting of $n$ distinct integers from $1$ to $n$ in any order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation (as $2$ appears twice in the array) and $[1,3,4]$ is also not a permutation (as $n=3$, but $4$ appears in the array).</p><p>The element-wise difference between two arrays $a$ and $b$ of length $n$ is an array $c$ of length $n$, where $c_i$ = $a_i - b_i$ ($1 \leq i \leq n$).</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 4 \cdot 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 4 \cdot 10^4$).</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $4 \cdot 10^4$.</p></div><div class="output-specification"><p>For each test case, output $n$ numbers - a suitable permutation $b$. If there are multiple solutions, print any of them.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 4 \cdot 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 4 \cdot 10^4$).</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $4 \cdot 10^4$.</p>

## Output

<p>For each test case, output $n$ numbers - a suitable permutation $b$. If there are multiple solutions, print any of them.</p>





```input1|2,3,6,7
3
1
100000
2
1 1
3
10 3 3
```




```output1
1 
2 1 
1 3 2
```



## Note

<p>In the first set of input data, the element-wise difference of the arrays is [99999]. Here, there is one distinct number, and it is obvious that in an array of length one, there cannot be more than one different element.</p><p>In the second set of input data, the element-wise difference of the arrays is [-1, 0]. Here, there are two distinct numbers, and it is obvious that in an array of length two, there cannot be more than two different elements.</p><p>In the third set of input data, the element-wise difference of the arrays is [9, 0, 1]. Here, there are three distinct numbers, and it is obvious that in an array of length three, there cannot be more than three different elements.</p>
