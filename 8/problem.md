## Description

<div><p><span class="tex-font-style-it">This is an interactive problem!</span></p><p>Mr. 1048576 is one of those faculty who hates wasting his time in taking class attendance. Instead of taking attendance the old-fashioned way, he decided to try out something new today.</p><p>There are $n$ students in his class, having roll numbers $1$ to $n$. He knows that <span class="tex-font-style-bf">exactly $1$ student is absent</span> today. In order to determine who is absent, he can ask some queries to the class. In each query, he can provide two integers $l$ and $r$ ($1\leq l\leq r\leq n$) and all students whose roll numbers are between $l$ and $r$ (inclusive) will raise their hands. He then counts them to determine if the roll number of the absent student lies between these values.</p><p>Things seemed fine until his teaching assistant noticed something — the students are dishonest! Some students whose roll numbers lie in the given range may not raise their hands, while some other students whose roll number does not lie in the given range may raise their hands. But the students don't want to raise much suspicion. So, only the following $4$ cases are possible for a particular query $(l,r)$ — </p><ol> <li> True Positive: $r-l+1$ students are present and $r-l+1$ students raised their hands. </li><li> True Negative: $r-l$ students are present and $r-l$ students raised their hands. </li><li> False Positive: $r-l$ students are present but $r-l+1$ students raised their hands. </li><li> False Negative: $r-l+1$ students are present but $r-l$ students raised their hands. </li></ol><p>In the first two cases, the students are said to be answering honestly, while in the last two cases, the students are said to be answering dishonestly. The students can mutually decide upon their strategy, not known to Mr. 1048576. Also, the students do not want to raise any suspicion and at the same time, want to create a lot of confusion. So, their strategy always meets the following two conditions — </p><ol> <li> The students will never answer honestly $3$ times in a row. </li><li> The students will never answer dishonestly $3$ times in a row. </li></ol><p>Mr. 1048576 is frustrated by this act of students. So, he is willing to mark at most $2$ students as absent (though he knows that only one is). The attendance is said to be successful if the student who is actually absent is among those two. Also, due to limited class time, he can only ask up to $\lceil\log_{1.116}{n}\rceil-1$ queries (weird numbers but okay). Help him complete a successful attendance.</p></div><div><h2>Interaction</h2><p>First read a line containing a single integer $t$ ($1\leq t\leq 2048$) denoting the number of independent test cases that you must solve.</p><p>For each test case, first read a line containing a single integer $n$ ($3\leq n\leq 10^5$). Then you may ask up to $\lceil\log_{1.116}{n}\rceil-1$ queries.</p><p>To ask a query, print a single line in the format <span class="tex-font-style-tt">"? l r"</span> (without quotes) $(1\leq l\leq r\leq n)$. Then read a single line containing a single integer $x$ ($r-l\leq x\leq r-l+1$) denoting the number of students who raised their hands corresponding to the query.</p><p>To mark a student as absent, print a single line in the format <span class="tex-font-style-tt">"! a"</span> (without quotes) $(1\leq a\leq n)$. Then read a single integer $y$ ($y\in\{0,1\}$). If the student with roll number $a$ was absent, $y=1$, else, $y=0$. Note that this operation does not count as a query but you can do this operation at most $2$ times.</p><p>To end a test case, print a single line in the format <span class="tex-font-style-tt">"#"</span> (without quotes). Then you must continue solving the remaining test cases.</p><p>If you ask more queries than allowed or ask an invalid query, you will get the <span class="tex-font-style-tt">Wrong answer</span> verdict.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p><p>After printing the answers, do not forget to output end of line and flush the output buffer. Otherwise, you will get the verdict <span class="tex-font-style-tt">Idleness limit exceeded</span>. To flush the buffer, use:</p><ul> <li> <span class="tex-font-style-tt">fflush(stdout)</span> or <span class="tex-font-style-tt">cout.flush()</span> in C++; </li><li> <span class="tex-font-style-tt">System.out.flush()</span> in Java; </li><li> <span class="tex-font-style-tt">flush(output)</span> in Pascal; </li><li> <span class="tex-font-style-tt">stdout.flush()</span> in Python; </li><li> Read documentation for other languages. </li></ul><p>Note that the grader for this problem is adaptive meaning that the answer may change depending on your queries but will always remain consistent with the constraints and the answer to the previous queries.</p><p><span class="tex-font-style-bf"><span class="tex-font-style-section">Input format for Hacks</span></span></p><p>The test cases for this problem use both non-adaptive and adaptive graders. You can use the non-adaptive grader for making hacks.</p><p>The first line of input contains a single integer $t$ ($1\leq t\leq 2048$).</p><p>The first line of each test case contains three integers $g$, $n$ and $x$ where $g=1$ (to identify that this test case must use the non-adaptive grader), $n$ ($3\leq n\leq 10^5$) represents the number of students in the class and $x$ ($1\leq x\leq n$) represents the roll number of the student who is absent. You must ensure that the sum of $n$ over all test cases does not exceed $10^5$.</p><p>The second line of each test case contains a single string $S$ ($1\leq\vert S\vert\leq 120, S_i\in \{\texttt{T},\texttt{F}\}$). This string represents the pattern of the truth sequence. If $S_{(i-1)\bmod \vert S\vert+1}= \texttt{T}$, the students will act honestly during the $i$-th query, otherwise they will act dishonestly. You must also ensure that there is no index $i$ such that $S_{(i-1)\bmod \vert S\vert+1} = S_{i\bmod \vert S\vert+1} = S_{(i+1)\bmod \vert S\vert+1}$.</p></div>





```input1
2
5

3

2

1

2

0

1

0

2

0

1

6

6

2

2

0

1

1

0

0

0

1
```




```output1
? 1 4

? 3 5

? 2 2

? 1 3

? 3 3

? 3 3

! 3

? 2 4

? 4 4

! 2

#

? 1 6

? 1 3

? 4 6

? 1 1

? 3 3

? 5 5

! 3

? 2 2

? 4 4

! 4

#
```



## Note

<p>For the first test case, the student with roll number $2$ is absent and the truth sequence (see section for hacks) is <span class="tex-font-style-tt">TFFTFTTF</span>. During execution of your solution, this test case will use a non-adaptive grader.</p><p>For the second test case, the student with roll number $4$ is absent, and the truth sequence is <span class="tex-font-style-tt">FFTFTTFT</span>. During the execution of your solution, in this test case your program will interact with an adaptive grader. So, the actual answer might be different depending on your queries but will always remain consistent with the responses to the previous queries.</p>
