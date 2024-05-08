## Description

<div><p>Beppa and her circle of geek friends keep up to date on a group chat in the instant messaging app SwerChat$^{\text{TM}}$.</p><p>The group has $n$ members, excluding Beppa. Each of those members has a unique ID between $1$ and $n$. When a user opens a group chat, SwerChat$^{\text{TM}}$ displays the list of other members of that group, sorted by <span class="tex-font-style-bf">decreasing</span> times of last seen online (so the member who opened the chat most recently is the first of the list). However, the times of last seen are not displayed.</p><p>Today, Beppa has been busy all day: she has only opened the group chat twice, once at 9:00 and once at 22:00. Both times, she wrote down the list of members in the order they appeared at that time. Now she wonders: what is the minimum number of other members that must have been online at least once between 9:00 and 22:00?</p><p>Beppa is sure that no two members are ever online at the same time and no members are online when Beppa opens the group chat at 9:00 and 22:00.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 10\,000$) — the number of test cases. The descriptions of the $t$ test cases follow.</p><p>The first line of each test case contains an integer $n$ ($1 \leq n \leq 10^5$) — the number of members of the group excluding Beppa.</p><p>The second line contains $n$ integers $a_1, \, a_2, \, \dots, \, a_n$ ($1 \le a_i \le n$) — the list of IDs of the members, sorted by decreasing times of last seen online at 9:00.</p><p>The third line contains $n$ integers $b_1, \, b_2, \, \dots, \, b_n$ ($1 \le b_i \le n$) — the list of IDs of the members, sorted by decreasing times of last seen online at 22:00.</p><p>For all $1\le i &lt; j\le n$, it is guaranteed that $a_i \ne a_j$ and $b_i \ne b_j$.</p><p>It is also guaranteed that the sum of the values of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, print the minimum number of members that must have been online between 9:00 and 22:00.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 10\,000$) — the number of test cases. The descriptions of the $t$ test cases follow.</p><p>The first line of each test case contains an integer $n$ ($1 \leq n \leq 10^5$) — the number of members of the group excluding Beppa.</p><p>The second line contains $n$ integers $a_1, \, a_2, \, \dots, \, a_n$ ($1 \le a_i \le n$) — the list of IDs of the members, sorted by decreasing times of last seen online at 9:00.</p><p>The third line contains $n$ integers $b_1, \, b_2, \, \dots, \, b_n$ ($1 \le b_i \le n$) — the list of IDs of the members, sorted by decreasing times of last seen online at 22:00.</p><p>For all $1\le i &lt; j\le n$, it is guaranteed that $a_i \ne a_j$ and $b_i \ne b_j$.</p><p>It is also guaranteed that the sum of the values of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, print the minimum number of members that must have been online between 9:00 and 22:00.</p>





```input1|2,3,4,8,9,10
4
5
1 4 2 5 3
4 5 1 2 3
6
1 2 3 4 5 6
1 2 3 4 5 6
8
8 2 4 7 1 6 5 3
5 6 1 4 8 2 7 3
1
1
1
```




```output1
2
0
4
0
```



## Note

<p>In the <span class="tex-font-style-bf">first test case</span>, members $4, 5$ must have been online between 9:00 and 22:00.</p><p>In the <span class="tex-font-style-bf">second test case</span>, it is possible that nobody has been online between 9:00 and 22:00.</p>
