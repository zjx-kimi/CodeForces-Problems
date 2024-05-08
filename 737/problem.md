## Description

<div> Little Sasha has two friends, whom he wants to please with gifts on the Eighth of March. To do this, he went to the largest shopping center in the city.<p>There are $n$ departments in the mall, each of which has exactly two stores. For convenience, we number the departments with integers from $1$ to $n$. It is known that gifts in the first store of the $i$ department cost $a_i$ rubles, and in the second store of the $i$ department&nbsp;— $b_i$ rubles.</p><p>Entering the mall, Sasha will visit each of the $n$ departments of the mall, and in each department, he will enter exactly one store. When Sasha gets into the $i$-th department, he will perform exactly one of two actions:</p><ol> <li> Buy a gift for the first friend, spending $a_i$ rubles on it. </li><li> Buy a gift for the second friend, spending $b_i$ rubles on it. </li></ol><p>Sasha is going to buy at least one gift for each friend. Moreover, he wants to pick up gifts in such a way that the price difference of the most expensive gifts bought for friends is as small as possible so that no one is offended.</p><p>More formally: let $m_1$&nbsp; be the maximum price of a gift bought to the first friend, and $m_2$&nbsp; be the maximum price of a gift bought to the second friend. Sasha wants to choose gifts in such a way as to minimize the value of $\lvert m_1 - m_2 \rvert$. </p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 1\,000$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 500\,000$)&nbsp;— the number of departments in the mall.</p><p>Each of the following $n$ lines of each test case contains two integers $a_i$ and $b_i$ ($0 \le a_i, b_i \le 10^9$)&nbsp;— the prices of gifts in the first and second store of the $i$ department, respectively.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $500\,000$. </p></div><div class="output-specification"><p>Print one integer&nbsp;— the minimum price difference of the most expensive gifts bought to friends. </p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 1\,000$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 500\,000$)&nbsp;— the number of departments in the mall.</p><p>Each of the following $n$ lines of each test case contains two integers $a_i$ and $b_i$ ($0 \le a_i, b_i \le 10^9$)&nbsp;— the prices of gifts in the first and second store of the $i$ department, respectively.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $500\,000$. </p>

## Output

<p>Print one integer&nbsp;— the minimum price difference of the most expensive gifts bought to friends. </p>





```input1|2,3,4
2
2
1 2
2 1
5
1 5
2 7
3 3
4 10
2 5
```




```output1
0
1
```



## Note

<p>In the first test case, Sasha has two possible options: buy a gift for the first friend in the first department, and the second friend &nbsp;— in the second department, or vice versa. In the first case, $m_1 = m_2 = 1$, and in the second case&nbsp;— $m_1 = m_2 = 2$. In both cases, the answer is $0$.  In the second test case, you can buy gifts for the first friend in the $2$, $4$ and $5$ departments, and for the second friend &nbsp;— in the $1$ and $3$ departments.So $m_1 = \max(2, 4, 2) = 4$, $m_2 = \max(5, 3) = 5$. The answer is $\lvert 4 - 5 \rvert = 1$. </p>
