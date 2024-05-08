## Description

<div><p>For the simplicity, let's say that the "Death Note" is a notebook that kills a person when their name is written in it.</p><p>It's easy to kill with it, but it's pretty hard to keep track of people you haven't killed and still plan to. You decided to make a "Death Database Management System"&nbsp;— a computer program that provides the easy access to the database of possible victims. Let me describe its specifications to you.</p><p>Let's define a victim entity: a victim has a name (not necessarily unique) that consists only of lowercase Latin letters and an integer suspicion value.</p><p>At the start of the program the user enters a list of $n$ victim names into a database, each suspicion value is set to $0$.</p><p>Then the user makes queries of two types: </p><ul> <li> $1~i~x$&nbsp;— set the suspicion value of the $i$-th victim to $x$; </li><li> $2~q$&nbsp;— given a string $q$ find the maximum suspicion value of a victim whose name is a contiguous substring of $q$. </li></ul><p>Just to remind you, this program doesn't kill people, it only helps to search for the names to write down in an actual notebook. Thus, the list of the victims in the database doesn't change throughout the queries.</p><p>What are you waiting for? Write that program now!</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $m$ ($1 \le n, m \le 3 \cdot 10^5$)&nbsp;— the number of victims and the number of queries, respectively.</p><p>Each of the next $n$ lines contains a single string $s_i$&nbsp;— the name of the $i$-th victim. Each name consists only of lowercase Latin letters.</p><p>Each of the next $m$ lines contains a query of one of two types: </p><ul> <li> $1~i~x$ ($1 \le i \le n$, $0 \le x \le 10^9$)&nbsp;— change the suspicion value of the $i$-th victim to $x$; </li><li> $2~q$&nbsp;— given a string $q$ consisting only of lowercase Latin letters find the maximum suspicion value of a victim whose name is a contiguous substring of $q$. </li></ul><p>There is at least one query of the second type. The total length of the strings $s_i$ doesn't exceed $3 \cdot 10^5$. The total length of the strings $q$ doesn't exceed $3 \cdot 10^5$. </p></div><div class="output-specification"><p>For each query of the second type print an integer value. If there is no victim name that is a contiguous substring of $q$, then print $-1$. Otherwise, print the maximum suspicion value of a victim whose name is a contiguous substring of $q$.</p></div>

## Input

<p>The first line contains two integers $n$ and $m$ ($1 \le n, m \le 3 \cdot 10^5$)&nbsp;— the number of victims and the number of queries, respectively.</p><p>Each of the next $n$ lines contains a single string $s_i$&nbsp;— the name of the $i$-th victim. Each name consists only of lowercase Latin letters.</p><p>Each of the next $m$ lines contains a query of one of two types: </p><ul> <li> $1~i~x$ ($1 \le i \le n$, $0 \le x \le 10^9$)&nbsp;— change the suspicion value of the $i$-th victim to $x$; </li><li> $2~q$&nbsp;— given a string $q$ consisting only of lowercase Latin letters find the maximum suspicion value of a victim whose name is a contiguous substring of $q$. </li></ul><p>There is at least one query of the second type. The total length of the strings $s_i$ doesn't exceed $3 \cdot 10^5$. The total length of the strings $q$ doesn't exceed $3 \cdot 10^5$. </p>

## Output

<p>For each query of the second type print an integer value. If there is no victim name that is a contiguous substring of $q$, then print $-1$. Otherwise, print the maximum suspicion value of a victim whose name is a contiguous substring of $q$.</p>





```input1
5 8
kurou
takuo
takeshi
naomi
shingo
2 nakiraomi
2 abanaomicaba
1 3 943
2 takuotakeshishingo
1 5 135832
2 shingotakeshi
1 5 0
2 shingotakeshi
```




```input2
6 15
a
ab
ba
b
a
ba
2 aa
1 4 4
2 bbb
1 2 1
1 2 18
2 b
2 c
1 6 10
2 aba
2 abbbba
1 2 12
2 bbaaab
1 1 11
1 5 5
2 baa
```




```output1
-1
0
943
135832
943
```




```output2
0
4
4
-1
18
18
12
11
```


