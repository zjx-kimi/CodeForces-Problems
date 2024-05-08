## Description

<div><p>Rudolf is going to visit Bernard, and he decided to take the metro to get to him. The ticket can be purchased at a machine that accepts exactly two coins, the sum of which does not exceed $k$.</p><p>Rudolf has two pockets with coins. In the left pocket, there are $n$ coins with denominations $b_1, b_2, \dots, b_n$. In the right pocket, there are $m$ coins with denominations $c_1, c_2, \dots, c_m$. He wants to choose exactly one coin from the left pocket and exactly one coin from the right pocket (two coins in total).</p><p>Help Rudolf determine how many ways there are to select indices $f$ and $s$ such that $b_f + c_s \le k$.</p></div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \le t \le 100$) — the number of test cases. Then follows the description of each test case.</p><p>The first line of each test case contains three natural numbers $n$, $m$, and $k$ ($1 \le n, m \le 100, 1 \le k \le 2000$) — the number of coins in the left and right pockets, and the maximum sum of two coins for the ticket payment at the counter, respectively.</p><p>The second line of each test case contains $n$ integers $b_i$ ($1 \le b_i \le 1000$) — the denominations of coins in the left pocket.</p><p>The third line of each test case contains $m$ integers $c_i$ ($1 \le c_i \le 1000$) — the denominations of coins in the right pocket.</p></div><div class="output-specification"><p>For each testcase, output a single integer — the number of ways Rudolf can select two coins, taking one from each pocket, so that the sum of the coins does not exceed $k$.</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \le t \le 100$) — the number of test cases. Then follows the description of each test case.</p><p>The first line of each test case contains three natural numbers $n$, $m$, and $k$ ($1 \le n, m \le 100, 1 \le k \le 2000$) — the number of coins in the left and right pockets, and the maximum sum of two coins for the ticket payment at the counter, respectively.</p><p>The second line of each test case contains $n$ integers $b_i$ ($1 \le b_i \le 1000$) — the denominations of coins in the left pocket.</p><p>The third line of each test case contains $m$ integers $c_i$ ($1 \le c_i \le 1000$) — the denominations of coins in the right pocket.</p>

## Output

<p>For each testcase, output a single integer — the number of ways Rudolf can select two coins, taking one from each pocket, so that the sum of the coins does not exceed $k$.</p>





```input1|2,3,4,8,9,10
4
4 4 8
1 5 10 14
2 1 8 1
2 3 4
4 8
1 2 3
4 2 7
1 1 1 1
2 7
3 4 2000
1 1 1
1 1 1 1
```




```output1
6
0
4
12
```



## Note

<p>Note that the pairs indicate the <span class="tex-font-style-bf">indices</span> of the coins in the array, not their denominations.</p><p>In the first test case, Rudolf can choose the following pairs of coins: $[1, 1], [1, 2], [1, 4], [2, 1], [2, 2], [2, 4]$.</p><p>In the second test case, Rudolf cannot choose one coin from each pocket in any way, as the sum of any two elements from the first and second arrays will exceed the value of $k=4$.</p><p>In the third test case, Rudolf can choose: $[1, 1], [2, 1], [3, 1], [4, 1]$.</p><p>In the fourth test case, Rudolf can choose any coin from the left pocket and any coin from the right pocket.</p>
