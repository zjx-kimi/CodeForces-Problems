## Description

<div><p>You are given an array of integers $a_1, a_2, \ldots, a_n$, as well as a binary string$^{\dagger}$ $s$ consisting of $n$ characters.</p><p>Augustin is a big fan of data structures. Therefore, he asked you to implement a data structure that can answer $q$ queries. There are two types of queries:</p><ul><li> "1 $l$ $r$" ($1\le l \le r \le n$)&nbsp;— replace each character $s_i$ for $l \le i \le r$ with its opposite. That is, replace all $\texttt{0}$ with $\texttt{1}$ and all $\texttt{1}$ with $\texttt{0}$.</li><li> "2 $g$" ($g \in \{0, 1\}$)&nbsp;— calculate the value of the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#XOR">bitwise XOR</a> of the numbers $a_i$ for all indices $i$ such that $s_i = g$. Note that the $\operatorname{XOR}$ of an empty set of numbers is considered to be equal to $0$.</li></ul><p>Please help Augustin to answer all the queries!</p><p>For example, if $n = 4$, $a = [1, 2, 3, 6]$, $s = \texttt{1001}$, consider the following series of queries:</p><ol><li> "2 $0$"&nbsp;— we are interested in the indices $i$ for which $s_i = \tt{0}$, since $s = \tt{1001}$, these are the indices $2$ and $3$, so the answer to the query will be $a_2 \oplus a_3 = 2 \oplus 3 = 1$.</li><li> "1 $1$ $3$"&nbsp;— we need to replace the characters $s_1, s_2, s_3$ with their opposites, so before the query $s = \tt{1001}$, and after the query: $s = \tt{0111}$.</li><li> "2 $1$"&nbsp;— we are interested in the indices $i$ for which $s_i = \tt{1}$, since $s = \tt{0111}$, these are the indices $2$, $3$, and $4$, so the answer to the query will be $a_2 \oplus a_3 \oplus a_4 = 2 \oplus 3 \oplus 6 = 7$.</li><li> "1 $2$ $4$"&nbsp;— $s = \tt{0111}$ $\to$ $s = \tt{0000}$.</li><li> "2 $1$"&nbsp;— $s = \tt{0000}$, there are no indices with $s_i = \tt{1}$, so since the $\operatorname{XOR}$ of an empty set of numbers is considered to be equal to $0$, the answer to this query is $0$.</li></ol><p>$^{\dagger}$ A binary string is a string containing only characters $\texttt{0}$ or $\texttt{1}$.</p></div><div class="input-specification"><p>The first line of the input contains one integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases in the test.</p><p>The descriptions of the test cases follow.</p><p>The first line of each test case description contains an integer $n$ ($1 \le n \le 10^5$)&nbsp;— the length of the array.</p><p>The second line of the test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$).</p><p>The third line of the test case contains the binary string $s$ of length $n$.</p><p>The fourth line of the test case contains one integer $q$ ($1 \le q \le 10^5$)&nbsp;— the number of queries.</p><p>The subsequent $q$ lines of the test case describe the queries. The first number of each query, $tp \in \{1, 2\}$, characterizes the type of the query: if $tp = 1$, then $2$ integers $1 \le l \le r \le n$ follow, meaning that the operation of type $1$ should be performed with parameters $l, r$, and if $tp = 2$, then one integer $g \in \{0, 1\}$ follows, meaning that the operation of type $2$ should be performed with parameter $g$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$, and also that the sum of $q$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, and for each query of type $2$ in it, output the answer to the corresponding query.</p></div>

## Input

<p>The first line of the input contains one integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases in the test.</p><p>The descriptions of the test cases follow.</p><p>The first line of each test case description contains an integer $n$ ($1 \le n \le 10^5$)&nbsp;— the length of the array.</p><p>The second line of the test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$).</p><p>The third line of the test case contains the binary string $s$ of length $n$.</p><p>The fourth line of the test case contains one integer $q$ ($1 \le q \le 10^5$)&nbsp;— the number of queries.</p><p>The subsequent $q$ lines of the test case describe the queries. The first number of each query, $tp \in \{1, 2\}$, characterizes the type of the query: if $tp = 1$, then $2$ integers $1 \le l \le r \le n$ follow, meaning that the operation of type $1$ should be performed with parameters $l, r$, and if $tp = 2$, then one integer $g \in \{0, 1\}$ follows, meaning that the operation of type $2$ should be performed with parameter $g$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$, and also that the sum of $q$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, and for each query of type $2$ in it, output the answer to the corresponding query.</p>





```input1|2,3,4,5,6,7,8,9,10,11,12,20,21,22,23,24,25,26,32,33,34,35,36,37,38,39,40
5
5
1 2 3 4 5
01000
7
2 0
2 1
1 2 4
2 0
2 1
1 1 3
2 1
6
12 12 14 14 5 5
001001
3
2 1
1 2 4
2 1
4
7 7 7 777
1111
3
2 0
1 2 3
2 0
2
1000000000 996179179
11
1
2 1
5
1 42 20 47 7
00011
5
1 3 4
1 1 1
1 3 4
1 2 4
2 0
```




```output1
3 2 6 7 7 
11 7 
0 0 
16430827 
47
```



## Note

<p>Let's analyze the first test case:</p><ol><li> "2 $0$"&nbsp;— we are interested in the indices $i$ for which $s_i = \tt{0}$, since $s = \tt{01000}$, these are the indices $1, 3, 4$, and $5$, so the answer to the query will be $a_1 \oplus a_3 \oplus a_4 \oplus a_5 = 1 \oplus 3 \oplus 4 \oplus 5 = 3$.</li><li> "2 $1$"&nbsp;— we are interested in the indices $i$ for which $s_i = \tt{1}$, since $s = \tt{01000}$, the only suitable index is $2$, so the answer to the query will be $a_2 = 2$.</li><li> "1 $2$ $4$"&nbsp;— we need to replace the characters $s_2, s_3, s_4$ with their opposites, so before the query $s = \tt{01000}$, and after the query: $s = \tt{00110}$.</li><li> "2 $0$"&nbsp;— we are interested in the indices $i$ for which $s_i = \tt{0}$, since $s = \tt{00110}$, these are the indices $1, 2$, and $5$, so the answer to the query will be $a_1 \oplus a_2 \oplus a_5 = 1 \oplus 2 \oplus 5 = 6$.</li><li> "2 $1$"&nbsp;— we are interested in the indices $i$ for which $s_i = \tt{1}$, since $s = \tt{00110}$, these are the indices $3$ and $4$, so the answer to the query will be $a_3 \oplus a_4 = 3 \oplus 4 = 7$.</li><li> "1 $1$ $3$"&nbsp;— $s = \tt{00110}$ $\to$ $s = \tt{11010}$.</li><li> "2 $1$"&nbsp;— we are interested in the indices $i$ for which $s_i = \tt{1}$, since $s = \tt{11010}$, these are the indices $1, 2$, and $4$, so the answer to the query will be $a_1 \oplus a_2 \oplus a_4 = 1 \oplus 2 \oplus 4 = 7$.</li></ol>
