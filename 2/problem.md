## Description

<div><p>There are $n$ children in a class, $m$ pairs among them are friends. The $i$-th pair who are friends have a friendship value of $f_i$. </p><p>The teacher has to go for $k$ excursions, and for each of the excursions she chooses a pair of children randomly, equiprobably and independently. If a pair of children who are friends is chosen, their friendship value increases by $1$ for all subsequent excursions (the teacher can choose a pair of children more than once). The friendship value of a pair who are not friends is considered $0$, and it does not change for subsequent excursions. </p><p>Find the expected value of the sum of friendship values of all $k$ pairs chosen for the excursions (at the time of being chosen). It can be shown that this answer can always be expressed as a fraction $\dfrac{p}{q}$ where $p$ and $q$ are coprime integers. Calculate $p\cdot q^{-1} \bmod (10^9+7)$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 5 \cdot 10^4$). Description of the test cases follows.</p><p>The first line of each test case contains $3$ integers $n$, $m$ and $k$ ($2 \le n \le 10^5$, $0 \le m \le \min \Big(10^5$, $ \frac{n(n-1)}{2} \Big)$, $1 \le k \le 2 \cdot 10^5$) — the number of children, pairs of friends and excursions respectively.</p><p>The next $m$ lines contain three integers each — $a_i$, $b_i$, $f_i$ — the indices of the pair of children who are friends and their friendship value. ($a_i \neq b_i$, $1 \le a_i,b_i \le n$, $1 \le f_i \le 10^9$). <span class="tex-font-style-bf">It is guaranteed that all pairs of friends are distinct</span>.</p><p>It is guaranteed that the sum of $n$ and sum $m$ over all test cases does not exceed $10^5$ and the sum of $k$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print one integer — the answer to the problem.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 5 \cdot 10^4$). Description of the test cases follows.</p><p>The first line of each test case contains $3$ integers $n$, $m$ and $k$ ($2 \le n \le 10^5$, $0 \le m \le \min \Big(10^5$, $ \frac{n(n-1)}{2} \Big)$, $1 \le k \le 2 \cdot 10^5$) — the number of children, pairs of friends and excursions respectively.</p><p>The next $m$ lines contain three integers each — $a_i$, $b_i$, $f_i$ — the indices of the pair of children who are friends and their friendship value. ($a_i \neq b_i$, $1 \le a_i,b_i \le n$, $1 \le f_i \le 10^9$). <span class="tex-font-style-bf">It is guaranteed that all pairs of friends are distinct</span>.</p><p>It is guaranteed that the sum of $n$ and sum $m$ over all test cases does not exceed $10^5$ and the sum of $k$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, print one integer — the answer to the problem.</p>





```input1|2,5,6
4
100 0 24
2 1 10
1 2 1
3 1 2
2 1 1
5 2 4
1 2 25
3 2 24
```




```output1
0
55
777777784
40000020
```



## Note

<p>For the first test case, there are no pairs of friends, so the friendship value of all pairs is $0$ and stays $0$ for subsequent rounds, hence the friendship value for all excursions is $0$.</p><p>For the second test case, there is only one pair possible $(1, 2)$ and its friendship value is initially $1$, so each turn they are picked and their friendship value increases by $1$. Therefore, the total sum is $1+2+3+\ldots+10 = 55$.</p><p>For the third test case, the final answer is $\frac{7}{9} = 777\,777\,784\bmod (10^9+7)$.</p>
