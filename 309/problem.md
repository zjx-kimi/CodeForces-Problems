## Description

<div><p>Vasilije is a smart student and his discrete mathematics teacher Sonja taught him number theory very well.</p><p>He gave Ognjen a positive integer $n$.</p><p>Denote $d(n)$ as the number of positive integer divisors of $n$, and denote $gcd(a, b)$ as the largest integer $g$ such that $a$ is divisible by $g$ and $b$ is divisible by $g$.</p><p>After that, he gave Ognjen $q$ queries, and there are $2$ types of queries. </p><ul> <li> $1$, $x$&nbsp;— set $n$ to $n \cdot x$, and then answer the following question: does there exist a positive integer $a$ such that $gcd(a, n) = 1$, and $d(n \cdot a) = n$? </li><li> $2$&nbsp;— reset $n$ to its initial value (before any queries). </li></ul><p>Note that $n$ <span class="tex-font-style-bf">does not</span> get back to its initial value after the <span class="tex-font-style-bf">type 1</span> query.</p><p>Since Ognjen is afraid of number theory, Vasilije promised him that <span class="tex-font-style-bf">after each query</span>, $d(n) \le 10^9$, however, even with that constraint, he still needs your help with this problem.</p></div><div class="input-specification"><p>The first line contains a positive integer $t$, ($1 \le t \le 100$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains $2$ integers, $n$ and $q$ ($1 \le n \le 10^{6}$, $1\le q \le 1000$)&nbsp;— the number $n$ and the number of queries.</p><p>The following $q$ lines contain an integer $k$ ($1 \le k \le 2$), if $k=1$ then there is another integer in this line $x$ ($1 \le x \le 10^6$)&nbsp;— the description of the queries.</p><p>It is guaranteed that, for the given input, $d(n)$ does not exceed $10^9$ at any point.</p><p>It is guaranteed that the sum of $q$ over all test cases doesn't exceed $10^3$.</p></div><div class="output-specification"><p>For each <span class="tex-font-style-bf">type 1</span> query, you should output "<span class="tex-font-style-tt">YES</span>" if there exist such positive integer $a$ that $gcd(a, n) = 1$ and $d(n \cdot a)=n$, and "<span class="tex-font-style-tt">NO</span>" if he can't.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p></div>

## Input

<p>The first line contains a positive integer $t$, ($1 \le t \le 100$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains $2$ integers, $n$ and $q$ ($1 \le n \le 10^{6}$, $1\le q \le 1000$)&nbsp;— the number $n$ and the number of queries.</p><p>The following $q$ lines contain an integer $k$ ($1 \le k \le 2$), if $k=1$ then there is another integer in this line $x$ ($1 \le x \le 10^6$)&nbsp;— the description of the queries.</p><p>It is guaranteed that, for the given input, $d(n)$ does not exceed $10^9$ at any point.</p><p>It is guaranteed that the sum of $q$ over all test cases doesn't exceed $10^3$.</p>

## Output

<p>For each <span class="tex-font-style-bf">type 1</span> query, you should output "<span class="tex-font-style-tt">YES</span>" if there exist such positive integer $a$ that $gcd(a, n) = 1$ and $d(n \cdot a)=n$, and "<span class="tex-font-style-tt">NO</span>" if he can't.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p>





```input1|2,3,4,5,6,7,13,14,15,16,17,18,19,20,21,22,23,26,27,32,33,34,35,36,37
7
1 5
1 1
1 2
2
1 8
1 9
20 4
1 3
2
1 7
1 12
16 10
1 6
1 6
1 10
1 9
1 1
1 9
1 7
1 3
1 2
1 10
9 1
1 3
8 1
1 2
8 3
1 5
1 8
1 10
11 5
1 8
1 2
1 1
1 3
1 1
```




```output1
YES
YES
YES
YES

YES
NO
YES

YES
NO
YES
YES
YES
NO
YES
NO
YES
YES

NO

NO

YES
NO
NO

YES
NO
NO
NO
NO
```



## Note

<p><span class="tex-font-style-bf">In the first test case</span>, we initially have $n=1$.</p><p>After the first query: $n=1$, $d(n)=1$, so by taking $a = 1$, $d(n \cdot a) = n$, and the answer to this query is "<span class="tex-font-style-tt">YES</span>".</p><p>After the second query: $n=2$, $d(n)=2$, we can, again, take $a = 1$, $d(n \cdot a) = n$, and the answer to this query is "<span class="tex-font-style-tt">YES</span>".</p><p>After the third query $n=1$, and this is a type $2$ query so we don't answer it.</p><p>After the fourth query: $n=8$, and by taking $a=3$, $d(n \cdot a) = d(24) = 8 = n$, so the answer is "<span class="tex-font-style-tt">YES</span>".</p><p>After the fifth query: $n=72$, now we can take $a=637$ to get $n \cdot a = 45864$, and $d(n \cdot a) = 72 = n$, so the answer is "<span class="tex-font-style-tt">YES</span>".</p><p><span class="tex-font-style-bf">In the second test case</span>, we initially have $n=20$.</p><p>After the first query: $n=60$, and the answer is "<span class="tex-font-style-tt">YES</span>".</p><p>After the second query: $n=20$, this is a type $2$ query, so we don't answer it.</p><p>After the third query: $n=140$, and it can be proven that no matter which positive integer $a$ we take, $d(n \cdot a)$ will never be equal to $n$, so the answer to this query is "<span class="tex-font-style-tt">NO</span>".</p><p>After the fourth query: $n=1680$. It can be proven that there exists a positive integer $a$, such that $d(n \cdot a) = n$, so the answer is "<span class="tex-font-style-tt">YES</span>".</p>
