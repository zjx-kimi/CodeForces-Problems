## Description

<div><p>The organizing committee plans to take the participants of the Olympiad on a hike after the tour. Currently, the number of tents needed to be taken is being calculated. It is known that each tent can accommodate up to $3$ people.</p><p>Among the participants, there are $a$ introverts, $b$ extroverts, and $c$ universals:</p><ul> <li> Each introvert wants to live in a tent alone. Thus, a tent with an introvert must contain exactly one person&nbsp;— only the introvert himself. </li><li> Each extrovert wants to live in a tent with two others. Thus, the tent with an extrovert must contain exactly three people. </li><li> Each universal is fine with any option (living alone, with one other person, or with two others). </li></ul><p>The organizing committee respects the wishes of each participant very much, so they want to fulfill all of them.</p><p>Tell us the minimum number of tents needed to be taken so that all participants can be accommodated according to their preferences. If it is impossible to accommodate the participants in a way that fulfills all the wishes, output $-1$.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. This is followed by the descriptions of the test cases.</p><p>Each test case is described by a single line containing three integers $a$, $b$, $c$ ($0 \le a, b, c \le 10^9$)&nbsp;— the number of introverts, extroverts, and universals, respectively.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the minimum number of tents, or $-1$ if it is impossible to accommodate the participants.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. This is followed by the descriptions of the test cases.</p><p>Each test case is described by a single line containing three integers $a$, $b$, $c$ ($0 \le a, b, c \le 10^9$)&nbsp;— the number of introverts, extroverts, and universals, respectively.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the minimum number of tents, or $-1$ if it is impossible to accommodate the participants.</p>





```input1|2,4,6,8,10
10
1 2 3
1 4 1
1 4 2
1 1 1
1 3 2
19 7 18
0 0 0
7 0 0
0 24 0
1000000000 1000000000 1000000000
```




```output1
3
-1
3
-1
3
28
0
7
8
1666666667
```



## Note

<p>In the first test case, $1$ tent will be given to the introverts, $1$ tent will be shared by two extroverts and one universal, and the last tent will be shared by two universals. In total, $3$ tents are needed.</p><p>In the second test case, three extroverts will take $1$ tent, and $1$ tent will be taken by an introvert. Then, one extrovert and one universal will be left. This extrovert will not be able to live with two others.</p>
