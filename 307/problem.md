## Description

<div><p>Monocarp organizes a weightlifting competition. There are $n$ athletes participating in the competition, the $i$-th athlete has strength $s_i$ and endurance $e_i$. The $1$-st athlete is Monocarp's friend Polycarp, and Monocarp really wants Polycarp to win.</p><p>The competition will be conducted as follows. The jury will choose a positive <span class="tex-font-style-bf">(greater than zero)</span> integer $w$, which denotes the weight of the barbell that will be used in the competition. The goal for each athlete is to lift the barbell as many times as possible. The athlete who lifts the barbell the most amount of times will be declared the winner <span class="tex-font-style-bf">(if there are multiple such athletes — there's no winner)</span>.</p><p>If the barbell's weight $w$ is <span class="tex-font-style-bf">strictly greater</span> than the strength of the $i$-th athlete $s_i$, then the $i$-th athlete will be unable to lift the barbell even one single time. Otherwise, the $i$-th athlete will be able to lift the barbell, and the number of times he does it will be equal to his endurance $e_i$.</p><p>For example, suppose there are $4$ athletes with parameters $s_1 = 7, e_1 = 4$; $s_2 = 9, e_2 = 3$; $s_3 = 4, e_3 = 6$; $s_4 = 2, e_4 = 2$. If the weight of the barbell is $5$, then:</p><ul> <li> the first athlete will be able to lift the barbell $4$ times; </li><li> the second athlete will be able to lift the barbell $3$ times; </li><li> the third athlete will be unable to lift the barbell; </li><li> the fourth athlete will be unable to lift the barbell. </li></ul><p>Monocarp wants to choose $w$ in such a way that Polycarp (the $1$-st athlete) wins the competition. Help him to choose the value of $w$, or report that it is impossible.</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 100$) — the number of test cases.</p><p>The first line of each test case contains one integer $n$ ($2 \le n \le 100$) — the number of athletes. Then $n$ lines follow, the $i$-th of them contains two integers $s_i$ and $e_i$ ($1 \le s_i \le 10^9$; $1 \le e_i \le 100$) — the strength and the endurance of the $i$-th athlete.</p></div><div class="output-specification"><p>For each test case, print the answer as follows:</p><ul> <li> if the answer exists, print one integer — the value of $w$ meeting the constraints. The integer you print should satisfy $1 \le w \le 10^9$. It can be shown that if the answer exists, at least one such value of $w$ exists as well. If there are multiple answers, you can print any of them; </li><li> otherwise, print one integer $-1$. </li></ul></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 100$) — the number of test cases.</p><p>The first line of each test case contains one integer $n$ ($2 \le n \le 100$) — the number of athletes. Then $n$ lines follow, the $i$-th of them contains two integers $s_i$ and $e_i$ ($1 \le s_i \le 10^9$; $1 \le e_i \le 100$) — the strength and the endurance of the $i$-th athlete.</p>

## Output

<p>For each test case, print the answer as follows:</p><ul> <li> if the answer exists, print one integer — the value of $w$ meeting the constraints. The integer you print should satisfy $1 \le w \le 10^9$. It can be shown that if the answer exists, at least one such value of $w$ exists as well. If there are multiple answers, you can print any of them; </li><li> otherwise, print one integer $-1$. </li></ul>





```input1|2,3,4,5,6,10,11,12
3
4
7 4
9 3
4 6
2 2
2
4 6
100 100
2
1337 3
1337 3
```




```output1
5
-1
-1
```



## Note

<p>The first test case of the example is described in the statement.</p>
