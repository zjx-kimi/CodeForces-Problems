## Description

<div><p>A string $t$ is said to be $k$-good if there exists at least one substring$^\dagger$ of length $k$ which is not a palindrome$^\ddagger$. Let $f(t)$ denote the sum of all values of $k$ such that the string $t$ is $k$-good.</p><p>You are given a string $s$ of length $n$. You will have to answer $q$ of the following queries:</p><ul> <li> Given $l$ and $r$ ($l &lt; r$), find the value of $f(s_ls_{l + 1}\ldots s_r)$. </li></ul><p>$^\dagger$ A substring of a string $z$ is a contiguous segment of characters from $z$. For example, "$\mathtt{defor}$", "$\mathtt{code}$" and "$\mathtt{o}$" are all substrings of "$\mathtt{codeforces}$" while "$\mathtt{codes}$" and "$\mathtt{aaa}$" are not.</p><p>$^\ddagger$ A palindrome is a string that reads the same backwards as forwards. For example, the strings "$\texttt{z}$", "$\texttt{aa}$" and "$\texttt{tacocat}$" are palindromes while "$\texttt{codeforces}$" and "$\texttt{ab}$" are not.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 2 \cdot 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $q$ ($2 \le n \le 2 \cdot 10^5, 1 \le q \le 2 \cdot 10^5$), the size of the string and the number of queries respectively.</p><p>The second line of each test case contains the string $s$. It is guaranteed the string $s$ only contains lowercase English characters.</p><p>The next $q$ lines each contain two integers, $l$ and $r$ ($1 \le l &lt; r \le n$). </p><p>It is guaranteed the sum of $n$ and the sum of $q$ both do not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each query, output $f(s_ls_{l + 1}\ldots s_r)$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 2 \cdot 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $q$ ($2 \le n \le 2 \cdot 10^5, 1 \le q \le 2 \cdot 10^5$), the size of the string and the number of queries respectively.</p><p>The second line of each test case contains the string $s$. It is guaranteed the string $s$ only contains lowercase English characters.</p><p>The next $q$ lines each contain two integers, $l$ and $r$ ($1 \le l &lt; r \le n$). </p><p>It is guaranteed the sum of $n$ and the sum of $q$ both do not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each query, output $f(s_ls_{l + 1}\ldots s_r)$.</p>





```input1|2,3,4,5,6,7,12,13,14,15,16,17,21,22,23
5
4 4
aaab
1 4
1 3
3 4
2 4
3 2
abc
1 3
1 2
5 4
pqpcc
1 5
4 5
1 3
2 4
2 1
aa
1 2
12 1
steponnopets
1 12
```




```output1
9
0
2
5
5
2
14
0
2
5
0
65
```



## Note

<p>In the first query of the first test case, the string is $\mathtt{aaab}$. $\mathtt{aaab}$, $\mathtt{aab}$ and $\mathtt{ab}$ are all substrings that are not palindromes, and they have lengths $4$, $3$ and $2$ respectively. Thus, the string is $2$-good, $3$-good and $4$-good. Hence, $f(\mathtt{aaab}) = 2 + 3 + 4 = 9$.</p><p>In the second query of the first test case, the string is $\mathtt{aaa}$. There are no non-palindromic substrings. Hence, $f(\mathtt{aaa}) = 0$.</p><p>In the first query of the second test case, the string is $\mathtt{abc}$. $\mathtt{ab}$, $\mathtt{bc}$ and $\mathtt{abc}$ are all substrings that are not palindromes, and they have lengths $2$, $2$ and $3$ respectively. Thus, the string is $2$-good and $3$-good. Hence, $f(\mathtt{abc}) = 2 + 3 = 5$. Note that even though there are $2$ non-palindromic substrings of length $2$, we count it only once.</p>
