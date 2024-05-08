## Description

<div><p>Vika came to her favorite cosmetics store "Golden Pear". She noticed that the prices of $n$ items have changed since her last visit.</p><p>She decided to analyze how much the prices have changed and calculated the difference between the old and new prices for each of the $n$ items.</p><p>Vika enjoyed calculating the price differences and decided to continue this process.</p><p>Let the old prices be represented as an array of non-negative integers $a$, and the new prices as an array of non-negative integers $b$. Both arrays have the same length $n$.</p><p>In one operation, Vika constructs a new array $c$ according to the following principle: $c_i = |a_i - b_i|$. Then, array $c$ renamed into array $b$, and array $b$ renamed into array $a$ at the same time, after which Vika repeats the operation with them.</p><p>For example, if $a = [1, 2, 3, 4, 5, 6, 7]$; $b = [7, 6, 5, 4, 3, 2, 1]$, then $c = [6, 4, 2, 0, 2, 4, 6]$. Then, $a = [7, 6, 5, 4, 3, 2, 1]$; $b = [6, 4, 2, 0, 2, 4, 6]$.</p><p>Vika decided to call a pair of arrays $a$, $b$ <span class="tex-font-style-it">dull</span> if after some number of such operations all elements of array $a$ become zeros.</p><p>Output "<span class="tex-font-style-tt">YES</span>" if the original pair of arrays is dull, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$)&nbsp;— the number of items whose prices have changed.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i \le 10^9$)&nbsp;— the old prices of the items.</p><p>The third line contains $n$ integers $b_1, b_2, \ldots, b_n$ ($0 \le b_i \le 10^9$)&nbsp;— the new prices of the items.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if the pair of price arrays is dull, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output each letter in any case (lowercase or uppercase). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be accepted as a positive answer.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$)&nbsp;— the number of items whose prices have changed.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i \le 10^9$)&nbsp;— the old prices of the items.</p><p>The third line contains $n$ integers $b_1, b_2, \ldots, b_n$ ($0 \le b_i \le 10^9$)&nbsp;— the new prices of the items.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if the pair of price arrays is dull, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output each letter in any case (lowercase or uppercase). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be accepted as a positive answer.</p>





```input1|2,3,4,8,9,10,14,15,16,20,21,22,26,27,28
9
4
0 0 0 0
1 2 3 4
3
1 2 3
1 2 3
2
1 2
2 1
6
100 23 53 11 56 32
1245 31 12 6 6 6
7
1 2 3 4 5 6 7
7 6 5 4 3 2 1
3
4 0 2
4 0 2
3
2 5 2
1 3 4
2
6 1
4 2
2
0 0
0 3
```




```output1
YES
YES
NO
NO
YES
YES
NO
YES
YES
```



## Note

<p>In the first test case, the array $a$ is initially zero.</p><p>In the second test case, after the first operation $a = [1, 2, 3], b = [0, 0, 0]$. After the second operation $a = [0, 0, 0], b = [1, 2, 3]$.</p><p>In the third test case, it can be shown that the array $a$ will never become zero.</p>
