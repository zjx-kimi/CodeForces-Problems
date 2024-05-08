## Description

<div><p>In the end of the day, Anna needs to turn off the lights in the office. There are $n$ lights and $n$ light switches, but their operation scheme is really strange. The switch $i$ changes the state of light $i$, but it also changes the state of some other light $a_i$ (change the state means that if the light was on, it goes off and vice versa).</p><p>Help Anna to turn all the lights off using minimal number of switches, or say it is impossible.</p></div><div class="input-specification"><p>The first line of input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Descriptions of test cases follow.</p><p>The first line of each test case contains the integer $n$ ($2 \le n \le 10^5$)&nbsp;— the number of lights. </p><p>The second line of each test case contains the string of $n$ characters, the initial state of the lights. Character "<span class="tex-font-style-tt">0</span>" means that the corresponding light is off, and "<span class="tex-font-style-tt">1</span>" means that it is on. </p><p>The third line of each test case contains $n$ integers $a_i$ ($1 \le a_i \le n$, $a_i \neq i$)&nbsp;— the switch $i$ changes the states of light $i$ and light $a_i$.</p><p>It is guaranteed that sum of $n$ over all test cases does not exceed $2 \cdot 10^5$</p></div><div class="output-specification"><p>For each test case output the integer $k$, the minimal number of switches to use, then in the separate line output the list of $k$ switches.</p><p>If it is impossible to turn off all the lights, output single integer $-1$.</p></div>

## Input

<p>The first line of input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Descriptions of test cases follow.</p><p>The first line of each test case contains the integer $n$ ($2 \le n \le 10^5$)&nbsp;— the number of lights. </p><p>The second line of each test case contains the string of $n$ characters, the initial state of the lights. Character "<span class="tex-font-style-tt">0</span>" means that the corresponding light is off, and "<span class="tex-font-style-tt">1</span>" means that it is on. </p><p>The third line of each test case contains $n$ integers $a_i$ ($1 \le a_i \le n$, $a_i \neq i$)&nbsp;— the switch $i$ changes the states of light $i$ and light $a_i$.</p><p>It is guaranteed that sum of $n$ over all test cases does not exceed $2 \cdot 10^5$</p>

## Output

<p>For each test case output the integer $k$, the minimal number of switches to use, then in the separate line output the list of $k$ switches.</p><p>If it is impossible to turn off all the lights, output single integer $-1$.</p>





```input1|2,3,4,8,9,10,14,15,16,20,21,22
8
5
11101
4 3 4 2 2
2
10
2 1
10
0000000011
9 10 10 7 10 9 9 9 10 2
10
1000111101
9 3 8 9 2 1 3 7 2 7
10
0001101010
5 7 6 10 8 3 6 6 2 2
10
0101100010
8 7 7 9 9 4 1 4 2 7
10
1010111010
7 9 10 7 7 2 8 6 10 4
10
1110000001
3 10 10 1 10 8 6 3 2 1
```




```output1
3
1 5 3 
-1
1
9 
5
5 6 10 2 3 
6
4 9 5 10 8 7 
3
5 4 9 
6
1 3 5 9 7 8 
2
2 1
```


