## Description

<div><p>We define an integer to be <span class="tex-font-style-it">the most common</span> on a subsegment, if its number of occurrences on that subsegment is larger than the number of occurrences of any other integer in that subsegment. A subsegment of an array is a consecutive segment of elements in the array $a$.</p><p>Given an array $a$ of size $n$, and an integer $k$, determine if there exists a non-empty subsegment of $a$ where $k$ is <span class="tex-font-style-it">the most common element</span>.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le n \le 100$, $1 \le k \le 100$)&nbsp;— the number of elements in array and the element which must be <span class="tex-font-style-it">the most common</span>.</p><p>The second line of each test case contains $n$ integers $a_1$, $a_2$, $a_3$, $\dots$, $a_n$ ($1 \le a_i \le 100$)&nbsp;— elements of the array.</p></div><div class="output-specification"><p>For each test case output "<span class="tex-font-style-tt">YES</span>" if there exists a subsegment in which $k$ is <span class="tex-font-style-it">the most common</span> element, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le n \le 100$, $1 \le k \le 100$)&nbsp;— the number of elements in array and the element which must be <span class="tex-font-style-it">the most common</span>.</p><p>The second line of each test case contains $n$ integers $a_1$, $a_2$, $a_3$, $\dots$, $a_n$ ($1 \le a_i \le 100$)&nbsp;— elements of the array.</p>

## Output

<p>For each test case output "<span class="tex-font-style-tt">YES</span>" if there exists a subsegment in which $k$ is <span class="tex-font-style-it">the most common</span> element, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p>





```input1|2,3,6,7,10,11,14,15
7
5 4
1 4 3 4 1
4 1
2 3 4 4
5 6
43 5 60 4 2
2 5
1 5
4 1
5 3 3 1
1 3
3
5 3
3 4 1 5 5
```




```output1
YES
NO
NO
YES
YES
YES
YES
```



## Note

<p>In the first test case we need to check if there is a subsegment where the <span class="tex-font-style-it">most common element</span> is $4$.</p><p>On the subsegment $[2,5]$ the elements are $4, \ 3, \ 4, \ 1$. </p><ul><li> $4$ appears $2$ times;</li><li> $1$ appears $1$ time;</li><li> $3$ appears $1$ time.</li></ul><p>This means that $4$ is the <span class="tex-font-style-it">most common element</span> on the subsegment $[2, 5]$, so there exists a subsegment where $4$ is the <span class="tex-font-style-it">most common element</span>.</p>
