## Description

<div><p>Rudolf has an array $a$ of $n$ integers, the elements are numbered from $1$ to $n$.</p><p>In one operation, he can choose an index $i$ ($2 \le i \le n - 1$) and assign:</p><ul> <li> $a_{i - 1} = a_{i - 1} - 1$ </li><li> $a_i = a_i - 2$ </li><li> $a_{i + 1} = a_{i + 1} - 1$ </li></ul><p>Rudolf can apply this operation any number of times. Any index $i$ can be used zero or more times.</p><p>Can he make all the elements of the array equal to zero using this operation?</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases in the test.</p><p>The first line of each case contains a single integer $n$ ($3 \le n \le 2 \cdot 10^5$)&nbsp;— the number of elements in the array.</p><p>The second line of each case contains $n$ integers $a_1, a_2, \dots, a_n$ ($0 \le a_j \le 10^9$)&nbsp;— the elements of the array.</p><p>It is guaranteed that the sum of the values of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if it is possible to make all the elements of the array zero using the described operations. Otherwise, output "<span class="tex-font-style-tt">NO</span>".</p><p>You can output each letter in any case (lowercase or uppercase). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be accepted as a positive answer.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases in the test.</p><p>The first line of each case contains a single integer $n$ ($3 \le n \le 2 \cdot 10^5$)&nbsp;— the number of elements in the array.</p><p>The second line of each case contains $n$ integers $a_1, a_2, \dots, a_n$ ($0 \le a_j \le 10^9$)&nbsp;— the elements of the array.</p><p>It is guaranteed that the sum of the values of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if it is possible to make all the elements of the array zero using the described operations. Otherwise, output "<span class="tex-font-style-tt">NO</span>".</p><p>You can output each letter in any case (lowercase or uppercase). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be accepted as a positive answer.</p>





```input1|2,3,6,7,10,11,14,15
7
5
1 3 5 5 2
5
2 4 4 5 1
5
0 1 3 3 1
6
5 6 0 2 3 0
4
1 2 7 2
3
7 1 0
4
1 1 1 1
```




```output1
YES
NO
YES
NO
NO
NO
NO
```



## Note

<p>In the first example, the original array is $[1, 3, 5, 5, 2]$, to make all its elements zero, Rudolf can act as follows:</p><ul> <li> apply the operation at $i=4$ and get the array $[1, 3, 4, 3, 1]$; </li><li> apply the operation at $i=3$ and get the array $[1, 2, 2, 2, 1]$; </li><li> apply the operation at $i=2$ and get the array $[0, 0, 1, 2, 1]$; </li><li> apply the operation at $i=4$ and get the array $[0, 0, 0, 0, 0]$. </li></ul>
