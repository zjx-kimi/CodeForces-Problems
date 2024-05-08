## Description

<div><p>Petya and his friend, the robot Petya++, have a common friend&nbsp;— the cyborg Petr#. Sometimes Petr# comes to the friends for a cup of tea and tells them interesting problems.</p><p>Today, Petr# told them the following problem.</p><p>A palindrome is a sequence that reads the same from left to right as from right to left. For example, $[38, 12, 8, 12, 38]$, $[1]$, and $[3, 8, 8, 3]$ are palindromes.</p><p>Let's call the <span class="tex-font-style-it">palindromicity</span> of a sequence $a_1, a_2, \dots, a_n$ the minimum count of elements that need to be replaced to make this sequence a palindrome. For example, the palindromicity of the sequence $[38, 12, 8, 38, 38]$ is $1$ since it is sufficient to replace the number $38$ at the fourth position with the number $12$. And the palindromicity of the sequence $[3, 3, 5, 5, 5]$ is two since you can replace the first two threes with fives, and the resulting sequence $[5, 5, 5, 5, 5]$ is a palindrome.</p><p>Given a sequence $a$ of length $n$, and an <span class="tex-font-style-bf">odd</span> integer $k$, you need to find the sum of palindromicity of all subarrays of length $k$, i.&nbsp;e., the sum of the palindromicity values for the sequences $a_i, a_{i+1}, \dots, a_{i+k-1}$ for all $i$ from $1$ to $n-k+1$.</p><p>The students quickly solved the problem. Can you do it too?</p><center> <img class="tex-graphics" src="file://srpKUUnO.png" style="max-width: 100.0%;max-height: 100.0%;"> </center></div><div class="input-specification"><p>The first line of the input contains two integers $n$ and $k$ ($1 \le n \le 2 \cdot 10^5$, $1 \le k \le n$, $k$ is odd) — the length of the sequence and the length of subarrays for which it is necessary to determine whether they are palindromes.</p><p>The second line of the input contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 2 \cdot 10^5$) — the sequence itself.</p></div><div class="output-specification"><p>Output a single integer — the total palindromicity of all subarrays of length $k$.</p></div>

## Input

<p>The first line of the input contains two integers $n$ and $k$ ($1 \le n \le 2 \cdot 10^5$, $1 \le k \le n$, $k$ is odd) — the length of the sequence and the length of subarrays for which it is necessary to determine whether they are palindromes.</p><p>The second line of the input contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 2 \cdot 10^5$) — the sequence itself.</p>

## Output

<p>Output a single integer — the total palindromicity of all subarrays of length $k$.</p>





```input1
8 5
1 2 8 2 5 2 8 6
```




```input2
9 9
1 2 3 4 5 4 3 2 1
```




```output1
4
```




```output2
0
```



## Note

<p>In the first example, the palindromicity of the subarray $[1, 2, 8, 2, 5]$ is $1$, the palindromicity of the string $[2, 8, 2, 5, 2]$ is also $1$, the palindromicity of the string $[8, 2, 5, 2, 8]$ is $0$, and the palindromicity of the string $[2, 5, 2, 8, 6]$ is $2$. The total palindromicity is $1+1+0+2 = 4$.</p><p>In the second example, the only substring of length $9$ coincides with the entire string, and its palindromicity is $0$, so the answer is also $0$.</p>
