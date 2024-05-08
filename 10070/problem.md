## Description

<div><p><span class="tex-font-style-bf">This is the hard version of the problem. The only difference between the two versions is the constraint on $t$, $m$ and the sum of $m$. You can make hacks only if both versions of the problem are solved.</span></p><p>Alice and Bob play yet another game on an array $a$ of size $n$. Alice starts with an empty array $c$. Both players take turns playing, with Alice starting first.</p><p>On Alice's turn, she picks one element from $a$, appends that element to $c$, and then deletes it from $a$.</p><p>On Bob's turn, he picks at most $k$ elements from $a$, and then deletes it from $a$. </p><p>The game ends when the array $a$ is empty. Alice's score is defined to be the MEX$^\dagger$ of $c$. Alice wants to maximize her score while Bob wants to minimize it. Find Alice's final score if both players play optimally.</p><p>The array will be given in compressed format. Instead of giving the elements present in the array, we will be giving their frequencies. Formally, you will be given $m$, the maximum element in the array, and then $m + 1$ integers $f_0, f_1, \ldots, f_{m}$, where $f_i$ represents the number of times $i$ occurs in the array $a$.</p><p>$^\dagger$ The $\operatorname{MEX}$ (minimum excludant) of an array of integers is defined as the smallest non-negative integer which does not occur in the array. For example: </p><ul> <li> The MEX of $[2,2,1]$ is $0$, because $0$ does not belong to the array. </li><li> The MEX of $[3,1,0,1]$ is $2$, because $0$ and $1$ belong to the array, but $2$ does not. </li><li> The MEX of $[0,3,1,2]$ is $4$, because $0$, $1$, $2$ and $3$ belong to the array, but $4$ does not. </li></ul> </div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^5$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $m$ and $k$ ($1 \le m \le 2 \cdot 10^5, 1 \le k \le 10^9$).</p><p>The second line contains $m + 1$ integers $f_0, f_1, \ldots, f_m$ ($1 \le f_i \le 10^9$).</p><p>It is guaranteed the sum of $m$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, find Alice's score if both players play optimally.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^5$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $m$ and $k$ ($1 \le m \le 2 \cdot 10^5, 1 \le k \le 10^9$).</p><p>The second line contains $m + 1$ integers $f_0, f_1, \ldots, f_m$ ($1 \le f_i \le 10^9$).</p><p>It is guaranteed the sum of $m$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, find Alice's score if both players play optimally.</p>





```input1|2,3,6,7,10,11
5
1 4
4 5
2 1000000000
1000000000 1000000000 1000000000
3 2
2 3 100 1
1 1
2 2
3 1
1 1 1 1
```




```output1
2
1
3
2
1
```



## Note

<p>In the first test case, the array $a$ is $[0, 0, 0, 0, 1, 1, 1, 1, 1]$. A possible game with a score of $2$ is as follows: </p><ol> <li> Alice chooses the element $0$. After this move, $a = [0, 0, 0, 1, 1, 1, 1, 1]$ and $c=[0]$. </li><li> Bob chooses to remove the $3$ elements $0$, $0$ and $1$. After this move, $a = [0, 1, 1, 1, 1]$ and $c=[0]$. </li><li> Alice chooses the element $1$. After this move, $a = [0,1,1,1]$ and $c=[0,1]$. </li><li> Bob removes the $4$ remaining elements $0$, $1$, $1$ and $1$. After this move, $a=[\,]$ and $c=[0,1]$. </li></ol><p>At the end, $c=[0,1]$ which has a MEX of $2$. Note that this is an example game and does not necessarily represent the optimal strategy for both players.</p><p>In the second test case, Alice can choose a $0$ in her first turn, guaranteeing that her score is at least $1$. While Bob can remove all copies element $1$ in his first turn, thus guaranteeing that Alice's score cannot exceed $1$. So Alice's score is $1$ if both players play optimally.</p>
