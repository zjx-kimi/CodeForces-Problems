## Description

<div><p>Artem suggested a game to the girl Olya. There is a list of $n$ arrays, where the $i$-th array contains $m_i \ge 2$ positive integers $a_{i,1}, a_{i,2}, \ldots, a_{i,m_i}$.</p><p>Olya can move <span class="tex-font-style-bf">at most one</span> (possibly $0$) integer from <span class="tex-font-style-bf">each</span> array to another array. Note that integers can be moved from one array only once, but integers can be added to one array <span class="tex-font-style-bf">multiple times</span>, and all the movements are done <span class="tex-font-style-bf">at the same time</span>.</p><p>The <span class="tex-font-style-it">beauty</span> of the list of arrays is defined as the sum $\sum_{i=1}^n \min_{j=1}^{m_i} a_{i,j}$. In other words, for each array, we find the minimum value in it and then sum up these values.</p><p>The goal of the game is to maximize the beauty of the list of arrays. Help Olya win this challenging game!</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 25000$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 25000$) — the number of arrays in the list.</p><p>This is followed by descriptions of the arrays. Each array description consists of two lines.</p><p>The first line contains a single integer $m_i$ ($2 \le m_i \le 50000$) — the number of elements in the $i$-th array.</p><p>The next line contains $m_i$ integers $a_{i, 1}, a_{i, 2}, \ldots, a_{i, m_i}$ ($1 \le a_{i,j} \le 10^9$) — the elements of the $i$-th array.</p><p>It is guaranteed that the sum of $m_i$ over all test cases does not exceed $50000$.</p></div><div class="output-specification"><p>For each test case, output a single line containing a single integer — the maximum beauty of the list of arrays that Olya can achieve.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 25000$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 25000$) — the number of arrays in the list.</p><p>This is followed by descriptions of the arrays. Each array description consists of two lines.</p><p>The first line contains a single integer $m_i$ ($2 \le m_i \le 50000$) — the number of elements in the $i$-th array.</p><p>The next line contains $m_i$ integers $a_{i, 1}, a_{i, 2}, \ldots, a_{i, m_i}$ ($1 \le a_{i,j} \le 10^9$) — the elements of the $i$-th array.</p><p>It is guaranteed that the sum of $m_i$ over all test cases does not exceed $50000$.</p>

## Output

<p>For each test case, output a single line containing a single integer — the maximum beauty of the list of arrays that Olya can achieve.</p>





```input1|2,3,4,5,6,10,11,12,13,14,15,16
3
2
2
1 2
2
4 3
1
3
100 1 6
3
4
1001 7 1007 5
3
8 11 6
2
2 9
```




```output1
5
1
19
```



## Note

<p>In the first test case, we can move the integer $3$ from the second array to the first array. Then the beauty is $\min(1, 2, 3) + \min(4) = 5$. It can be shown that this is the maximum possible beauty.</p><p>In the second test case, there is only one array, so regardless of the movements, the beauty will be $\min(100, 1, 6) = 1$.</p>
