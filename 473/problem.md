## Description

<div><p>Recently, Vika was studying her favorite internet resource - Wikipedia.</p><p>On the expanses of Wikipedia, she read about an interesting mathematical operation <a href="https://en.wikipedia.org/wiki/Bitwise_operation#XOR">bitwise XOR</a>, denoted by $\oplus$. </p><p>Vika began to study the properties of this mysterious operation. To do this, she took an array $a$ consisting of $n$ non-negative integers and applied the following operation to all its elements at the same time: $a_i = a_i \oplus a_{(i+1) \bmod n}$. Here $x \bmod y$ denotes the remainder of dividing $x$ by $y$. The elements of the array are numbered starting from $0$.</p><p>Since it is not enough to perform the above actions once for a complete study, Vika repeats them until the array $a$ becomes all zeros.</p><p>Determine how many of the above actions it will take to make all elements of the array $a$ zero. If this moment never comes, output $-1$.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($1 \le n \le 2^{20}$) - the length of the array $a$.</p><p>It is guaranteed that $n$ can be represented as $2^k$ for some integer $k$ ($0 \le k \le 20$).</p><p>The second line contains $n$ integers $a_0, a_1, a_2, \dots, a_{n-1}$ ($0 \le a_i \le 10^9$) - the elements of the array $a$.</p></div><div class="output-specification"><p>Output a single number - the minimum number of actions required to make all elements of the array $a$ zero, or $-1$ if the array $a$ will never become zero.</p></div>

## Input

<p>The first line contains a single integer $n$ ($1 \le n \le 2^{20}$) - the length of the array $a$.</p><p>It is guaranteed that $n$ can be represented as $2^k$ for some integer $k$ ($0 \le k \le 20$).</p><p>The second line contains $n$ integers $a_0, a_1, a_2, \dots, a_{n-1}$ ($0 \le a_i \le 10^9$) - the elements of the array $a$.</p>

## Output

<p>Output a single number - the minimum number of actions required to make all elements of the array $a$ zero, or $-1$ if the array $a$ will never become zero.</p>





```input1
4
1 2 1 2
```




```input2
2
0 0
```




```input3
1
14
```




```input4
8
0 1 2 3 4 5 6 7
```




```output1
2
```




```output2
0
```




```output3
1
```




```output4
5
```



## Note

<p>In the first example, after one operation, the array $a$ will become equal to $[3, 3, 3, 3]$. After one more operation, it will become equal to $[0, 0, 0, 0]$.</p><p>In the second example, the array $a$ initially consists only of zeros.</p><p>In the third example, after one operation, the array $a$ will become equal to $[0]$.</p>
