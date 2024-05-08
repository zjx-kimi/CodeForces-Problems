## Description

<div><p>In a debate club with $n$ members, including yourself (member $1$), there are $k$ opinions to be discussed in sequence. During each discussion, members express their agreement or disagreement with the opinion. Let's define $Y$ as the number of members who agree and $N$ as the number of members who disagree. After each discussion, members leave the club based on the following criteria:</p><ul> <li> If more members agree than disagree ($Y &gt; N$), all members who disagreed leave the club. </li><li> If more members disagree than agree ($Y &lt; N$), all members who agreed leave the club. </li><li> If there is a tie ($Y = N$), all members leave the club. </li></ul><p>As the club president, your goal is to stay in the club and maximize the number of members remaining after the meeting. You have access to each member's stance on all $k$ opinions before the meeting starts, and you can expel any number of members (excluding yourself) before the meeting begins.</p><p>Determine the maximum number of members, including yourself, who can remain in the club after the meeting. You don't need to provide the specific expulsion strategy but only the maximum number of members that can stay. Ensure that you remain in the club after the meeting as well.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 1000$). Description of the test cases follows.</p><p>The first line of each test case contains two positive integers $n$ and $k$ ($1 \le n, k \le 100$) — the number of members and the number of discussions.</p><p>The $i$-th of the following $n$ lines contains a string $t_i$ of length $k$. The $j$-th character in the string $t_i$ indicates whether the $i$-th member agrees or disagrees with the $j$-th opinion if they are present during that discussion. A "<span class="tex-font-style-tt">+</span>" symbol means the member agrees, while a "<span class="tex-font-style-tt">-</span>" symbol means the member disagrees.</p><p>It is guaranteed that the sum of $n \cdot k$ over all test cases does not exceed $5 \cdot 10^4$.</p></div><div class="output-specification"><p>For each test case, output the maximum number of members, including yourself, who can remain in the club after the meeting.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 1000$). Description of the test cases follows.</p><p>The first line of each test case contains two positive integers $n$ and $k$ ($1 \le n, k \le 100$) — the number of members and the number of discussions.</p><p>The $i$-th of the following $n$ lines contains a string $t_i$ of length $k$. The $j$-th character in the string $t_i$ indicates whether the $i$-th member agrees or disagrees with the $j$-th opinion if they are present during that discussion. A "<span class="tex-font-style-tt">+</span>" symbol means the member agrees, while a "<span class="tex-font-style-tt">-</span>" symbol means the member disagrees.</p><p>It is guaranteed that the sum of $n \cdot k$ over all test cases does not exceed $5 \cdot 10^4$.</p>

## Output

<p>For each test case, output the maximum number of members, including yourself, who can remain in the club after the meeting.</p>





```input1|2,3,4,7,8,9,10,11,18,19,20,21,22
5
2 2
++
+-
1 3
+-+
4 1
+
-
-
+
5 4
++++
+--+
++-+
+-++
++++
4 2
++
--
--
-+
```




```output1
1
1
2
2
1
```



## Note

<p>For convenience, we will analyze the examples based on who actually attended the meeting (i.&nbsp;e. was <span class="tex-font-style-it">not</span> expelled) rather than who was expelled.</p><p>Example 1:</p><p>Only the first member could have attended the meeting, otherwise both members would have left after the second opinion is discussed.</p><p>Example 2:</p><p>There is only a single member that attends the meeting and stays till the end.</p><p>Example 3:</p><p>The club has $4$ members and only one opinion will be discussed during the meeting. Let's analyze the possible outcomes based on the participants in the meeting:</p><ul> <li> If only the first member attends, they'll be the only one left after the meeting. </li><li> If the first member attends with the second or third member, they will be a tie in the discussion, making them both leave. </li><li> If the first member attends with the second and third members, the first member will be in the minority and will leave after the discussion, which contradicts the statement. </li><li> If the first and fourth members attend, they will agree during the discussion and both remain till the end. </li><li> If the first, second, and fourth members attend, the second member will be in the minority during the discussion, and only the first and fourth members will remain at the end. The same happens if the second member is replaced by the third member. </li><li> If all four members attend, there will be a tie during the discussion, making everyone leave. </li></ul><p>The maximum number of members remaining after the meeting is $2$.</p><p>Example 4:</p><p>The club has $5$ members and $4$ opinions will be discussed during the meeting.</p><p>One way to achieve the maximum number of members is if only the first, third, and fifth members attend the meeting. In this case, they all agree during the first two discussions, after which the third member is in the minority during the third discussion. Then, the first and fifth members agree in the last discussion, and those two members stay till the end of the meeting.</p><p>Example 5:</p><p>The club has $4$ members and $2$ opinions will be discussed.</p><p>If the first three members attend the meeting, the first member will be in the minority during the first discussion and will leave the club. After that, the second and third members will both disagree with the second opinion, and they both will stay till the end of the meeting. In this way, there will be 2 members left after the meeting, but it is an invalid outcome, as it forces the first member to leave. Therefore, the maximum number of 1 member is achieved if only the first member attends the meeting.</p>
