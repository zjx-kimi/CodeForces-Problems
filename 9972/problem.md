## Description

<div><p>You have a one-dimensional puzzle, all the elements of which need to be put in one row, connecting with each other. All the puzzle elements are completely white and distinguishable from each other only if they have different shapes. </p><p>Each element has straight borders at the top and bottom, and on the left and right it has connections, each of which can be a protrusion or a recess. You <span class="tex-font-style-bf">cannot</span> rotate the elements.</p><p>You can see that there are exactly $4$ types of elements. Two elements can be connected if the right connection of the left element is opposite to the left connection of the right element.</p><center> <img class="tex-graphics" src="file://rAwLOS5I.png" style="max-width: 100.0%;max-height: 100.0%;"> All possible types of elements. </center><p>The puzzle contains $c_1, c_2, c_3, c_4$ elements of each type. The puzzle is considered complete if you have managed to combine <span class="tex-font-style-bf">all</span> elements into one long chain. You want to know how many ways this can be done.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 2 \cdot 10^5$) — the number of input test cases. The descriptions of the test cases follow.</p><p>The description of each test case contains $4$ integers $c_i$ ($0 \le c_i \le 10^6$) — the number of elements of each type, respectively.</p><p>It is guaranteed that the sum of $c_i$ for all test cases does not exceed $4 \cdot 10^6$.</p></div><div class="output-specification"><p>For each test case, print one integer — the number of possible ways to solve the puzzle. </p><p>Two methods are considered different if there is $i$, such that the types of elements at the $i$ position in these methods differ.</p><p>Since the answer can be very large, output it modulo $998244353$.</p><p>If it is impossible to solve the puzzle, print $0$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 2 \cdot 10^5$) — the number of input test cases. The descriptions of the test cases follow.</p><p>The description of each test case contains $4$ integers $c_i$ ($0 \le c_i \le 10^6$) — the number of elements of each type, respectively.</p><p>It is guaranteed that the sum of $c_i$ for all test cases does not exceed $4 \cdot 10^6$.</p>

## Output

<p>For each test case, print one integer — the number of possible ways to solve the puzzle. </p><p>Two methods are considered different if there is $i$, such that the types of elements at the $i$ position in these methods differ.</p><p>Since the answer can be very large, output it modulo $998244353$.</p><p>If it is impossible to solve the puzzle, print $0$.</p>





```input1|2,4,6,8,10,12
11
1 1 1 1
1 2 5 10
4 6 100 200
900000 900000 900000 900000
0 0 0 0
0 0 566 239
1 0 0 0
100 0 100 0
0 0 0 4
5 5 0 2
5 4 0 5
```




```output1
4
66
0
794100779
1
0
1
0
1
36
126
```


