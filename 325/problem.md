## Description

<div><p>Jellyfish has $n$ green apple pieces. Each green apple piece weighs $1~\text{kg}$. Jellyfish wants to divide these green apple pieces <span class="tex-font-style-bf">equally</span> among $m$ people.</p><p>Jellyfish has a magic knife. Each time Jellyfish can choose one piece of green apple and divide it into two smaller pieces, with each piece having half the weight of the original piece.</p><p>Jellyfish wants to know the minimum number of operations needed such that she can divide the green apple pieces such that the total weight of apple pieces received by each person is the same.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 2 \cdot 10^4$). The description of the test cases follows.</p><p>The first and only line of each test case contains two integers, $n$ and $m$ ($1 \leq n, m \leq 10^9$)&nbsp;— the number of the green apple pieces initially and the number of the people.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the minimum number of operations required to divide all the green apples equally among the $m$ people. If this cannot be achieved using a finite number of operations, output $-1$ instead.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 2 \cdot 10^4$). The description of the test cases follows.</p><p>The first and only line of each test case contains two integers, $n$ and $m$ ($1 \leq n, m \leq 10^9$)&nbsp;— the number of the green apple pieces initially and the number of the people.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the minimum number of operations required to divide all the green apples equally among the $m$ people. If this cannot be achieved using a finite number of operations, output $-1$ instead.</p>





```input1|2,4
4
10 5
1 5
10 4
3 4
```




```output1
0
-1
2
5
```



## Note

<p>In the first test case, we do not need to divide the apple pieces. Each person will receive $2$ pieces of $1~\text{kg}$ and the total weight of apple pieces received by each person is $2~\text{kg}$.</p><p>In the second test case, it is impossible to divide the apple equally using a finite number of operations.</p><p>In the third test case, we can divide two of the apple pieces of weight $1~\text{kg}$, getting $4$ apple pieces of weight $0.5~\text{kg}$. Each person will receive $1$ apple piece of weight $0.5~\text{kg}$ and $2$ apple pieces of weight $1~\text{kg}$. The total weight of apple pieces received by each person is $2.5~\text{kg}$.</p><p>In the fourth test case, we first divide all $3$ of the apple pieces of weight $1~\text{kg}$, getting $6$ pieces of weight $0.5~\text{kg}$. Then, we further divide two of the apple pieces of weight $0.5~\text{kg}$, getting $4$ pieces of weight $0.25~\text{kg}$. Each person will receive $1$ apple piece of weight $0.5~\text{kg}$ and $1$ apple piece of weight $0.25~\text{kg}$. The total weight of apples received by each person is $0.75~\text{kg}$.</p>
