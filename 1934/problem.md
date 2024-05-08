## Description

<div><p>$n$ students attended the first meeting of the Berland SU programming course ($n$ is even). All students will be divided into two groups. Each group will be attending exactly one lesson each week during one of the five working days (Monday, Tuesday, Wednesday, Thursday and Friday), and the days chosen for the groups must be different. Furthermore, both groups should contain the same number of students.</p><p>Each student has filled a survey in which they told which days of the week are convenient for them to attend a lesson, and which are not. </p><p>Your task is to determine if it is possible to choose two different week days to schedule the lessons for the group (the first group will attend the lesson on the first chosen day, the second group will attend the lesson on the second chosen day), and divide the students into two groups, so the groups have equal sizes, and for each student, the chosen lesson day for their group is convenient.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>Then the descriptions of $t$ testcases follow.</p><p>The first line of each testcase contains one integer $n$ ($2 \le n \le 1\,000$)&nbsp;— the number of students.</p><p>The $i$-th of the next $n$ lines contains $5$ integers, each of them is $0$ or $1$. If the $j$-th integer is $1$, then the $i$-th student can attend the lessons on the $j$-th day of the week. If the $j$-th integer is $0$, then the $i$-th student cannot attend the lessons on the $j$-th day of the week. </p><p>Additional constraints on the input: for each student, at least one of the days of the week is convenient, the total number of students over all testcases doesn't exceed $10^5$.</p></div><div class="output-specification"><p>For each testcase print an answer. If it's possible to divide the students into two groups of equal sizes and choose different days for the groups so each student can attend the lesson in the chosen day of their group, print "<span class="tex-font-style-tt">YES</span>" (without quotes). Otherwise, print "<span class="tex-font-style-tt">NO</span>" (without quotes). </p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>Then the descriptions of $t$ testcases follow.</p><p>The first line of each testcase contains one integer $n$ ($2 \le n \le 1\,000$)&nbsp;— the number of students.</p><p>The $i$-th of the next $n$ lines contains $5$ integers, each of them is $0$ or $1$. If the $j$-th integer is $1$, then the $i$-th student can attend the lessons on the $j$-th day of the week. If the $j$-th integer is $0$, then the $i$-th student cannot attend the lessons on the $j$-th day of the week. </p><p>Additional constraints on the input: for each student, at least one of the days of the week is convenient, the total number of students over all testcases doesn't exceed $10^5$.</p>

## Output

<p>For each testcase print an answer. If it's possible to divide the students into two groups of equal sizes and choose different days for the groups so each student can attend the lesson in the chosen day of their group, print "<span class="tex-font-style-tt">YES</span>" (without quotes). Otherwise, print "<span class="tex-font-style-tt">NO</span>" (without quotes). </p>





```input1
2
4
1 0 0 1 0
0 1 0 0 1
0 0 0 1 0
0 1 0 1 0
2
0 0 0 1 0
0 0 0 1 0
```




```output1
YES
NO
```



## Note

<p>In the first testcase, there is a way to meet all the constraints. For example, the first group can consist of the first and the third students, they will attend the lessons on Thursday (the fourth day); the second group can consist of the second and the fourth students, and they will attend the lessons on Tuesday (the second day).</p><p>In the second testcase, it is impossible to divide the students into groups so they attend the lessons on different days.</p>
