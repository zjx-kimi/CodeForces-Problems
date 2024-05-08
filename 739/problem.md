## Description

<div><p>Kid was gifted a tree of $n$ vertices with the root in the vertex $1$. Since he really like <span class="tex-font-style-it">symmetrical</span> objects, Kid wants to find out if this tree is <span class="tex-font-style-it">symmetrical</span>.</p><center> <img class="tex-graphics" src="file://fy0duK4b.png" style="max-width: 100.0%;max-height: 100.0%;"> <span class="tex-font-size-small">For example, the trees in the picture above are <span class="tex-font-style-it">symmetrical</span>.</span> </center><center> <img class="tex-graphics" src="file://6zlk92Es.png" style="max-width: 100.0%;max-height: 100.0%;"> <span class="tex-font-size-small">And the trees in this picture are not <span class="tex-font-style-it">symmetrical</span>.</span> </center><p>Formally, a tree is <span class="tex-font-style-it">symmetrical</span> if there exists an order of children such that:</p><ul> <li> The subtree of the leftmost child of the root is a mirror image of the subtree of the rightmost child; </li><li> the subtree of the second-left child of the root is a mirror image of the subtree of the second-right child of the root; </li><li> ... </li><li> if the number of children of the root is odd, then the subtree of the middle child should be <span class="tex-font-style-it">symmetrical</span>. </li></ul></div><div class="input-specification"><p>The first line of input data contains single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases in the test.</p><p>The first line of each case contains an integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of vertices in the tree.</p><p>The following $n-1$ lines contain two integers each $u$ and $v$ ($1 \le u, v \le n$, $u \neq v$) — indices of vertices connected by an edge.</p><p>It is guaranteed that the sum of $n$ over all cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>Output $t$ strings, each of which is the answer to the corresponding test case. As an answer, output "<span class="tex-font-style-tt">YES</span>" if this tree is <span class="tex-font-style-it">symmetrical</span>, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p></div>

## Input

<p>The first line of input data contains single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases in the test.</p><p>The first line of each case contains an integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of vertices in the tree.</p><p>The following $n-1$ lines contain two integers each $u$ and $v$ ($1 \le u, v \le n$, $u \neq v$) — indices of vertices connected by an edge.</p><p>It is guaranteed that the sum of $n$ over all cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>Output $t$ strings, each of which is the answer to the corresponding test case. As an answer, output "<span class="tex-font-style-tt">YES</span>" if this tree is <span class="tex-font-style-it">symmetrical</span>, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p>





```input1|2,3,4,5,6,7,15,16,17,18,19,20,21,22,23,34,35,36,37,38,39,40,41,42,43
6
6
1 5
1 6
1 2
2 3
2 4
7
1 5
1 3
3 6
1 4
4 7
4 2
9
1 2
2 4
2 3
3 5
1 7
7 6
7 8
8 9
10
2 9
9 10
2 3
6 7
4 3
1 2
3 8
2 5
6 5
10
3 2
8 10
9 7
4 2
8 2
2 1
4 5
6 5
5 7
1
```




```output1
YES
NO
YES
NO
NO
YES
```


