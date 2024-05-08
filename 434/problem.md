## Description

<div><p>Given a natural number $x$. You can perform the following operation: </p><ul> <li> choose a positive integer $k$ and round $x$ to the $k$-th digit </li></ul><p>Note that the positions are numbered from right to left, starting from zero. If the number has $k$ digits, it is considered that the digit at the $k$-th position is equal to $0$.</p><p>The rounding is done as follows: </p><ul> <li> if the digit at the $(k-1)$-th position is greater than or equal to $5$, then the digit at the $k$-th position is increased by $1$, otherwise the digit at the $k$-th position remains unchanged (mathematical rounding is used).<p> </p></li><li> if before the operations the digit at the $k$-th position was $9$, and it should be increased by $1$, then we search for the least position $k'$ ($k'&gt;k$), where the digit at the $k'$-th position is less than $9$ and add $1$ to the digit at the $k'$-th position. Then we assign $k=k'$.<p> </p></li><li> after that, all digits which positions are less than $k$ are replaced with zeros.</li></ul><p>Your task is to make $x$ as large as possible, if you can perform the operation as many times as you want.</p><p>For example, if $x$ is equal to $3451$, then if you choose consecutively: </p><ul> <li> $k=1$, then after the operation $x$ will become $3450$ </li><li> $k=2$, then after the operation $x$ will become $3500$ </li><li> $k=3$, then after the operation $x$ will become $4000$ </li><li> $k=4$, then after the operation $x$ will become $0$ </li></ul> To maximize the answer, you need to choose $k=2$ first, and then $k=3$, then the number will become $4000$.</div><div class="input-specification"><p>The first line contains a single integer $t$ ($1\le t\le 10^4$)&nbsp;— the number of test cases.</p><p>Each test case consists of positive integer $x$ with a length of up to $2 \cdot 10^5$. It is guaranteed that there are no leading zeros in the integer.</p><p>It is guaranteed that the sum of the lengths of all integers $x$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each set of input data, output the maximum possible value of $x$ after the operations. The number should not have leading zeros in its representation.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1\le t\le 10^4$)&nbsp;— the number of test cases.</p><p>Each test case consists of positive integer $x$ with a length of up to $2 \cdot 10^5$. It is guaranteed that there are no leading zeros in the integer.</p><p>It is guaranteed that the sum of the lengths of all integers $x$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each set of input data, output the maximum possible value of $x$ after the operations. The number should not have leading zeros in its representation.</p>





```input1|2,4,6,8,10
10
1
5
99
913
1980
20444
20445
60947
419860
40862016542130810467
```




```output1
1
10
100
1000
2000
20444
21000
100000
420000
41000000000000000000
```



## Note

<p>In the first sample, it is better not to perform any operations.</p><p>In the second sample, you can perform one operation and obtain $10$.</p><p>In the third sample, you can choose $k=1$ or $k=2$. In both cases the answer will be $100$.</p>
