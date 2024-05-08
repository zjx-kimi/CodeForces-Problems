## Description

<div><p>Consider an array $a_1, a_2, \dots, a_n$ consisting of numbers $1$ and $-1$. Define $A$-characteristic of this array as a number of pairs of indices $1 \le i &lt; j \le n$, such that $a_i \cdot a_j = 1$.</p><p>Find any array $a$ with given length $n$ with $A$-characteristic equal to the given value $k$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). The description of the test cases follows.</p><p>The only line of each test case contains two integers $n$ and $k$ ($2 \le n \le 100$; $0 \le k \le \frac{(n-1) n}{2}$)&nbsp;— the length of required array and required $A$-characteristic.</p></div><div class="output-specification"><p>For each test case, if there is no array $a$ with given $A$-characteristic $k$, print <span class="tex-font-style-tt">NO</span>.</p><p>Otherwise, print <span class="tex-font-style-tt">YES</span> and $n$ numbers $1$ and $-1$, which form the required array $a$. If there are multiple answers, print any of them.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). The description of the test cases follows.</p><p>The only line of each test case contains two integers $n$ and $k$ ($2 \le n \le 100$; $0 \le k \le \frac{(n-1) n}{2}$)&nbsp;— the length of required array and required $A$-characteristic.</p>

## Output

<p>For each test case, if there is no array $a$ with given $A$-characteristic $k$, print <span class="tex-font-style-tt">NO</span>.</p><p>Otherwise, print <span class="tex-font-style-tt">YES</span> and $n$ numbers $1$ and $-1$, which form the required array $a$. If there are multiple answers, print any of them.</p>





```input1|2,4,6,8
7
2 0
2 1
3 1
3 2
3 3
5 4
5 5
```




```output1
YES
1 -1 
YES
1 1 
YES
1 -1 1 
NO
YES
1 1 1 
YES
-1 1 -1 1 1 
NO
```



## Note

<p>In the first test case, there is only one pair of different elements in the array, and their product is $a_1 \cdot a_2 = -1 \neq 1$, hence its $A$-characteristic is $0$.</p><p>In the second test case, there is only one pair of different elements in the array, and their product is $a_1 \cdot a_2 = 1$, hence its $A$-characteristic is $1$.</p><p>In the third test case, there are three pairs of different elements in the array, and their product are: $a_1 \cdot a_2 = -1$, $a_1 \cdot a_3 = 1$, $a_2 \cdot a_3 = -1$, hence its $A$-characteristic is $1$.</p><p>In the fourth test case, we can show, that there is no array with length $3$, which $A$-characteristic is $2$.</p>
