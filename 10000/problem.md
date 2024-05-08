## Description

<div><p>You are given an array $a$ of length $n$, a positive integer $m$, and a string of commands of length $n$. Each command is either the character '<span class="tex-font-style-tt">L</span>' or the character '<span class="tex-font-style-tt">R</span>'.</p><p>Process all $n$ commands in the order they are written in the string $s$. Processing a command is done as follows:</p><ul> <li> First, output the remainder of the product of all elements of the array $a$ when divided by $m$. </li><li> Then, if the command is '<span class="tex-font-style-tt">L</span>', remove the leftmost element from the array $a$, if the command is '<span class="tex-font-style-tt">R</span>', remove the rightmost element from the array $a$. </li></ul><p>Note that after each move, the length of the array $a$ decreases by $1$, and after processing all commands, it will be empty.</p><p>Write a program that will process all commands in the order they are written in the string $s$ (from left to right).</p></div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \le t \le 10^4$) — the number of test cases in the input. Then descriptions of $t$ test cases follow.</p><p>Each test case of the input is given by three lines.</p><p>The first line contains two integers $n$ and $m$ ($1 \le n \le 2\cdot10^5, 1 \le m \le 10^4$) — the initial length of the array $a$ and the value to take the remainder by.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^4$) — the elements of the array $a$.</p><p>The third line contains a string $s$ consisting of $n$ characters '<span class="tex-font-style-tt">L</span>' and '<span class="tex-font-style-tt">R</span>'.</p><p>It is guaranteed that the sum of the values of $n$ for all test cases in a test does not exceed $2\cdot10^5$.</p></div><div class="output-specification"><p>For each test case, output $n$ integers $b_1, b_2, \dots, b_n$, where $b_i$ is the remainder when dividing the product of all elements of the current state of the array $a$ by $m$ at the beginning of the execution of the $i$-th command.</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \le t \le 10^4$) — the number of test cases in the input. Then descriptions of $t$ test cases follow.</p><p>Each test case of the input is given by three lines.</p><p>The first line contains two integers $n$ and $m$ ($1 \le n \le 2\cdot10^5, 1 \le m \le 10^4$) — the initial length of the array $a$ and the value to take the remainder by.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^4$) — the elements of the array $a$.</p><p>The third line contains a string $s$ consisting of $n$ characters '<span class="tex-font-style-tt">L</span>' and '<span class="tex-font-style-tt">R</span>'.</p><p>It is guaranteed that the sum of the values of $n$ for all test cases in a test does not exceed $2\cdot10^5$.</p>

## Output

<p>For each test case, output $n$ integers $b_1, b_2, \dots, b_n$, where $b_i$ is the remainder when dividing the product of all elements of the current state of the array $a$ by $m$ at the beginning of the execution of the $i$-th command.</p>





```input1|2,3,4,8,9,10
4
4 6
3 1 4 2
LRRL
5 1
1 1 1 1 1
LLLLL
6 8
1 2 3 4 5 6
RLLLRR
1 10000
10000
R
```




```output1
0 2 4 1 
0 0 0 0 0 
0 0 0 4 4 4 
0
```



## Note

<p>In the first test case of the example:</p><ul><li> $3 \cdot 1 \cdot 4 \cdot 2 \bmod 6 = 24 \bmod 6 = 0$;</li><li> $s_1 = \text{L}$, so we remove the first element and get the array $[1, 4, 2]$;</li><li> $1 \cdot 4 \cdot 2 \bmod 6 = 8 \bmod 6 = 2$;</li><li> $s_2 = \text{R}$, so we remove the last element and get the array $[1, 4]$;</li><li> $1 \cdot 4 \bmod 6 = 4 \bmod 6 = 4$;</li><li> $s_3 = \text{R}$, so we remove the last element and get the array $[1]$;</li><li> $1 \bmod 6 = 1$;</li><li> $s_4 = \text{L}$, so we remove the first element and get an empty array.</li></ul>
