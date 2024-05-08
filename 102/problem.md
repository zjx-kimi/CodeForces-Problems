## Description

<div><p>Monocarp is a great solver of adhoc problems. Recently, he participated in an Educational Codeforces Round, and gained rating!</p><p>Monocarp knew that, before the round, his rating was $a$. After the round, it increased to $b$ ($b &gt; a$). He wrote both values one after another to not forget them.</p><p>However, he wrote them so close to each other, that he can't tell now where the first value ends and the second value starts.</p><p>Please, help him find some values $a$ and $b$ such that: </p><ul> <li> neither of them has a leading zero; </li><li> both of them are strictly greater than $0$; </li><li> $b &gt; a$; </li><li> they produce the given value $ab$ when written one after another. </li></ul><p>If there are multiple answers, you can print any of them.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The only line of each testcase consists of a single string $ab$ of length from $2$ to $8$ that: </p><ul> <li> consists only of digits; </li><li> doesn't start with a zero. </li></ul></div><div class="output-specification"><p>For each testcase, determine if such values $a$ and $b$ exist. If they don't, print <span class="tex-font-style-tt">-1</span>. Otherwise, print two integers $a$ and $b$.</p><p>If there are multiple answers, you can print any of them.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The only line of each testcase consists of a single string $ab$ of length from $2$ to $8$ that: </p><ul> <li> consists only of digits; </li><li> doesn't start with a zero. </li></ul>

## Output

<p>For each testcase, determine if such values $a$ and $b$ exist. If they don't, print <span class="tex-font-style-tt">-1</span>. Otherwise, print two integers $a$ and $b$.</p><p>If there are multiple answers, you can print any of them.</p>





```input1|2,4,6
5
20002001
391125
200200
2001000
12
```




```output1
2000 2001
39 1125
-1
200 1000
1 2
```



## Note

<p>In the second testcase, printing $3$ and $91125$ is also valid.</p><p>In the third testcase, $20$ and $0200$ is not valid, because $b$ has a leading zero. $200$ and $200$ is not valid, because $200$ is not strictly greater than $200$.</p>
