## Description

<div><p>In a sequence $a$, whose product was equal to $2023$, $k$ numbers were removed, leaving a sequence $b$ of length $n$. Given the resulting sequence $b$, find any suitable sequence $a$ and output which $k$ elements were removed from it, or state that such a sequence could not have existed.</p><p>Notice that you are not guaranteed that such array exists.</p></div><div class="input-specification"><p>Each test consists of several test cases. The first line contains a single integer $t$ ($1 \le t \le 100$)&nbsp;— the number of test cases. This is followed by a description of the test cases.</p><p>The first line of each test case contains two integers $n$ ($1 \le n, k \le 5$)&nbsp;— the size of sequence $b$ and the number of numbers removed from sequence $a$.</p><p>The second line contains $n$ integers $b_1,b_2, \ldots,b_n$ ($1 \leq b_i \leq 2023$)&nbsp;— the remaining sequence. The values of $b_i$ might not be divisors of $2023$.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if the sequence $a$ exists, and in the following line output $k$ non-negative integers that were removed from the sequence $a$. If the sequence $a$ does not exist, output "<span class="tex-font-style-tt">NO</span>" in a single line.</p><p>You can output the answer in any case (uppercase or lowercase). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive answers.</p></div>

## Input

<p>Each test consists of several test cases. The first line contains a single integer $t$ ($1 \le t \le 100$)&nbsp;— the number of test cases. This is followed by a description of the test cases.</p><p>The first line of each test case contains two integers $n$ ($1 \le n, k \le 5$)&nbsp;— the size of sequence $b$ and the number of numbers removed from sequence $a$.</p><p>The second line contains $n$ integers $b_1,b_2, \ldots,b_n$ ($1 \leq b_i \leq 2023$)&nbsp;— the remaining sequence. The values of $b_i$ might not be divisors of $2023$.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if the sequence $a$ exists, and in the following line output $k$ non-negative integers that were removed from the sequence $a$. If the sequence $a$ does not exist, output "<span class="tex-font-style-tt">NO</span>" in a single line.</p><p>You can output the answer in any case (uppercase or lowercase). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive answers.</p>





```input1|2,3,6,7,10,11,14,15
7
2 2
5 2
3 1
7 17 7
4 2
1 289 1 1
3 1
7 17 17
1 1
289
1 1
2023
1 3
1
```




```output1
NO
NO
YES
7 1
YES
1
YES
7
YES
1
YES
7 17 17
```



## Note

<p>In third test case product is equal to $289 \cdot 7 = 2023$.</p><p>In fourth test case product is already equal to $2023$.</p><p>In seventh test case product is equal to $7 \cdot 17 \cdot 17 = 2023$.</p>
