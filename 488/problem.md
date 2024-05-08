## Description

<div><p>Rudolf has registered for a programming competition that will follow the rules of ICPC. The rules imply that for each solved problem, a participant gets $1$ point, and also incurs a penalty equal to the number of minutes passed from the beginning of the competition to the moment of solving the problem. In the final table, the participant with the most points is ranked higher, and in case of a tie in points, the participant with the lower penalty is ranked higher.</p><p>In total, $n$ participants have registered for the competition. Rudolf is a participant with index $1$. It is known that $m$ problems will be proposed. And the competition will last $h$ minutes.</p><p>A powerful artificial intelligence has predicted the values $t_{i, j}$, which represent the number of minutes it will take for the $i$-th participant to solve the $j$-th problem.</p><p>Rudolf realized that the order of solving problems will affect the final result. For example, if $h = 120$, and the times to solve problems are [$20, 15, 110$], then if Rudolf solves the problems in the order:</p><ul> <li> ${3, 1, 2}$, then he will only solve the third problem and get $1$ point and $110$ penalty. </li><li> ${1, 2, 3}$, then he will solve the first problem after $20$ minutes from the start, the second one after $20+15=35$ minutes, and he will not have time to solve the third one. Thus, he will get $2$ points and $20+35=55$ penalty. </li><li> ${2, 1, 3}$, then he will solve the second problem after $15$ minutes from the start, the first one after $15+20=35$ minutes, and he will not have time to solve the third one. Thus, he will get $2$ points and $15+35=50$ penalty. </li></ul><p>Rudolf became interested in what place he will take in the competition if each participant solves problems in the optimal order based on the predictions of the artificial intelligence. It will be assumed that in case of a tie in points and penalty, Rudolf will take the best place.</p></div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \le t \le 10^3$) — the number of test cases.</p><p>Then follow the descriptions of the test cases.</p><p>The first line of each test case contains three integers $n, m, h$ ($1 \le n \cdot m \le 2 \cdot 10^5, 1 \le h \le 10^6$) — the number of participants, the number of problems, and the duration of the competition, respectively.</p><p>Then there are $n$ lines, each containing $m$ integers $t_{i, j}$ ($1 \le t_{i, j} \le 10^6$) — the number of minutes it will take for the $i$-th participant to solve the $j$-th problem.</p><p>The sum of $n \cdot m$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output an integer — Rudolf's place in the final table if all participants solve problems in the optimal order.</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \le t \le 10^3$) — the number of test cases.</p><p>Then follow the descriptions of the test cases.</p><p>The first line of each test case contains three integers $n, m, h$ ($1 \le n \cdot m \le 2 \cdot 10^5, 1 \le h \le 10^6$) — the number of participants, the number of problems, and the duration of the competition, respectively.</p><p>Then there are $n$ lines, each containing $m$ integers $t_{i, j}$ ($1 \le t_{i, j} \le 10^6$) — the number of minutes it will take for the $i$-th participant to solve the $j$-th problem.</p><p>The sum of $n \cdot m$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output an integer — Rudolf's place in the final table if all participants solve problems in the optimal order.</p>





```input1|2,3,4,5,9,10,15,16,17,18
5
3 3 120
20 15 110
90 90 100
40 40 40
2 1 120
30
30
1 3 120
10 20 30
3 2 27
8 9
10 7
10 8
3 3 15
7 2 6
7 5 4
1 9 8
```




```output1
2
1
1
2
1
```



## Note

<p>In the first example, Rudolf will get $2$ points and $50$ penalty minutes. The second participant will solve only one problem and get $1$ point and $90$ penalty minutes. And the third participant will solve all $3$ problems and get $3$ points and $240$ penalty minutes. Thus, Rudolf will take the second place.</p><p>In the second example, both participants will get $1$ point and $30$ penalty minutes. In case of a tie in points, Rudolf gets the better position, so he will take the first place.</p><p>In the third example, Rudolf is the only participant, so he will take the first place.</p><p>In the fourth example, all participants can solve two problems with penalty of $25 = 8 + (8 + 9)$, $24 = 7 + (7 + 10)$ and $26 = 8 + (8 + 10)$, respectively, thanks to the penalty, the second participant gets the first place, and Rudolf gets the second.</p>
