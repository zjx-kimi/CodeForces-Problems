## Description

<div><p>One day, Vlad became curious about who he can have a conversation with on the escalator in the subway. There are a total of $n$ passengers. The escalator has a total of $m$ steps, all steps indexed from $1$ to $m$ and $i$-th step has height $i \cdot k$.</p><p>Vlad's height is $H$ centimeters. Two people with heights $a$ and $b$ can have a conversation on the escalator if they are standing on <span class="tex-font-style-bf">different</span> steps and the height difference between them is equal to the height difference between the steps.</p><p>For example, if two people have heights $170$ and $180$ centimeters, and $m = 10, k = 5$, then they can stand on steps numbered $7$ and $5$, where the height difference between the steps is equal to the height difference between the two people: $k \cdot 2 = 5 \cdot 2 = 10 = 180 - 170$. There are other possible ways.</p><p>Given an array $h$ of size $n$, where $h_i$ represents the height of the $i$-th person. Vlad is interested in how many people he can have a conversation with on the escalator <span class="tex-font-style-bf">individually</span>.</p><p>For example, if $n = 5, m = 3, k = 3, H = 11$, and $h = [5, 4, 14, 18, 2]$, Vlad can have a conversation with the person with height $5$ (Vlad will stand on step $1$, and the other person will stand on step $3$) and with the person with height $14$ (for example, Vlad can stand on step $3$, and the other person will stand on step $2$). Vlad cannot have a conversation with the person with height $2$ because even if they stand on the extreme steps of the escalator, the height difference between them will be $6$, while their height difference is $9$. Vlad cannot have a conversation with the rest of the people on the escalator, so the answer for this example is $2$.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>Then the descriptions of the test cases follow.</p><p>The first line of each test case contains integers: $n, m, k, H$ ($1 \le n,m \le 50$, $1 \le k,H \le 10^6$). Here, $n$ is the number of people, $m$ is the number of steps, $k$ is the height difference between neighboring steps, and $H$ is Vlad's height.</p><p>The second line contains $n$ integers: $h_1, h_2, \ldots, h_n$ ($1 \le h_i \le 10^6$). Here, $h_i$ represents the height of the $i$-th person.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the number of people Vlad can have a conversation with on the escalator <span class="tex-font-style-bf">individually</span>.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>Then the descriptions of the test cases follow.</p><p>The first line of each test case contains integers: $n, m, k, H$ ($1 \le n,m \le 50$, $1 \le k,H \le 10^6$). Here, $n$ is the number of people, $m$ is the number of steps, $k$ is the height difference between neighboring steps, and $H$ is Vlad's height.</p><p>The second line contains $n$ integers: $h_1, h_2, \ldots, h_n$ ($1 \le h_i \le 10^6$). Here, $h_i$ represents the height of the $i$-th person.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the number of people Vlad can have a conversation with on the escalator <span class="tex-font-style-bf">individually</span>.</p>





```input1|2,3,6,7,10,11,14,15
7
5 3 3 11
5 4 14 18 2
2 9 5 6
11 9
10 50 3 11
43 44 74 98 62 60 99 4 11 73
4 8 8 49
68 58 82 73
7 1 4 66
18 66 39 83 48 99 79
9 1 1 13
26 23 84 6 60 87 40 41 25
6 13 3 28
30 70 85 13 1 55
```




```output1
2
1
4
1
0
0
3
```



## Note

<p>The first example is explained in the problem statement.</p><p>In the second example, Vlad can have a conversation with the person with height $11$.</p><p>In the third example, Vlad can have a conversation with people with heights: $44, 74, 98, 62$. Therefore, the answer is $4$.</p><p>In the fourth example, Vlad can have a conversation with the person with height $73$.</p>
