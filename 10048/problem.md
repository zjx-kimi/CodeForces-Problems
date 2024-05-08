## Description

<div><p>The New Year has arrived in the Master's Assistance Center, which means it's time to introduce a new feature!</p><p>Now students are given distance learning courses, with a total of $n$ courses available. For the $i$-th distance learning course, a student can receive a grade ranging from $x_i$ to $y_i$.</p><p>However, not all courses may be available to each student. Specifically, the $j$-th student is only given courses with numbers from $l_j$ to $r_j$, meaning the distance learning courses with numbers $l_j, l_j + 1, \ldots, r_j$.</p><p>The creators of the distance learning courses have decided to determine the final grade in a special way. Let the $j$-th student receive grades $c_{l_j}, c_{l_j + 1}, \ldots, c_{r_j}$ for their distance learning courses. Then their final grade will be equal to $c_{l_j}$ $|$ $c_{l_j + 1}$ $|$ $\ldots$ $|$ $c_{r_j}$, where $|$ denotes the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#OR">bitwise OR</a> operation.</p><p>Since the chatbot for solving distance learning courses is broken, the students have asked for your help. For each of the $q$ students, tell them the maximum final grade they can achieve.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 2 \cdot 10^4$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$) — the number of distance learning courses.</p><p>Each of the following $n$ lines contains two integers $x_i$ and $y_i$ ($0 \le x_i \le y_i &lt; 2^{30}$) — the minimum and maximum grade that can be received for the $i$-th course.</p><p>The next line contains a single integer $q$ ($1 \le q \le 2\cdot10^5$) — the number of students.</p><p>Each of the following $q$ lines contains two integers $l_j$ and $r_j$ ($1 \le l_j \le r_j \le n$) — the minimum and maximum course numbers accessible to the $j$-th student.</p><p>It is guaranteed that the sum of $n$ over all test cases and the sum of $q$ over all test cases do not exceed $2\cdot10^5$.</p></div><div class="output-specification"><p>For each test case, output $q$ integers, where the $j$-th integer is the maximum final grade that the $j$-th student can achieve.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 2 \cdot 10^4$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$) — the number of distance learning courses.</p><p>Each of the following $n$ lines contains two integers $x_i$ and $y_i$ ($0 \le x_i \le y_i &lt; 2^{30}$) — the minimum and maximum grade that can be received for the $i$-th course.</p><p>The next line contains a single integer $q$ ($1 \le q \le 2\cdot10^5$) — the number of students.</p><p>Each of the following $q$ lines contains two integers $l_j$ and $r_j$ ($1 \le l_j \le r_j \le n$) — the minimum and maximum course numbers accessible to the $j$-th student.</p><p>It is guaranteed that the sum of $n$ over all test cases and the sum of $q$ over all test cases do not exceed $2\cdot10^5$.</p>

## Output

<p>For each test case, output $q$ integers, where the $j$-th integer is the maximum final grade that the $j$-th student can achieve.</p>





```input1|2,3,4,5,6,7,8,20,21,22,23,24,25,26,27,28,29,30,31
3
2
0 1
3 4
3
1 1
1 2
2 2
4
1 7
1 7
3 10
2 2
5
1 3
3 4
2 3
1 4
1 2
6
1 2
2 2
0 1
1 1
3 3
0 0
4
3 4
5 5
2 5
1 2
```




```output1
1 5 4 
15 11 15 15 7 
1 3 3 3
```



## Note

<p>In the first test case:</p><ol> <li> The maximum grade for the first student is $1$: <ul> <li> On the first distance learning course, he will receive a grade of $1$. </li></ul> Therefore, the final grade is $1$.<p> </p></li><li> The maximum grade for the second student is $5$: <ul> <li> On the first distance learning course, he will receive a grade of $1$. </li><li> On the second distance learning course, he will receive a grade of $4$. </li></ul> Therefore, the final grade is $1$ $|$ $4$ $=$ $5$.</li><li> The maximum grade for the third student is $4$: <ul> <li> On the second distance learning course, he will receive a grade of $4$. </li></ul> Therefore, the final grade is $4$. </li></ol><p>In the second test case:</p><ol> <li> The maximum grade for the first student is $15$: <ul> <li> On the first distance learning course, he will receive a grade of $7$. </li><li> On the second distance learning course, he will receive a grade of $4$. </li><li> On the third distance learning course, he will receive a grade of $8$. </li></ul> Therefore, the final grade is $7$ $|$ $4$ $|$ $8$ $=$ $15$.<p> </p></li><li> The maximum grade for the second student is $11$: <ul> <li> On the third distance learning course, he will receive a grade of $9$. </li><li> On the fourth distance learning course, he will receive a grade of $2$. </li></ul> Therefore, the final grade is $9$ $|$ $2$ $=$ $11$. </li></ol>
