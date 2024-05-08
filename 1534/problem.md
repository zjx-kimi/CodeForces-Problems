## Description

<div><p>Hosssam decided to sneak into Hemose's room while he is sleeping and change his laptop's password. He already knows the password, which is a string $s$ of length $n$. He also knows that there are $k$ <span class="tex-font-style-it">special</span> letters of the alphabet: $c_1,c_2,\ldots, c_k$.</p><p>Hosssam made a program that can do the following.</p><ol> <li> The program considers the current password $s$ of some length $m$. </li><li> Then it finds all positions $i$ ($1\le i&lt;m$) such that $s_{i+1}$ is one of the $k$ special letters. </li><li> Then it deletes all of those positions from the password $s$ <span class="tex-font-style-bf">even if $s_{i}$ is a special character</span>. If there are no positions to delete, then the program displays an error message which has a very loud sound. </li></ol><p>For example, suppose the string $s$ is "<span class="tex-font-style-tt">abcdef</span>" and the special characters are '<span class="tex-font-style-tt">b</span>' and '<span class="tex-font-style-tt">d</span>'. If he runs the program once, the positions $1$ and $3$ will be deleted as they come before special characters, so the password becomes "<span class="tex-font-style-tt">bdef</span>". If he runs the program again, it deletes position $1$, and the password becomes "<span class="tex-font-style-tt">def</span>". If he is wise, he won't run it a third time.</p><p>Hosssam wants to know how many times he can run the program on Hemose's laptop without waking him up from the sound of the error message. Can you help him?</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^5$) — the number of test cases. Then $t$ test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 10^5$) — the initial length of the password.</p><p>The next line contains a string $s$ consisting of $n$ lowercase English letters — the initial password.</p><p>The next line contains an integer $k$ ($1 \le k \le 26$), followed by $k$ distinct lowercase letters $c_1,c_2,\ldots,c_k$ — the special letters.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print the maximum number of times Hosssam can run the program without displaying the error message, on a new line.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^5$) — the number of test cases. Then $t$ test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 10^5$) — the initial length of the password.</p><p>The next line contains a string $s$ consisting of $n$ lowercase English letters — the initial password.</p><p>The next line contains an integer $k$ ($1 \le k \le 26$), followed by $k$ distinct lowercase letters $c_1,c_2,\ldots,c_k$ — the special letters.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p>

## Output

<p>For each test case, print the maximum number of times Hosssam can run the program without displaying the error message, on a new line.</p>





```input1|2,3,4,8,9,10,14,15,16,20,21,22,26,27,28
10
9
iloveslim
1 s
7
joobeel
2 o e
7
basiozi
2 s i
6
khater
1 r
7
abobeih
6 a b e h i o
5
zondl
5 a b c e f
6
shoman
2 a h
7
shetwey
2 h y
5
samez
1 m
6
mouraz
1 m
```




```output1
5
2
3
5
1
0
3
5
2
0
```



## Note

<p>In the first test case, the program can run $5$ times as follows: $\text{iloveslim} \to \text{ilovslim} \to \text{iloslim} \to \text{ilslim} \to \text{islim} \to \text{slim}$</p><p>In the second test case, the program can run $2$ times as follows: $\text{joobeel} \to \text{oel} \to \text{el}$</p><p>In the third test case, the program can run $3$ times as follows: $\text{basiozi} \to \text{bioi} \to \text{ii} \to \text{i}$.</p><p>In the fourth test case, the program can run $5$ times as follows: $\text{khater} \to \text{khatr} \to \text{khar} \to \text{khr} \to \text{kr} \to \text{r}$</p><p>In the fifth test case, the program can run only once as follows: $\text{abobeih} \to \text{h}$</p><p>In the sixth test case, the program cannot run as none of the characters in the password is a special character.</p>
