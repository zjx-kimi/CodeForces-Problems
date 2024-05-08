## Description

<div><p>Polycarp is an organizer of a Berland ICPC regional event. There are $n$ universities in Berland numbered from $1$ to $n$. Polycarp knows all competitive programmers in the region. There are $n$ students: the $i$-th student is enrolled at a university $u_i$ and has a programming skill $s_i$.</p><p>Polycarp has to decide on the rules now. In particular, the number of members in the team.</p><p>Polycarp knows that if he chooses the size of the team to be some integer $k$, each university will send their $k$ strongest (with the highest programming skill $s$) students in the first team, the next $k$ strongest students in the second team and so on. If there are fewer than $k$ students left, then the team can't be formed. Note that there might be universities that send zero teams.</p><p>The strength of the region is the total skill of the members of all present teams. If there are no teams present, then the strength is $0$.</p><p>Help Polycarp to find the strength of the region for each choice of $k$ from $1$ to $n$.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of universities and the number of students.</p><p>The second line of each testcase contains $n$ integers $u_1, u_2, \dots, u_n$ ($1 \le u_i \le n$)&nbsp;— the university the $i$-th student is enrolled at.</p><p>The third line of each testcase contains $n$ integers $s_1, s_2, \dots, s_n$ ($1 \le s_i \le 10^9$)&nbsp;— the programming skill of the $i$-th student.</p><p>The sum of $n$ over all testcases doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each testcase print $n$ integers: the strength of the region&nbsp;— the total skill of the members of the present teams&nbsp;— for each choice of team size $k$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of universities and the number of students.</p><p>The second line of each testcase contains $n$ integers $u_1, u_2, \dots, u_n$ ($1 \le u_i \le n$)&nbsp;— the university the $i$-th student is enrolled at.</p><p>The third line of each testcase contains $n$ integers $s_1, s_2, \dots, s_n$ ($1 \le s_i \le 10^9$)&nbsp;— the programming skill of the $i$-th student.</p><p>The sum of $n$ over all testcases doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>For each testcase print $n$ integers: the strength of the region&nbsp;— the total skill of the members of the present teams&nbsp;— for each choice of team size $k$.</p>





```input1
4
7
1 2 1 2 1 2 1
6 8 3 1 5 1 5
10
1 1 1 2 2 2 2 3 3 3
3435 3014 2241 2233 2893 2102 2286 2175 1961 2567
6
3 3 3 3 3 3
5 9 6 7 9 7
1
1
3083
```




```output1
29 28 26 19 0 0 0 
24907 20705 22805 9514 0 0 0 0 0 0 
43 43 43 32 38 43 
3083
```



## Note

<p>In the first testcase the teams from each university for each $k$ are: </p><ul> <li> $k=1$: <ul> <li> university $1$: $[6], [5], [5], [3]$; </li><li> university $2$: $[8], [1], [1]$; </li></ul> </li><li> $k=2$: <ul> <li> university $1$: $[6, 5], [5, 3]$; </li><li> university $2$: $[8, 1]$; </li></ul> </li><li> $k=3$: <ul> <li> university $1$: $[6, 5, 5]$; </li><li> university $2$: $[8, 1, 1]$; </li></ul> </li><li> $k=4$: <ul> <li> university $1$: $[6, 5, 5, 3]$; </li></ul> </li></ul>
