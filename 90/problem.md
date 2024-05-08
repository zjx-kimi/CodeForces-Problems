## Description

<div><p>BerSoft is the biggest IT corporation in Berland. There are $n$ employees at BerSoft company, numbered from $1$ to $n$. </p><p>The first employee is the head of the company, and he does not have any superiors. Every other employee $i$ has exactly one direct superior $p_i$.</p><p>Employee $x$ is considered to be a superior (direct or indirect) of employee $y$ if one of the following conditions holds: </p><ul> <li> employee $x$ is the direct superior of employee $y$; </li><li> employee $x$ is a superior of the direct superior of employee $y$. </li></ul><p>The structure of BerSoft is organized in such a way that the head of the company is superior of every employee.</p><p>A programming competition is going to be held soon. Two-person teams should be created for this purpose. However, if one employee in a team is the superior of another, they are uncomfortable together. So, teams of two people should be created so that no one is the superior of the other. Note that no employee can participate in more than one team.</p><p>Your task is to calculate the maximum possible number of teams according to the aforementioned rules.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 2 \cdot 10^5$)&nbsp;— the number of employees.</p><p>The second line contains $n-1$ integers $p_2, p_3, \dots, p_n$ ($1 \le p_i \le n$), where $p_i$ is the index of the direct superior of the $i$-th employee.</p><p>The sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print a single integer&nbsp;— the maximum possible number of teams according to the aforementioned rules.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 2 \cdot 10^5$)&nbsp;— the number of employees.</p><p>The second line contains $n-1$ integers $p_2, p_3, \dots, p_n$ ($1 \le p_i \le n$), where $p_i$ is the index of the direct superior of the $i$-th employee.</p><p>The sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, print a single integer&nbsp;— the maximum possible number of teams according to the aforementioned rules.</p>





```input1|2,3,6,7,10,11
6
4
1 2 1
2
1
5
5 5 5 1
7
1 2 1 1 3 3
7
1 1 3 2 2 4
7
1 2 1 1 1 3
```




```output1
1
0
1
3
3
3
```



## Note

<p>In the first test case, team $(3, 4)$ can be created.</p><p>In the second test case, no team can be created, because there are only $2$ employees and one is the superior of another.</p><p>In the third test case, team $(2, 3)$ can be created.</p><p>In the fourth test case, teams $(2, 4)$, $(3, 5)$ and $(6, 7)$ can be created.</p><p>In the fifth test case, teams $(2, 3)$, $(6, 4)$ and $(5, 7)$ can be created.</p>
