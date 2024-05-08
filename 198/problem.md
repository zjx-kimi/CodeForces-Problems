## Description

<div><p>Vanya and Vova are playing a game. Players are given an integer $n$. On their turn, the player can add $1$ to the current integer or subtract $1$. The players take turns; Vanya starts. If <span class="tex-font-style-bf">after</span> Vanya's move the integer is divisible by $3$, then he wins. If $10$ moves have passed and Vanya has not won, then Vova wins.</p><p>Write a program that, based on the integer $n$, determines who will win if both players play optimally.</p></div><div class="input-specification"><p>The first line contains the integer $t$ ($1 \leq t \leq 100$)&nbsp;— the number of test cases.</p><p>The single line of each test case contains the integer $n$ ($1 \leq n \leq 1000$).</p></div><div class="output-specification"><p>For each test case, print "<span class="tex-font-style-tt">First</span>" without quotes if Vanya wins, and "<span class="tex-font-style-tt">Second</span>" without quotes if Vova wins.</p></div>

## Input

<p>The first line contains the integer $t$ ($1 \leq t \leq 100$)&nbsp;— the number of test cases.</p><p>The single line of each test case contains the integer $n$ ($1 \leq n \leq 1000$).</p>

## Output

<p>For each test case, print "<span class="tex-font-style-tt">First</span>" without quotes if Vanya wins, and "<span class="tex-font-style-tt">Second</span>" without quotes if Vova wins.</p>





```input1|2,4,6
6
1
3
5
100
999
1000
```




```output1
First
Second
First
First
Second
First
```


