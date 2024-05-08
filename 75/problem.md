## Description

<div><p>In the $31$st lyceum, there were two groups of olympiad participants: computer science and mathematics. The number of computer scientists was $n_1$, and the number of mathematicians was $n_2$. It is not known for certain who belonged to which group, but it is known that there were friendly connections between some pairs of people (these connections could exist between a pair of people from the same group or from different groups).</p><p>The connections were so strong that even if one person is removed along with all their friendly connections, any pair of people still remains acquainted either directly or through mutual friends.</p><p>$^{\dagger}$ More formally, two people $(x, y)$ are acquainted in the following case: there are people $a_1, a_2, \ldots,a_n$ ($1 \le a_i \le n_1 + n_2$) such that the following conditions are simultaneously met:</p><p>$\bullet$ Person $x$ is directly acquainted with $a_1$.</p><p>$\bullet$ Person $a_n$ is directly acquainted with $y$.</p><p>$\bullet$ Person $a_i$ is directly acquainted with $a_{i + 1}$ for any ($1 \le i \le n - 1$).</p><p>The teachers were dissatisfied with the fact that computer scientists were friends with mathematicians and vice versa, so they decided to divide the students into two groups in such a way that the following two conditions are met:</p><p>$\bullet$ There were $n_1$ people in the computer science group, and $n_2$ people in the mathematics group.</p><p>$\bullet$ Any pair of computer scientists should be acquainted (acquaintance involving mutual friends, who must be from the same group as the people in the pair, is allowed), the same should be true for mathematicians.</p><p>Help them solve this problem and find out who belongs to which group.</p></div><div class="input-specification"><p>Each test consists of several test cases. The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases. Then follows the description of the test cases.</p><p>The first line of each test case contains three integers $n_1$, $n_2$, and $m$ ($1 \le n_1, n_2 \le 2000$, $1 \le m \le 5000$). $n_1$, $n_2$ are the sizes of the two groups described in the problem, and $m$ is the number of friendly connections initially.</p><p>The following $m$ lines describe the friendly connections: in the $i$-th ($1 \le i \le m$) line, a pair of numbers $(a, b)$ is given, which means that the person with number $a$ is friends with the person with number $b$ (and vice versa).</p><p>It is guaranteed that for each test case, all friendly connections are distinct.</p><p>It is guaranteed that the sum of $n_1 + n_2$ for all test cases does not exceed $2000$, and the sum of $m$ for all test cases does not exceed $5000$.</p><p>It is also guaranteed that for each test case, a solution exists.</p><p>If there are several answers, print any of them.</p></div><div class="output-specification"><p>For each test case, output two lines.</p><p>In the first line, output $n_1$ distinct numbers $a_i$ ($1 \le a_i \le n_1 + n_2$)&nbsp;— the people belonging to the first group.</p><p>In the second line, output $n_2$ distinct numbers $b_i$ ($1 \le b_i \le n_1 + n_2$)&nbsp;— the people belonging to the second group.</p><p>All numbers must be distinct.</p><p>If there are several possible answers, print any one.</p></div>

## Input

<p>Each test consists of several test cases. The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases. Then follows the description of the test cases.</p><p>The first line of each test case contains three integers $n_1$, $n_2$, and $m$ ($1 \le n_1, n_2 \le 2000$, $1 \le m \le 5000$). $n_1$, $n_2$ are the sizes of the two groups described in the problem, and $m$ is the number of friendly connections initially.</p><p>The following $m$ lines describe the friendly connections: in the $i$-th ($1 \le i \le m$) line, a pair of numbers $(a, b)$ is given, which means that the person with number $a$ is friends with the person with number $b$ (and vice versa).</p><p>It is guaranteed that for each test case, all friendly connections are distinct.</p><p>It is guaranteed that the sum of $n_1 + n_2$ for all test cases does not exceed $2000$, and the sum of $m$ for all test cases does not exceed $5000$.</p><p>It is also guaranteed that for each test case, a solution exists.</p><p>If there are several answers, print any of them.</p>

## Output

<p>For each test case, output two lines.</p><p>In the first line, output $n_1$ distinct numbers $a_i$ ($1 \le a_i \le n_1 + n_2$)&nbsp;— the people belonging to the first group.</p><p>In the second line, output $n_2$ distinct numbers $b_i$ ($1 \le b_i \le n_1 + n_2$)&nbsp;— the people belonging to the second group.</p><p>All numbers must be distinct.</p><p>If there are several possible answers, print any one.</p>





```input1|2,3,4,5,14,15,16,17,18,19,20,21
3
1 2 3
2 3
1 3
1 2
1 4 7
2 5
3 4
2 4
1 2
3 5
4 5
1 5
3 3 7
1 2
1 6
2 3
2 5
3 4
4 5
4 6
```




```output1
3 
1 2 
5 
1 2 3 4 
4 5 6 
1 2 3
```



## Note

<p>Consider the third test case. The division into groups looks as follows: </p><center> <img class="tex-graphics" src="file://0PwRnoGs.png" style="max-width: 100.0%;max-height: 100.0%;"> </center> The students selected as computer scientists are colored in green, and those selected as mathematicians are colored in blue.<p>Consider all pairs of computer scientists and how they are acquainted:</p><p>Pairs $(4, 5), (4, 6)$ are directly acquainted.</p><p>Pair $(5, 6)$ is acquainted through the computer scientist with number $4$.</p><p>Consider all pairs of mathematicians and how they are acquainted:</p><p>Pairs $(1, 2), (2, 3)$ are directly acquainted.</p><p>Pair $(1, 3)$ is acquainted through the mathematician with number $2$.</p><p>We conclude that any pair of people belonging to the same group is acquainted with each other, thus the division into two groups is correct.</p>
