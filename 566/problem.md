## Description

<div><p>$n$ people came to the festival and decided to dance a few round dances. There are at least $2$ people in the round dance and each person has exactly two neighbors. If there are $2$ people in the round dance then they have the same neighbor on each side.</p><p>You decided to find out exactly how many dances there were. But each participant of the holiday remembered exactly <span class="tex-font-style-bf">one</span> neighbor. Your task is to determine what the minimum and maximum number of round dances could be.</p><p>For example, if there were $6$ people at the holiday, and the numbers of the neighbors they remembered are equal $[2, 1, 4, 3, 6, 5]$, then the <span class="tex-font-style-bf">minimum</span> number of round dances is$1$: </p><ul> <li>$1 - 2 - 3 - 4 - 5 - 6 - 1$ </li></ul> and the <span class="tex-font-style-bf">maximum</span> is $3$: <ul> <li> $1 - 2 - 1$ </li><li> $3 - 4 - 3$ </li><li> $5 - 6 - 5$ </li></ul></div><div class="input-specification"><p>The first line contains a positive number $t$ ($1 \le t \le 10^4$) — the number of test cases. The following is a description of the test cases.</p><p>The first line of the description of each test case contains a positive number $n$ ($2 \le n \le 2 \cdot 10^5$) — the number of people at the holiday.</p><p>The second line of the description of each test case contains $n$ integers $a_i$ ($1 \le a_i \le n, a_i \neq i$) — the number of the neighbor that the $i$th person remembered.</p><p>It is guaranteed that the test cases are correct and corresponds to at least one division of people into round dances.</p><p>It is guaranteed that the sum of $n$ for all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output two integers — the minimum and maximum number of round dances that could be.</p></div>

## Input

<p>The first line contains a positive number $t$ ($1 \le t \le 10^4$) — the number of test cases. The following is a description of the test cases.</p><p>The first line of the description of each test case contains a positive number $n$ ($2 \le n \le 2 \cdot 10^5$) — the number of people at the holiday.</p><p>The second line of the description of each test case contains $n$ integers $a_i$ ($1 \le a_i \le n, a_i \neq i$) — the number of the neighbor that the $i$th person remembered.</p><p>It is guaranteed that the test cases are correct and corresponds to at least one division of people into round dances.</p><p>It is guaranteed that the sum of $n$ for all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output two integers — the minimum and maximum number of round dances that could be.</p>





```input1|2,3,6,7,10,11,14,15,18,19
10
6
2 1 4 3 6 5
6
2 3 1 5 6 4
9
2 3 2 5 6 5 8 9 8
2
2 1
4
4 3 2 1
5
2 3 4 5 1
6
5 3 4 1 1 2
5
3 5 4 1 2
6
6 3 2 5 4 3
6
5 1 4 3 4 2
```




```output1
1 3
2 2
1 3
1 1
1 2
1 1
1 1
2 2
1 2
1 1
```


