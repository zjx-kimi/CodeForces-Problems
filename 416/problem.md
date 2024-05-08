## Description

<div><p>A <span class="tex-font-style-it">prime</span> number is a positive integer that has exactly two different positive divisors: $1$ and the integer itself. For example, $2$, $3$, $13$ and $101$ are prime numbers; $1$, $4$, $6$ and $42$ are not.</p><p>You are given a sequence of digits from $1$ to $9$, in which <span class="tex-font-style-bf">every digit from $1$ to $9$ appears exactly once</span>.</p><p>You are allowed to do the following operation <span class="tex-font-style-bf">several (maybe zero) times</span>: choose any digit from the sequence and delete it. <span class="tex-font-style-bf">However, you cannot perform this operation if the sequence consists of only two digits.</span></p><p>Your goal is to obtain a sequence which represents a prime number. Note that you cannot reorder the digits in the sequence.</p><p>Print the resulting sequence, or report that it is impossible to perform the operations so that the resulting sequence is a prime number.</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 5000$) — the number of test cases.</p><p>Each test case consists of one line containing a string of $9$ digits (without any characters between them). Each digit from $1$ to $9$ appears in this string exactly once.</p></div><div class="output-specification"><p>For each test case, print the answer on a separate line as follows:</p><ul> <li> if it is impossible to perform the described operations, print $-1$; </li><li> otherwise, print any sequence that represents a prime number, which can be obtained from the given string performing several (maybe zero) operations described in the statement. If there are multiple such sequences, you can print any one of them. </li></ul></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 5000$) — the number of test cases.</p><p>Each test case consists of one line containing a string of $9$ digits (without any characters between them). Each digit from $1$ to $9$ appears in this string exactly once.</p>

## Output

<p>For each test case, print the answer on a separate line as follows:</p><ul> <li> if it is impossible to perform the described operations, print $-1$; </li><li> otherwise, print any sequence that represents a prime number, which can be obtained from the given string performing several (maybe zero) operations described in the statement. If there are multiple such sequences, you can print any one of them. </li></ul>





```input1|2,4
4
123456789
987654321
243567918
576318429
```




```output1
167
53
3571
57638429
```


