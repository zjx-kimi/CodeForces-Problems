## Description

<div><p>You are given an array $a$ of $n$ positive integers and a score. If your score is greater than or equal to $a_i$, then you can increase your score by $a_i$ and remove $a_i$ from the array. </p><p>For each index $i$, output the maximum number of additional array elements that you can remove if you remove $a_i$ and then set your score to $a_i$. Note that the removal of $a_i$ should not be counted in the answer.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 5000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$)&nbsp;— the length of the array.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the elements of the array.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output $n$ integers, the $i$-th of which denotes the maximum number of additional array elements that you can remove if you remove $a_i$ from the array and then set your score to $a_i$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 5000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$)&nbsp;— the length of the array.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the elements of the array.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output $n$ integers, the $i$-th of which denotes the maximum number of additional array elements that you can remove if you remove $a_i$ from the array and then set your score to $a_i$.</p>





```input1|2,3,6,7
4
5
20 5 1 4 2
3
1434 7 1442
1
1
5
999999999 999999999 999999999 1000000000 1000000000
```




```output1
4 3 0 3 1 
1 0 2 
0 
4 4 4 4 4
```



## Note

<p>In the first test case, the answers are as follows:</p><p>If we start with $i=4$, our initial score is $a_4=4$ and $a=[20,5,1,2]$. We can remove $3$ additional elements in the following order: </p><ol> <li> Since $4 \ge 1$, we can remove $1$ and our score becomes $5$. After this, $a=[20,5,2]$. </li><li> Since $5 \ge 5$, we can remove $5$ and our score becomes $10$. After this, $a=[20,2]$. </li><li> Since $10 \ge 2$, we can remove $2$ and our score becomes $12$. After this, $a=[20]$. </li></ol><p>If we start with $i=1$ we can remove all remaining elements in the array, so the answer is $4$.</p><p>If we start with $i=2$, we can remove $3$ additional elements in the following order: $1$, $4$, $2$.</p><p>If we start with $i=3$, we can remove no additional elements.</p><p>If we start with $i=5$, we can remove $1$ additional element: $1$.</p>
