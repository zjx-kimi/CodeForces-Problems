## Description

<div><p>You are given an integer $n$.</p><p>Your task is to build a string of uppercase Latin letters. There must be exactly $n$ special characters in this string. Let's call a character <span class="tex-font-style-it">special</span> if it is equal to exactly one of its neighbors.</p><p>For example, there are $6$ special characters in the <span class="tex-font-style-tt">AAABAACC</span> string (at positions: $1$, $3$, $5$, $6$, $7$ and $8$).</p><p>Print any suitable string or report that there is no such string.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 50$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains a single integer $n$ ($1 \le n \le 50$).</p></div><div class="output-specification"><p>For each test case, print the answer as follows: </p><ul> <li> if there is no suitable string, print one line containing the string <span class="tex-font-style-tt">NO</span>; </li><li> otherwise, print two lines. The first line should contain the string <span class="tex-font-style-tt">YES</span>; on the second line print a string of length <span class="tex-font-style-bf">at most $200$</span>&nbsp;— the answer itself (it can be shown that if some answers exist, then there is an answer of length at most $200$). If there are several solutions, print any of them. </li></ul></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 50$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains a single integer $n$ ($1 \le n \le 50$).</p>

## Output

<p>For each test case, print the answer as follows: </p><ul> <li> if there is no suitable string, print one line containing the string <span class="tex-font-style-tt">NO</span>; </li><li> otherwise, print two lines. The first line should contain the string <span class="tex-font-style-tt">YES</span>; on the second line print a string of length <span class="tex-font-style-bf">at most $200$</span>&nbsp;— the answer itself (it can be shown that if some answers exist, then there is an answer of length at most $200$). If there are several solutions, print any of them. </li></ul>





```input1|2,4
3
6
1
2
```




```output1
YES
AAABAACC
NO
YES
MM
```


