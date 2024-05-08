## Description

<div><p>Once upon a time Algoland and Berland were a single country, but those times are long gone. Now they are two different countries, but their cities are scattered on a common territory.</p><p>All cities are represented as points on the Cartesian plane. Algoland consists of $a$ cities numbered from $1$ to $a$. The coordinates of the $i$-th Algoland city are a pair of integer numbers $(xa_i, ya_i)$. Similarly, Berland consists of $b$ cities numbered from $1$ to $b$. The coordinates of the $j$-th Berland city are a pair of integer numbers $(xb_j, yb_j)$. <span class="tex-font-style-it">No three of the $a+b$ mentioned cities lie on a single straight line</span>.</p><p>As the first step to unite the countries, Berland decided to build several bidirectional freeways. Each freeway is going to be a line segment that starts in a Berland city and ends in an Algoland city. Freeways can't intersect with each other at any point except freeway's start or end. Moreover, the freeways have to connect all $a+b$ cities. Here, connectivity means that one can get from any of the specified $a+b$ cities to any other of the $a+b$ cities using freeways. Note that all freeways are bidirectional, which means that one can drive on each of them in both directions.</p><p>Mayor of each of the $b$ Berland cities allocated a budget to build the freeways that start from this city. Thus, you are given the numbers $r_1, r_2, \dots, r_b$, where $r_j$ is the number of freeways that are going to start in the $j$-th Berland city. The total allocated budget is very tight and only covers building the minimal necessary set of freeways. In other words, $r_1+r_2+\dots+r_b=a+b-1$.</p><p>Help Berland to build the freeways so that:</p><ul> <li> each freeway is a line segment connecting a Berland city and an Algoland city, </li><li> no freeways intersect with each other except for the freeway's start or end, </li><li> freeways connect all $a+b$ cities (all freeways are bidirectional), </li><li> there are $r_j$ freeways that start from the $j$-th Berland city. </li></ul></div><div class="input-specification"><p>Input contains one or several test cases. The first input line contains a single integer number $t$ ($1 \le t \le 3000$) — number of test cases. Then, $t$ test cases follow. Solve test cases separately, test cases are completely independent and do not affect each other.</p><p>Each test case starts with a line containing space-separated integers $a$ and $b$ ($1 \le a, b \le 3000$) — numbers of Algoland cities and number of Berland cities correspondingly.</p><p>The next line contains $b$ space-separated integers $r_1, r_2, \dots, r_b$ ($1 \le r_b \le a$) where $r_j$ is the number of freeways, that should start in the $j$-th Berland city. It is guaranteed that $r_1+r_2+\dots+r_b=a+b-1$.</p><p>The next $a$ lines contain coordinates of the Algoland cities — pairs of space-separated integers $xa_i, ya_i$ ($-10000 \le xa_i, ya_i \le 10000$). The next $b$ lines contain coordinates of the Berland cities — pairs of space-separated integers $xb_i, yb_i$ ($-10000 \le xb_i, yb_i \le 10000$). All cities are located at distinct points, no three of the $a+b$ cities lie on a single straight line.</p><p>Sum of values $a$ across all test cases doesn't exceed $3000$. Sum of values $b$ across all test cases doesn't exceed $3000$.</p></div><div class="output-specification"><p>For each of the $t$ test cases, first print "<span class="tex-font-style-tt">YES</span>" if there is an answer or "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>If there is an answer, print the freeway building plan in the next $a+b-1$ lines. Each line of the plan should contain two space-separated integers $j$ and $i$ which means that a freeway from the $j$-th Berland city to the $i$-th Algoland city should be built. If there are multiple solutions, print any.</p></div>

## Input

<p>Input contains one or several test cases. The first input line contains a single integer number $t$ ($1 \le t \le 3000$) — number of test cases. Then, $t$ test cases follow. Solve test cases separately, test cases are completely independent and do not affect each other.</p><p>Each test case starts with a line containing space-separated integers $a$ and $b$ ($1 \le a, b \le 3000$) — numbers of Algoland cities and number of Berland cities correspondingly.</p><p>The next line contains $b$ space-separated integers $r_1, r_2, \dots, r_b$ ($1 \le r_b \le a$) where $r_j$ is the number of freeways, that should start in the $j$-th Berland city. It is guaranteed that $r_1+r_2+\dots+r_b=a+b-1$.</p><p>The next $a$ lines contain coordinates of the Algoland cities — pairs of space-separated integers $xa_i, ya_i$ ($-10000 \le xa_i, ya_i \le 10000$). The next $b$ lines contain coordinates of the Berland cities — pairs of space-separated integers $xb_i, yb_i$ ($-10000 \le xb_i, yb_i \le 10000$). All cities are located at distinct points, no three of the $a+b$ cities lie on a single straight line.</p><p>Sum of values $a$ across all test cases doesn't exceed $3000$. Sum of values $b$ across all test cases doesn't exceed $3000$.</p>

## Output

<p>For each of the $t$ test cases, first print "<span class="tex-font-style-tt">YES</span>" if there is an answer or "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>If there is an answer, print the freeway building plan in the next $a+b-1$ lines. Each line of the plan should contain two space-separated integers $j$ and $i$ which means that a freeway from the $j$-th Berland city to the $i$-th Algoland city should be built. If there are multiple solutions, print any.</p>





```input1
2
2 3
1 1 2
0 0
1 1
1 2
3 2
4 0
1 1
1
0 0
0 1

```




```output1
YES
2 2
1 2
3 2
3 1
YES
1 1

```


