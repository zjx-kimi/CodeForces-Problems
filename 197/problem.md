## Description

<div><p>Alex is participating in the filming of another video of BrMeast, and BrMeast asked Alex to prepare 250 thousand tons of TNT, but Alex didn't hear him well, so he prepared $n$ boxes and arranged them in a row waiting for trucks. The $i$-th box from the left weighs $a_i$ tons.</p><p>All trucks that Alex is going to use hold the same number of boxes, denoted by $k$. Loading happens the following way:</p><ul> <li> The first $k$ boxes goes to the first truck, </li><li> The second $k$ boxes goes to the second truck, </li><li> $\dotsb$ </li><li> The last $k$ boxes goes to the $\frac{n}{k}$-th truck. </li></ul><p>Upon loading is completed, each truck must have <span class="tex-font-style-bf">exactly</span> $k$ boxes. In other words, if at some point it is not possible to load exactly $k$ boxes into the truck, then the loading option with that $k$ is not possible.</p><p>Alex hates justice, so he wants the maximum absolute difference between the total weights of two trucks to be as great as possible. If there is only one truck, this value is $0$.</p><p>Alex has quite a lot of connections, so for every $1 \leq k \leq n$, he can find a company such that each of its trucks can hold exactly $k$ boxes. Print the maximum absolute difference between the total weights of any two trucks.</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains one integer $n$ ($1 \leq n \leq 150\,000$)&nbsp;— the number of boxes.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \leq a_i \leq 10^9$)&nbsp;— the weights of the boxes.</p><p>It is guaranteed that the sum of $n$ for all test cases does not exceed $150\,000$.</p></div><div class="output-specification"><p>For each test case, print a single integer&nbsp;— the answer to the problem.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains one integer $n$ ($1 \leq n \leq 150\,000$)&nbsp;— the number of boxes.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \leq a_i \leq 10^9$)&nbsp;— the weights of the boxes.</p><p>It is guaranteed that the sum of $n$ for all test cases does not exceed $150\,000$.</p>

## Output

<p>For each test case, print a single integer&nbsp;— the answer to the problem.</p>





```input1|2,3,6,7,10,11
5
2
1 2
6
10 2 3 6 1 3
4
1000000000 1000000000 1000000000 1000000000
15
60978 82265 78961 56708 39846 31071 4913 4769 29092 91348 64119 72421 98405 222 14294
8
19957 69913 37531 96991 57838 21008 14207 19198
```




```output1
1
9
0
189114
112141
```



## Note

<p>In the first case, we should pick two trucks, so the first one will have only the first box, and the second one will have only the second box.</p><p>In the second case, we should pick six trucks, so the maximum will be $10$, the minimum will be $1$, and the answer is $10 - 1 = 9$.</p><p>In the third case, for any possible $k$, the trucks will have the same total weight of boxes, so the answer is $0$.</p>
