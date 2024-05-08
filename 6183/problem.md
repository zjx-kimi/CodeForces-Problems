## Description

<div><p>Vasya and Petya take part in a Codeforces round. The round lasts for two hours and contains five problems.</p><p>For this round the dynamic problem scoring is used. If you were lucky not to participate in any Codeforces round with dynamic problem scoring, here is what it means. The maximum point value of the problem depends on the ratio of the number of participants who solved the problem to the total number of round participants. Everyone who made at least one submission is considered to be participating in the round.</p><p><img align="middle" class="tex-formula" src="file://UdYNGE7e.png" style="max-width: 100.0%;max-height: 100.0%;"></p><p>Pay attention to the range bounds. For example, if 40 people are taking part in the round, and 10 of them solve a particular problem, then the solvers fraction is equal to <span class="tex-span">1 / 4</span>, and the problem's maximum point value is equal to 1500.</p><p>If the problem's maximum point value is equal to <span class="tex-span"><i>x</i></span>, then for each whole minute passed from the beginning of the contest to the moment of the participant's correct submission, the participant loses <span class="tex-span"><i>x</i> / 250</span> points. For example, if the problem's maximum point value is 2000, and the participant submits a correct solution to it 40 minutes into the round, this participant will be awarded with <span class="tex-span">2000·(1 - 40 / 250) = 1680</span> points for this problem.</p><p>There are <span class="tex-span"><i>n</i></span> participants in the round, including Vasya and Petya. For each participant and each problem, the number of minutes which passed between the beginning of the contest and the submission of this participant to this problem is known. It's also possible that this participant made no submissions to this problem.</p><p>With two seconds until the end of the round, all participants' submissions have passed pretests, and not a single hack attempt has been made. Vasya believes that no more submissions or hack attempts will be made in the remaining two seconds, and every submission will pass the system testing.</p><p>Unfortunately, Vasya is a cheater. He has registered <span class="tex-span">10<sup class="upper-index">9</sup> + 7</span> new accounts for the round. Now Vasya can submit any of his solutions from these new accounts in order to change the maximum point values of the problems. Vasya can also submit any wrong solutions to any problems. Note that Vasya can not submit correct solutions to the problems he hasn't solved.</p><p>Vasya seeks to score strictly more points than Petya in the current round. Vasya has already prepared the scripts which allow to obfuscate his solutions and submit them into the system from any of the new accounts in just fractions of seconds. However, Vasya doesn't want to make his cheating too obvious, so he wants to achieve his goal while making submissions from the smallest possible number of new accounts.</p><p>Find the smallest number of new accounts Vasya needs in order to beat Petya (provided that Vasya's assumptions are correct), or report that Vasya can't achieve his goal.</p></div><div class="input-specification"><p>The first line contains a single integer <span class="tex-span"><i>n</i></span> (<span class="tex-span">2 ≤ <i>n</i> ≤ 120</span>)&nbsp;— the number of round participants, including Vasya and Petya.</p><p>Each of the next <span class="tex-span"><i>n</i></span> lines contains five integers <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i>, 1</sub>, <i>a</i><sub class="lower-index"><i>i</i>, 2</sub>..., <i>a</i><sub class="lower-index"><i>i</i>, 5</sub></span> (<span class="tex-span"> - 1 ≤ <i>a</i><sub class="lower-index"><i>i</i>, <i>j</i></sub> ≤ 119</span>)&nbsp;— the number of minutes passed between the beginning of the round and the submission of problem <span class="tex-span"><i>j</i></span> by participant <span class="tex-span"><i>i</i></span>, or <span class="tex-font-style-tt">-1</span> if participant <span class="tex-span"><i>i</i></span> hasn't solved problem <span class="tex-span"><i>j</i></span>.</p><p>It is guaranteed that each participant has made at least one successful submission.</p><p>Vasya is listed as participant number 1, Petya is listed as participant number 2, all the other participants are listed in no particular order.</p></div><div class="output-specification"><p>Output a single integer&nbsp;— the number of new accounts Vasya needs to beat Petya, or <span class="tex-font-style-tt">-1</span> if Vasya can't achieve his goal.</p></div>

## Input

<p>The first line contains a single integer <span class="tex-span"><i>n</i></span> (<span class="tex-span">2 ≤ <i>n</i> ≤ 120</span>)&nbsp;— the number of round participants, including Vasya and Petya.</p><p>Each of the next <span class="tex-span"><i>n</i></span> lines contains five integers <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i>, 1</sub>, <i>a</i><sub class="lower-index"><i>i</i>, 2</sub>..., <i>a</i><sub class="lower-index"><i>i</i>, 5</sub></span> (<span class="tex-span"> - 1 ≤ <i>a</i><sub class="lower-index"><i>i</i>, <i>j</i></sub> ≤ 119</span>)&nbsp;— the number of minutes passed between the beginning of the round and the submission of problem <span class="tex-span"><i>j</i></span> by participant <span class="tex-span"><i>i</i></span>, or <span class="tex-font-style-tt">-1</span> if participant <span class="tex-span"><i>i</i></span> hasn't solved problem <span class="tex-span"><i>j</i></span>.</p><p>It is guaranteed that each participant has made at least one successful submission.</p><p>Vasya is listed as participant number 1, Petya is listed as participant number 2, all the other participants are listed in no particular order.</p>

## Output

<p>Output a single integer&nbsp;— the number of new accounts Vasya needs to beat Petya, or <span class="tex-font-style-tt">-1</span> if Vasya can't achieve his goal.</p>





```input1
2
5 15 40 70 115
50 45 40 30 15

```




```input2
3
55 80 10 -1 -1
15 -1 79 60 -1
42 -1 13 -1 -1

```




```input3
5
119 119 119 119 119
0 0 0 0 -1
20 65 12 73 77
78 112 22 23 11
1 78 60 111 62

```




```input4
4
-1 20 40 77 119
30 10 73 50 107
21 29 -1 64 98
117 65 -1 -1 -1

```




```output1
2

```




```output2
3

```




```output3
27

```




```output4
-1

```



## Note

<p>In the first example, Vasya's optimal strategy is to submit the solutions to the last three problems from two new accounts. In this case the first two problems will have the maximum point value of 1000, while the last three problems will have the maximum point value of 500. Vasya's score will be equal to <span class="tex-span">980 + 940 + 420 + 360 + 270 = 2970</span> points, while Petya will score just <span class="tex-span">800 + 820 + 420 + 440 + 470 = 2950</span> points.</p><p>In the second example, Vasya has to make a single unsuccessful submission to any problem from two new accounts, and a single successful submission to the first problem from the third new account. In this case, the maximum point values of the problems will be equal to 500, 1500, 1000, 1500, 3000. Vasya will score 2370 points, while Petya will score just 2294 points.</p><p>In the third example, Vasya can achieve his goal by submitting the solutions to the first four problems from 27 new accounts. The maximum point values of the problems will be equal to 500, 500, 500, 500, 2000. Thanks to the high cost of the fifth problem, Vasya will manage to beat Petya who solved the first four problems very quickly, but couldn't solve the fifth one.</p>
