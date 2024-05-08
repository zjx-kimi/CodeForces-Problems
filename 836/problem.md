## Description

<div><p>Serval loves playing music games. He meets a problem when playing music games, and he leaves it for you to solve.</p><p>You are given $n$ positive integers $s_1 &lt; s_2 &lt; \ldots &lt; s_n$. $f(x)$ is defined as the number of $i$ ($1\leq i\leq n$) that exist non-negative integers $p_i, q_i$ such that: </p><p>$$s_i=p_i\left\lfloor{s_n\over x}\right\rfloor + q_i\left\lceil{s_n\over x}\right\rceil$$</p><p>Find out $\sum_{x=1}^{s_n} x\cdot f(x)$ modulo $998\,244\,353$.</p><p>As a reminder, $\lfloor x\rfloor$ denotes the maximal integer that is no greater than $x$, and $\lceil x\rceil$ denotes the minimal integer that is no less than $x$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1\leq t\leq 10^4$). The description of the test cases follows.</p><p>The first line of each test cases contains a single integer $n$ ($1\leq n\leq 10^6$).</p><p>The second line of each test case contains $n$ positive integers $s_1,s_2,\ldots,s_n$ ($1\leq s_1 &lt; s_2 &lt; \ldots &lt; s_n \leq 10^7$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^6$, and the sum of $s_n$ does not exceed $10^7$.</p></div><div class="output-specification"><p>For each test case, print a single integer in a single line — the sum of $x\cdot f(x)$ over all possible $x$ modulo $998\,244\,353$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1\leq t\leq 10^4$). The description of the test cases follows.</p><p>The first line of each test cases contains a single integer $n$ ($1\leq n\leq 10^6$).</p><p>The second line of each test case contains $n$ positive integers $s_1,s_2,\ldots,s_n$ ($1\leq s_1 &lt; s_2 &lt; \ldots &lt; s_n \leq 10^7$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^6$, and the sum of $s_n$ does not exceed $10^7$.</p>

## Output

<p>For each test case, print a single integer in a single line — the sum of $x\cdot f(x)$ over all possible $x$ modulo $998\,244\,353$.</p>





```input1|2,3,6,7
4
3
1 2 4
4
1 2 7 9
4
344208 591000 4779956 5403429
5
1633 1661 1741 2134 2221
```




```output1
26
158
758737625
12334970
```



## Note

<p>For the first test case, $s_n=4$, $f(x)$ are calculated as followings:</p><ul><li> $f(1)=1$ <ul> <li> $\left\lfloor s_n\over 1\right\rfloor=4$, $\left\lceil s_n\over 1\right\rceil=4$. </li><li> It can be shown that such $p_1,p_2$ and $q_1,q_2$ that satisfy the conditions don't exist. </li><li> Let $p_3=1$ and $q_3=0$, then $s_3 = p_3\cdot\left\lfloor s_n\over 1\right\rfloor + q_3\cdot\left\lceil s_n\over 1\right\rceil = 1\cdot 4 + 0\cdot 4 = 4$. </li></ul></li><li> $f(2)=2$ <ul> <li> $\left\lfloor s_n\over 2\right\rfloor=2$, $\left\lceil s_n\over 2\right\rceil=2$. </li><li> It can be shown that such $p_1$ and $q_1$ that satisfy the conditions don't exist. </li><li> Let $p_2=1$ and $q_2=0$, then $s_2 = p_2\cdot\left\lfloor s_n\over 2\right\rfloor + q_2\cdot\left\lceil s_n\over 2\right\rceil = 1\cdot 2 + 0\cdot 2 = 2$. </li><li> Let $p_3=0$ and $q_3=2$, then $s_3 = p_3\cdot\left\lfloor s_n\over 2\right\rfloor + q_3\cdot\left\lceil s_n\over 2\right\rceil = 0\cdot 2 + 2\cdot 2 = 4$. </li></ul></li><li> $f(3)=3$ <ul> <li> $\left\lfloor s_n\over 3\right\rfloor=1$, $\left\lceil s_n\over 3\right\rceil=2$. </li><li> Let $p_1=1$ and $q_1=0$, then $s_1 = p_1\cdot\left\lfloor s_n\over 3\right\rfloor + q_1\cdot\left\lceil s_n\over 3\right\rceil = 1\cdot 1 + 0\cdot 2 = 1$. </li><li> Let $p_2=0$ and $q_2=1$, then $s_2 = p_2\cdot\left\lfloor s_n\over 3\right\rfloor + q_2\cdot\left\lceil s_n\over 3\right\rceil = 0\cdot 1 + 1\cdot 2 = 2$. </li><li> Let $p_3=0$ and $q_3=2$, then $s_3 = p_3\cdot\left\lfloor s_n\over 3\right\rfloor + q_3\cdot\left\lceil s_n\over 3\right\rceil = 0\cdot 1 + 2\cdot 2 = 4$. </li></ul></li><li> $f(4)=3$ <ul> <li> $\left\lfloor s_n\over 4\right\rfloor=1$, $\left\lceil s_n\over 4\right\rceil=1$. </li><li> Let $p_1=1$ and $q_1=0$, then $s_1 = p_1\cdot\left\lfloor s_n\over 4\right\rfloor + q_1\cdot\left\lceil s_n\over 4\right\rceil = 1\cdot 1 + 0\cdot 1 = 1$. </li><li> Let $p_2=1$ and $q_2=1$, then $s_2 = p_2\cdot\left\lfloor s_n\over 4\right\rfloor + q_2\cdot\left\lceil s_n\over 4\right\rceil = 1\cdot 1 + 1\cdot 1 = 2$. </li><li> Let $p_3=2$ and $q_3=2$, then $s_3 = p_3\cdot\left\lfloor s_n\over 4\right\rfloor + q_3\cdot\left\lceil s_n\over 4\right\rceil = 2\cdot 1 + 2\cdot 1 = 4$. </li></ul> </li></ul><p>Therefore, the answer is $\sum_{x=1}^4 x\cdot f(x) = 1\cdot 1 + 2\cdot 2 + 3\cdot 3 + 4\cdot 3 = 26$.</p><p>For the second test case:</p><ul> <li> $f(1)=f(2)=f(3)=1$ </li><li> $f(4)=3$ </li><li> $f(5)=f(6)=f(7)=f(8)=f(9)=4$ </li></ul><p>For example, when $x=3$ we have $f(3)=1$ because there exist $p_4$ and $q_4$:</p><p>$$9 = 1 \cdot\left\lfloor{9\over 3}\right\rfloor + 2 \cdot\left\lceil{9\over 3}\right\rceil$$</p><p>It can be shown that it is impossible to find $p_1,p_2,p_3$ and $q_1,q_2,q_3$ that satisfy the conditions.</p><p>When $x=5$ we have $f(5)=4$ because there exist $p_i$ and $q_i$ as followings:</p><p>$$1 = 1 \cdot\left\lfloor{9\over 5}\right\rfloor + 0 \cdot\left\lceil{9\over 5}\right\rceil$$ $$2 = 0 \cdot\left\lfloor{9\over 5}\right\rfloor + 1 \cdot\left\lceil{9\over 5}\right\rceil$$ $$7 = 3 \cdot\left\lfloor{9\over 5}\right\rfloor + 2 \cdot\left\lceil{9\over 5}\right\rceil$$ $$9 = 3 \cdot\left\lfloor{9\over 5}\right\rfloor + 3 \cdot\left\lceil{9\over 5}\right\rceil$$</p><p>Therefore, the answer is $\sum_{x=1}^9 x\cdot f(x) = 158$.</p>
