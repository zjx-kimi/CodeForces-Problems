## Description

<div><p>You are given two integers $x$ and $y$. A sequence $a$ of length $n$ is called <span class="tex-font-style-it">modular</span> if $a_1=x$, and for all $1 &lt; i \le n$ the value of $a_{i}$ is either $a_{i-1} + y$ or $a_{i-1} \bmod y$. Here $x \bmod y$ denotes the remainder from dividing $x$ by $y$.</p><p>Determine if there exists a modular sequence of length $n$ with the sum of its elements equal to $S$, and if it exists, find any such sequence.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 2 \cdot 10^4$). The description of the test cases follows.</p><p>The first and only line of each test case contains four integers $n$, $x$, $y$, and $s$ ($1 \le n \le 2 \cdot 10^5$, $0 \le x \le 2 \cdot 10^5$, $1 \le y \le 2 \cdot 10^5$, $0 \le s \le 2 \cdot 10^5$)&nbsp;— the length of the sequence, the parameters $x$ and $y$, and the required sum of the sequence elements.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$, and also the sum of $s$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, if the desired sequence exists, output "<span class="tex-font-style-tt">Yes</span>" on the first line (without quotes). Then, on the second line, output $n$ integers $a_1, a_2, \ldots, a_n$ separated by a space&nbsp;— the elements of the sequence $a$. If there are multiple suitable sequences, output any of them.</p><p>If the sequence does not exist, output "<span class="tex-font-style-tt">No</span>" on a single line.</p><p>You can output each letter in any case (lowercase or uppercase). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be accepted as a positive answer.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 2 \cdot 10^4$). The description of the test cases follows.</p><p>The first and only line of each test case contains four integers $n$, $x$, $y$, and $s$ ($1 \le n \le 2 \cdot 10^5$, $0 \le x \le 2 \cdot 10^5$, $1 \le y \le 2 \cdot 10^5$, $0 \le s \le 2 \cdot 10^5$)&nbsp;— the length of the sequence, the parameters $x$ and $y$, and the required sum of the sequence elements.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$, and also the sum of $s$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, if the desired sequence exists, output "<span class="tex-font-style-tt">Yes</span>" on the first line (without quotes). Then, on the second line, output $n$ integers $a_1, a_2, \ldots, a_n$ separated by a space&nbsp;— the elements of the sequence $a$. If there are multiple suitable sequences, output any of them.</p><p>If the sequence does not exist, output "<span class="tex-font-style-tt">No</span>" on a single line.</p><p>You can output each letter in any case (lowercase or uppercase). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be accepted as a positive answer.</p>





```input1|2,4
3
5 8 3 28
3 5 3 6
9 1 5 79
```




```output1
YES
8 11 2 2 5 
NO
NO
```



## Note

<p>In the first example, the sequence $[8, 11, 2, 5, 2]$ satisfies the conditions. Thus, $a_1 = 8 = x$, $a_2 = 11 = a_1 + 3$, $a_3 = 2 = a_2 \bmod 3$, $a_4 = 5 = a_3 + 3$, $a_5 = 2 = a_4 \bmod 3$.</p><p>In the second example, the first element of the sequence should be equal to $5$, so the sequence $[2, 2, 2]$ is not suitable.</p>
