## Description

<div><p>Vlad decided to go on a trip to the mountains. He plans to move between $n$ mountains, some of which are connected by roads. The $i$-th mountain has a height of $h_i$.</p><p>If there is a road between mountains $i$ and $j$, Vlad can move from mountain $i$ to mountain $j$ by spending $h_j - h_i$ units of energy. If his energy drops below zero during the transition, he will not be able to move from mountain $i$ to mountain $j$. Note that $h_j - h_i$ can be negative and then the energy will be restored.</p><p>Vlad wants to consider different route options, so he asks you to answer the following queries: is it possible to construct some route starting at mountain $a$ and ending at mountain $b$, given that he initially has $e$ units of energy?</p></div><div class="input-specification"><p>The first line of the input contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The descriptions of the test cases follow.</p><p>The first line of each test case contains two numbers $n$ and $m$ ($2 \le n \le 2 \cdot 10^5$, $1 \le m \le \min(\frac{n\cdot(n - 1)}{2}, 2 \cdot 10^5)$)&nbsp;— the number of mountains and the number of roads between them, respectively.</p><p>The second line contains $n$ integers $h_1, h_2, h_3, \dots, h_n$ ($1 \le h_i \le 10^9$)&nbsp;— the heights of the mountains.</p><p>The next $m$ lines contain two integers $u$ and $v$ ($1 \le u, v \le n$, $u \ne v$)&nbsp;— the numbers of the mountains connected by a road. It is guaranteed that no road appears twice.</p><p>The next line contains an integer $q$ ($1 \le q \le 2 \cdot 10^5$)&nbsp;— the number of queries.</p><p>The following $q$ lines contain three numbers $a$, $b$, and $e$ ($1 \le a, b \le n$, $0 \le e \le 10^9$)&nbsp;— the initial and final mountains of the route, and the amount of energy, respectively.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$. The same guarantee applies to $m$ and $q$.</p></div><div class="output-specification"><p>For each query, output "<span class="tex-font-style-tt">YES</span>" if Vlad can construct a route from mountain $a$ to mountain $b$, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p><p>In the examples below, the answers for different test cases are separated by an empty line, which you do not need to output.</p></div>

## Input

<p>The first line of the input contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The descriptions of the test cases follow.</p><p>The first line of each test case contains two numbers $n$ and $m$ ($2 \le n \le 2 \cdot 10^5$, $1 \le m \le \min(\frac{n\cdot(n - 1)}{2}, 2 \cdot 10^5)$)&nbsp;— the number of mountains and the number of roads between them, respectively.</p><p>The second line contains $n$ integers $h_1, h_2, h_3, \dots, h_n$ ($1 \le h_i \le 10^9$)&nbsp;— the heights of the mountains.</p><p>The next $m$ lines contain two integers $u$ and $v$ ($1 \le u, v \le n$, $u \ne v$)&nbsp;— the numbers of the mountains connected by a road. It is guaranteed that no road appears twice.</p><p>The next line contains an integer $q$ ($1 \le q \le 2 \cdot 10^5$)&nbsp;— the number of queries.</p><p>The following $q$ lines contain three numbers $a$, $b$, and $e$ ($1 \le a, b \le n$, $0 \le e \le 10^9$)&nbsp;— the initial and final mountains of the route, and the amount of energy, respectively.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$. The same guarantee applies to $m$ and $q$.</p>

## Output

<p>For each query, output "<span class="tex-font-style-tt">YES</span>" if Vlad can construct a route from mountain $a$ to mountain $b$, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p><p>In the examples below, the answers for different test cases are separated by an empty line, which you do not need to output.</p>





```input1|2,3,4,5,6,7,8,9,10,11,12,13,14,15,16
2
7 7
1 5 3 4 2 4 1
1 4
4 3
3 6
3 2
2 5
5 6
5 7
5
1 1 3
6 2 0
4 7 0
1 7 4
1 7 2
6 5
4 7 6 2 5 1
1 3
5 3
1 5
2 4
6 2
5
1 5 1
1 3 1
1 2 1000
6 2 6
6 2 5
```




```input2|2,3,4,5,6,7,8,9,10,11
2
3 2
1 3 9
1 2
2 3
5
1 1 1
3 2 2
1 1 2
3 3 0
1 2 1
3 3
1 4 1
1 2
2 3
1 3
5
3 3 9
1 3 6
1 1 2
3 3 6
3 3 4
```




```input3|2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19
1
6 10
7 9 2 10 8 6
4 2
6 1
4 5
3 5
6 4
1 3
2 6
6 5
1 2
3 6
5
4 4 8
3 3 1
5 5 9
2 1 7
6 6 10
```




```output1
YES
NO
YES
YES
NO

YES
NO
NO
YES
NO
```




```output2
YES
YES
YES
YES
NO

YES
YES
YES
YES
YES
```




```output3
YES
YES
YES
YES
YES
```


