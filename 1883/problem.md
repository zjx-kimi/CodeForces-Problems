## Description

<div><p>A known chef has prepared $n$ dishes: the $i$-th dish consists of $a_i$ grams of fish and $b_i$ grams of meat. </p><p>The banquet organizers estimate the <span class="tex-font-style-it">balance</span> of $n$ dishes as follows. The <span class="tex-font-style-it">balance</span> is equal to the absolute value of the difference between the total mass of fish and the total mass of meat.</p><p>Technically, the <span class="tex-font-style-it">balance</span> equals to $\left|\sum\limits_{i=1}^n a_i - \sum\limits_{i=1}^n b_i\right|$. The smaller the <span class="tex-font-style-it">balance</span>, the better.</p><p>In order to improve the <span class="tex-font-style-it">balance</span>, a taster was invited. He will eat <span class="tex-font-style-bf">exactly</span> $m$ grams of food from each dish. For each dish, the taster determines separately how much fish and how much meat he will eat. The only condition is that he should eat exactly $m$ grams of each dish in total.</p><p>Determine how much of what type of food the taster should eat from each dish so that the value of the <span class="tex-font-style-it">balance</span> is as minimal as possible. If there are several correct answers, you may choose any of them.</p></div><div class="input-specification"><p>The first line of input data contains an integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of the test cases.</p><p>Each test case's description is preceded by a blank line. Next comes a line that contains integers $n$ and $m$ ($1 \leq n \leq 2 \cdot 10^5$; $0 \leq m \leq 10^6$). The next $n$ lines describe dishes, the $i$-th of them contains a pair of integers $a_i$ and $b_i$ ($0 \leq a_i, b_i \le 10^6$)&nbsp;— the masses of fish and meat in the $i$-th dish.</p><p>It is guaranteed that it is possible to eat $m$ grams of food from each dish. In other words, $m \leq a_i+b_i$ for all $i$ from $1$ to $n$ inclusive.</p><p>The sum of all $n$ values over all test cases in the test does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print on the first line the minimal balance value that can be achieved by eating exactly $m$ grams of food from each dish.</p><p>Then print $n$ lines that describe a way to do this: the $i$-th line should contain two integers $x_i$ and $y_i$ ($0 \leq x_i \leq a_i$; $0 \leq y_i \leq b_i$; $x_i+y_i=m$), where $x_i$ is how many grams of fish taster should eat from the $i$-th meal and $y_i$ is how many grams of meat.</p><p>If there are several ways to achieve a minimal balance, find any of them.</p></div>

## Input

<p>The first line of input data contains an integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of the test cases.</p><p>Each test case's description is preceded by a blank line. Next comes a line that contains integers $n$ and $m$ ($1 \leq n \leq 2 \cdot 10^5$; $0 \leq m \leq 10^6$). The next $n$ lines describe dishes, the $i$-th of them contains a pair of integers $a_i$ and $b_i$ ($0 \leq a_i, b_i \le 10^6$)&nbsp;— the masses of fish and meat in the $i$-th dish.</p><p>It is guaranteed that it is possible to eat $m$ grams of food from each dish. In other words, $m \leq a_i+b_i$ for all $i$ from $1$ to $n$ inclusive.</p><p>The sum of all $n$ values over all test cases in the test does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, print on the first line the minimal balance value that can be achieved by eating exactly $m$ grams of food from each dish.</p><p>Then print $n$ lines that describe a way to do this: the $i$-th line should contain two integers $x_i$ and $y_i$ ($0 \leq x_i \leq a_i$; $0 \leq y_i \leq b_i$; $x_i+y_i=m$), where $x_i$ is how many grams of fish taster should eat from the $i$-th meal and $y_i$ is how many grams of meat.</p><p>If there are several ways to achieve a minimal balance, find any of them.</p>





```input1
8

1 5
3 4

1 6
3 4

2 2
1 3
4 2

2 4
1 3
1 7

3 6
1 7
1 8
1 9

3 6
1 8
1 9
30 10

3 4
3 1
3 2
4 1

5 4
0 7
6 4
0 8
4 1
5 3
```




```output1
0
2 3
1
3 3
0
1 1
1 1
2
1 3
0 4
3
0 6
0 6
0 6
7
1 5
1 5
6 0
0
3 1
3 1
3 1
0
0 4
2 2
0 4
3 1
1 3
```


