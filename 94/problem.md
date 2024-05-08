## Description

<div><p>Monocarp is playing a computer game. In order to level up his character, he can complete quests. There are $n$ quests in the game, numbered from $1$ to $n$.</p><p>Monocarp can complete quests according to the following rules: </p><ul> <li> the $1$-st quest is always available for completion; </li><li> the $i$-th quest is available for completion if all quests $j &lt; i$ have been completed at least once. </li></ul><p>Note that Monocarp can complete the same quest multiple times.</p><p>For each completion, the character gets some amount of experience points: </p><ul> <li> for the first completion of the $i$-th quest, he gets $a_i$ experience points; </li><li> for each subsequent completion of the $i$-th quest, he gets $b_i$ experience points. </li></ul><p>Monocarp is a very busy person, so he has free time to complete no more than $k$ quests. Your task is to calculate the maximum possible total experience Monocarp can get if he can complete no more than $k$ quests.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le n \le 2 \cdot 10^5$; $1 \le k \le 2 \cdot 10^5$)&nbsp;— the number of quests and the maximum number of quests Monocarp can complete, respectively.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^3$).</p><p>The third line contains $n$ integers $b_1, b_2, \dots, b_n$ ($1 \le b_i \le 10^3$).</p><p>Additional constraint on the input: the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print a single integer&nbsp;— the maximum possible total experience Monocarp can get if he can complete no more than $k$ quests.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le n \le 2 \cdot 10^5$; $1 \le k \le 2 \cdot 10^5$)&nbsp;— the number of quests and the maximum number of quests Monocarp can complete, respectively.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^3$).</p><p>The third line contains $n$ integers $b_1, b_2, \dots, b_n$ ($1 \le b_i \le 10^3$).</p><p>Additional constraint on the input: the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, print a single integer&nbsp;— the maximum possible total experience Monocarp can get if he can complete no more than $k$ quests.</p>





```input1|2,3,4,8,9,10
4
4 7
4 3 1 2
1 1 1 1
3 2
1 2 5
3 1 8
5 5
3 2 4 1 4
2 3 1 4 7
6 4
1 4 5 4 5 10
1 5 1 2 5 1
```




```output1
13
4
15
15
```



## Note

<p>In the first test case, one of the possible quest completion sequences is as follows: $1, 1, 2, 3, 2, 4, 4$; its total experience is equal to $\underline{4} + 1 + \underline{3} + \underline{1} + 1 + \underline{2} + 1 = 13$ (the underlined numbers correspond to the instances when we complete a quest for the first time).</p><p>In the second test case, one of the possible quest completion sequences is as follows: $1, 1$; its total experience is equal to $\underline{1} + 3 = 4$.</p><p>In the third test case, one of the possible quest completion sequences is as follows: $1, 2, 2, 2, 3$; its total experience is equal to $\underline{3} + \underline{2} + 3 + 3 + \underline{4} = 15$.</p>
