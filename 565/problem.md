## Description

<div><p>Ksyusha has a pet chinchilla, a tree on $n$ vertices and huge scissors. A tree is a connected graph without cycles. During a boring physics lesson Ksyusha thought about how to entertain her pet.</p><p>Chinchillas like to play with <span class="tex-font-style-it">branches</span>. <span class="tex-font-style-it">A branch</span> is a tree of $3$ vertices.</p><center> <img class="tex-graphics" src="file://t6Ouz9aW.png" style="max-width: 100.0%;max-height: 100.0%;"> <span class="tex-font-size-small"><span class="tex-font-style-it">The branch</span> looks like this.</span> </center><p><span class="tex-font-style-it">A cut</span> is the removal of some (not yet <span class="tex-font-style-it">cut</span>) edge in the tree. Ksyusha has plenty of free time, so she can afford to make enough <span class="tex-font-style-it">cuts</span> so that the tree splits into <span class="tex-font-style-it">branches</span>. In other words, after several (possibly zero) <span class="tex-font-style-it">cuts</span>, each vertex must belong to <span class="tex-font-style-bf">exactly one</span> <span class="tex-font-style-it">branch</span>.</p><p>Help Ksyusha choose the edges to be <span class="tex-font-style-it">cut</span> or tell that it is impossible.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— number of testcases.</p><p>The first line of each testcase contains a single integer $n$ ($2 \le n \le 2 \cdot 10^5$)&nbsp;— the number of vertices in the tree.</p><p>The next $n - 1$ rows of each testcase contain integers $v_i$ and $u_i$ ($1 \le v_i, u_i \le n$)&nbsp;— the numbers of vertices that the $i$-th edge connects.</p><p>It is guaranteed that this set of edges forms a tree. It is also guaranteed that the sum of $n$ over all testcases <span class="tex-font-style-bf">does not exceed</span> $2 \cdot 10^5$.</p></div><div class="output-specification"><p>Print the answer for each testcase.</p><p>If the desired way to <span class="tex-font-style-it">cut</span> the tree does not exist, print $-1$.</p><p>Otherwise, print an integer $k$&nbsp;— the number of edges to be <span class="tex-font-style-it">cut</span>. In the next line, print $k$ different integers $e_i$ ($1 \le e_i &lt; n$)&nbsp;— numbers of the edges to be <span class="tex-font-style-it">cut</span>. If $k = 0$, print an empty string instead.</p><p>If there are several solutions, you can print any.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— number of testcases.</p><p>The first line of each testcase contains a single integer $n$ ($2 \le n \le 2 \cdot 10^5$)&nbsp;— the number of vertices in the tree.</p><p>The next $n - 1$ rows of each testcase contain integers $v_i$ and $u_i$ ($1 \le v_i, u_i \le n$)&nbsp;— the numbers of vertices that the $i$-th edge connects.</p><p>It is guaranteed that this set of edges forms a tree. It is also guaranteed that the sum of $n$ over all testcases <span class="tex-font-style-bf">does not exceed</span> $2 \cdot 10^5$.</p>

## Output

<p>Print the answer for each testcase.</p><p>If the desired way to <span class="tex-font-style-it">cut</span> the tree does not exist, print $-1$.</p><p>Otherwise, print an integer $k$&nbsp;— the number of edges to be <span class="tex-font-style-it">cut</span>. In the next line, print $k$ different integers $e_i$ ($1 \le e_i &lt; n$)&nbsp;— numbers of the edges to be <span class="tex-font-style-it">cut</span>. If $k = 0$, print an empty string instead.</p><p>If there are several solutions, you can print any.</p>





```input1|2,3,4,5,6,7,8,9,10,17,18,19,20,21,22
4
9
1 2
4 3
7 9
5 4
4 6
3 2
8 7
1 7
6
1 2
1 3
4 3
1 5
6 1
6
1 2
3 2
3 4
4 5
6 5
5
1 3
5 3
5 2
3 4
```




```input2|2,3,7,8,9,10,11,12
4
2
1 2
3
1 2
3 1
6
1 2
3 1
3 4
3 5
6 1
9
2 6
6 9
9 1
9 7
1 8
7 3
8 5
4 7
```




```output1
2
2 8 
-1
1
3 
-1
```




```output2
-1
0

1
2 
2
4 3
```



## Note

<center> <img class="tex-graphics" src="file://V5Ughf4b.png" style="max-width: 100.0%;max-height: 100.0%;"> <span class="tex-font-size-small">The first testcase in first test.</span> </center>
