## Description

<div><p>Mocha is a young girl from high school. She has learned so much interesting knowledge from her teachers, especially her math teacher. Recently, Mocha is learning about binary system and very interested in bitwise operation.</p><p>This day, Mocha got a sequence $a$ of length $n$. In each operation, she can select an arbitrary interval $[l, r]$ and for all values $i$ ($0\leq i \leq r-l$), replace $a_{l+i}$ with $a_{l+i} \,\&amp;\, a_{r-i}$ at the same time, where $\&amp;$ denotes the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#AND">bitwise AND operation</a>. This operation can be performed <span class="tex-font-style-bf">any number of times</span>.</p><p>For example, if $n=5$, the array is $[a_1,a_2,a_3,a_4,a_5]$, and Mocha selects the interval $[2,5]$, then the new array is $[a_1,a_2\,\&amp;\, a_5, a_3\,\&amp;\, a_4, a_4\,\&amp;\, a_3, a_5\,\&amp;\, a_2]$.</p><p>Now Mocha wants to minimize the maximum value in the sequence. As her best friend, can you help her to get the answer?</p></div><div class="input-specification"><p>Each test contains multiple test cases. </p><p>The first line contains a single integer $t$ ($1 \le t \le 100$) — the number of test cases. Each test case consists of two lines.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 100$) — the length of the sequence.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i \le 10^9$).</p></div><div class="output-specification"><p>For each test case, print one integer — the minimal value of the maximum value in the sequence.</p></div>

## Input

<p>Each test contains multiple test cases. </p><p>The first line contains a single integer $t$ ($1 \le t \le 100$) — the number of test cases. Each test case consists of two lines.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 100$) — the length of the sequence.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i \le 10^9$).</p>

## Output

<p>For each test case, print one integer — the minimal value of the maximum value in the sequence.</p>





```input1
4
2
1 2
3
1 1 3
4
3 11 3 7
5
11 7 15 3 7
```




```output1
0
1
3
3
```



## Note

<p>In the first test case, Mocha can choose the interval $[1,2]$, then the sequence becomes $[ 0, 0]$, where the first element is $1\,\&amp;\,2$, and the second element is $2\,\&amp;\,1$.</p><p>In the second test case, Mocha can choose the interval $[1,3]$, then the sequence becomes $[ 1,1,1]$, where the first element is $1\,\&amp;\,3$, the second element is $1\,\&amp;\,1$, and the third element is $3\,\&amp;\,1$.</p>
