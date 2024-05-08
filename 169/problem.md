## Description

<div><p><span class="tex-font-style-bf">This is the hard version of the problem. The only difference between the two versions is the constraint on $n$ and $q$, the memory and time limits. You can make hacks only if all versions of the problem are solved.</span></p><p>Theofanis really likes to play with the bits of numbers. He has an array $a$ of size $n$ and an integer $k$. He can make at most $k$ operations in the array. In each operation, he picks a single element and increases it by $1$.</p><p>He found the <span class="tex-font-style-bf">maximum</span> <a href="https://en.wikipedia.org/wiki/Bitwise_operation#AND">bitwise AND</a> that array $a$ can have after at most $k$ operations.</p><p>Theofanis has put a lot of work into finding this value and was very happy with his result. Unfortunately, Adaś, being the evil person that he is, decided to bully him by repeatedly changing the value of $k$.</p><p>Help Theofanis by calculating the <span class="tex-font-style-bf">maximum</span> possible <a href="https://en.wikipedia.org/wiki/Bitwise_operation#AND">bitwise AND</a> for $q$ different values of $k$. Note that queries are independent.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $q$ ($1 \le n, q \le 10^6$)&nbsp;— the size of the array and the number of queries.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i \le 10^6$)&nbsp;— the elements of the array.</p><p>Next $q$ lines describe the queries. The $i$-th line contains one integer $k_i$ ($0 \le k_i \le 10^{18}$)&nbsp;— the number of operations that can be done in the $i$-th query.</p></div><div class="output-specification"><p>For each query, print one integer&nbsp;— the <span class="tex-font-style-bf">maximum</span> bitwise AND that array $a$ can have after at most $k_i$ operations.</p></div>

## Input

<p>The first line contains two integers $n$ and $q$ ($1 \le n, q \le 10^6$)&nbsp;— the size of the array and the number of queries.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i \le 10^6$)&nbsp;— the elements of the array.</p><p>Next $q$ lines describe the queries. The $i$-th line contains one integer $k_i$ ($0 \le k_i \le 10^{18}$)&nbsp;— the number of operations that can be done in the $i$-th query.</p>

## Output

<p>For each query, print one integer&nbsp;— the <span class="tex-font-style-bf">maximum</span> bitwise AND that array $a$ can have after at most $k_i$ operations.</p>





```input1|
4 2
1 3 7 5
2
10
```




```input2|
3 5
4 0 2
9
8
17
1
3
```




```input3|
1 2
10
5
2318381298321
```




```output1
2
6
```




```output2
5
4
7
0
1
```




```output3
15
2318381298331
```



## Note

<p>In the first test case, in the first query, we add $1$ in the first and last elements of the array. </p><p>Thus, the array becomes $[2,3,7,6]$ with bitwise AND equal to $2$.</p><p>In the second test case, in the first query, we add $1$ in the first element, $5$ in the second, and $3$ in the third and now all the elements are equal to $5$.</p>
