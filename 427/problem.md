## Description

<div><p><span class="tex-font-style-it">This is an easy version of this problem. The only difference between the versions is that you have to solve the hard version in online mode. You can make hacks only if both versions of the problem are solved.</span></p><p>You have an array $a$, which is initially empty. You need to process queries of the following types:</p><ul> <li> <span class="tex-font-style-tt">+</span> $x$&nbsp;— add the integer $x$ to the end of the array $a$. </li><li> <span class="tex-font-style-tt">-</span> $k$&nbsp;— remove the last $k$ numbers from the array $a$. </li><li> <span class="tex-font-style-tt">!</span>&nbsp;— roll back the last active change (i.e., make the array $a$ the way it was before the change). In this problem, only queries of the first two types (<span class="tex-font-style-tt">+</span> and <span class="tex-font-style-tt">-</span>) are considered as changes. </li><li> <span class="tex-font-style-tt">?</span>&nbsp;— find the number of distinct numbers in the array $a$. </li></ul></div><div class="input-specification"><p>The first line contains an integer $q$ ($1 \leq q \leq 10^6$)&nbsp;— the number of queries.</p><p>The next $q$ lines contain the queries as described above.</p><p>It is guaranteed that </p><ul> <li> in the queries of the first type, $1 \le x \le 10^6$; </li><li> in the queries of the second type, $k \ge 1$ and $k$ does not exceed the current length of the array $a$; </li><li> at the moment of the queries of the third type, there is at least one query of the first or of the second type that can be rolled back. </li></ul><p>It is also guaranteed that the number of queries of the fourth type (<span class="tex-font-style-tt">?</span>) does not exceed $10^5$.</p></div><div class="output-specification"><p>For each query of the fourth type output one integer&nbsp;— the number of distinct elements in array $a$ at the moment of query.</p></div>

## Input

<p>The first line contains an integer $q$ ($1 \leq q \leq 10^6$)&nbsp;— the number of queries.</p><p>The next $q$ lines contain the queries as described above.</p><p>It is guaranteed that </p><ul> <li> in the queries of the first type, $1 \le x \le 10^6$; </li><li> in the queries of the second type, $k \ge 1$ and $k$ does not exceed the current length of the array $a$; </li><li> at the moment of the queries of the third type, there is at least one query of the first or of the second type that can be rolled back. </li></ul><p>It is also guaranteed that the number of queries of the fourth type (<span class="tex-font-style-tt">?</span>) does not exceed $10^5$.</p>

## Output

<p>For each query of the fourth type output one integer&nbsp;— the number of distinct elements in array $a$ at the moment of query.</p>





```input1
10
+ 1
+ 2
+ 2
?
!
+ 3
- 2
?
+ 1
?
```




```input2
6
+ 1
+ 1000000
?
!
!
?
```




```output1
2
1
1
```




```output2
2
0
```



## Note

<p>In the first example array $a$ changes as follows: </p><ol> <li> After the first query, $a=[1]$. </li><li> After the second query, $a=[1,2]$. </li><li> After the third query, $a=[1,2,2]$. </li><li> At the moment of the fourth query, there are $2$ distinct intergers in the array $a$: $1$ and $2$. </li><li> After the fifth query, $a=[1,2]$ (rolled back the change <span class="tex-font-style-tt">+ 2</span>). </li><li> After the sixth query, $a=[1,2,3]$. </li><li> After the seventh query, $a=[1]$. </li><li> At the moment of the eigth query, there is only one $1$ in the array $a$. </li><li> After the ninth query, $a=[1,1]$. </li><li> At the moment of the tenth query, there are only two $1$ in the array $a$. </li></ol><p>In the second example array $a$ changes as follows: </p><ol> <li> After the first query, $a=[1]$. </li><li> After the second query, $a=[1,1\,000\,000]$. </li><li> At the moment of the third query, there are $2$ distinct intergers in the array $a$: $1$ and $1\,000\,000$. </li><li> After the fourth query, $a=[1]$ (rolled back the change <span class="tex-font-style-tt">+ 1000000</span>). </li><li> After the fifth query, $a=[]$ (rolled back the change <span class="tex-font-style-tt">+ 1</span>). </li><li> At the moment of the sixth query, there are no integers in the array $a$, so the answer to this query is $0$. </li></ol>
