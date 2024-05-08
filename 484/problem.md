## Description

<div><p>A new virus called "CodeVid-23" has spread among programmers. Rudolf, being a programmer, was not able to avoid it.</p><p>There are $n$ symptoms numbered from $1$ to $n$ that can appear when infected. Initially, Rudolf has some of them. He went to the pharmacy and bought $m$ medicines.</p><p>For each medicine, the number of days it needs to be taken is known, and the set of symptoms it removes. Unfortunately, medicines often have side effects. Therefore, for each medicine, the set of symptoms that appear when taking it is also known.</p><p>After reading the instructions, Rudolf realized that taking more than one medicine at a time is very unhealthy.</p><p>Rudolph wants to be healed as soon as possible. Therefore, he asks you to calculate the minimum number of days to remove all symptoms, or to say that it is impossible.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ $(1 \le t \le 100)$ — the number of test cases.</p><p>Then follow the descriptions of the test cases.</p><p>The first line of each test case contains two integers $n, m$ $(1 \le n \le 10, 1 \le m \le 10^3)$ — the number of symptoms and medicines, respectively.</p><p>The second line of each test case contains a string of length $n$ consisting of the characters $0$ and $1$ — the description of Rudolf's symptoms. If the $i$-th character of the string is $1$, Rudolf has the $i$-th symptom, otherwise he does not.</p><p>Then follow $3 \cdot m$ lines — the description of the medicines.</p><p>The first line of each medicine description contains an integer $d$ $(1 \le d \le 10^3)$ — the number of days the medicine needs to be taken.</p><p>The next two lines of the medicine description contain two strings of length $n$, consisting of the characters $0$ and $1$ — the description of the symptoms it removes and the description of the side effects.</p><p>In the first of the two lines, $1$ at position $i$ means that the medicine removes the $i$-th symptom, and $0$ otherwise.</p><p>In the second of the two lines, $1$ at position $i$ means that the $i$-th symptom appears after taking the medicine, and $0$ otherwise.</p><p>Different medicines can have the same sets of symptoms and side effects. If a medicine relieves a certain symptom, it will not be among the side effects.</p><p>The sum of $m$ over all test cases does not exceed $10^3$.</p></div><div class="output-specification"><p>For each test case, output a single integer on a separate line — the minimum number of days it will take Rudolf to remove all symptoms. If this never happens, output $-1$.</p></div>

## Input

<p>The first line contains a single integer $t$ $(1 \le t \le 100)$ — the number of test cases.</p><p>Then follow the descriptions of the test cases.</p><p>The first line of each test case contains two integers $n, m$ $(1 \le n \le 10, 1 \le m \le 10^3)$ — the number of symptoms and medicines, respectively.</p><p>The second line of each test case contains a string of length $n$ consisting of the characters $0$ and $1$ — the description of Rudolf's symptoms. If the $i$-th character of the string is $1$, Rudolf has the $i$-th symptom, otherwise he does not.</p><p>Then follow $3 \cdot m$ lines — the description of the medicines.</p><p>The first line of each medicine description contains an integer $d$ $(1 \le d \le 10^3)$ — the number of days the medicine needs to be taken.</p><p>The next two lines of the medicine description contain two strings of length $n$, consisting of the characters $0$ and $1$ — the description of the symptoms it removes and the description of the side effects.</p><p>In the first of the two lines, $1$ at position $i$ means that the medicine removes the $i$-th symptom, and $0$ otherwise.</p><p>In the second of the two lines, $1$ at position $i$ means that the $i$-th symptom appears after taking the medicine, and $0$ otherwise.</p><p>Different medicines can have the same sets of symptoms and side effects. If a medicine relieves a certain symptom, it will not be among the side effects.</p><p>The sum of $m$ over all test cases does not exceed $10^3$.</p>

## Output

<p>For each test case, output a single integer on a separate line — the minimum number of days it will take Rudolf to remove all symptoms. If this never happens, output $-1$.</p>





```input1|2,3,4,5,6,7,8,9,10,11,12,13,14,15,21,22,23,24,25,26,27,28
4
5 4
10011
3
10000
00110
3
00101
00000
3
01010
00100
5
11010
00100
4 1
0000
10
1011
0100
2 2
11
2
10
01
3
01
10
2 3
11
3
01
10
3
10
00
4
10
01
```




```output1
8
0
-1
6
```



## Note

<p>In the first example, we can first apply medicine number $4$, after which the symptoms will look like "00101". After that, medicine number $2$, then all symptoms will disappear, and the number of days will be $5 + 3 = 8$. Another option is to apply the medicines in the order $1, 3, 2$. In this case, all symptoms will also disappear, but the number of days will be $3 + 3 + 3 = 9$.</p><p>In the second example, there are no symptoms initially, so the treatment will take $0$ days.</p><p>In the third example, there are no options to remove all symptoms.</p>
