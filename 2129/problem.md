## Description

<div><p>Andrea has come up with what he believes to be a novel sorting algorithm for arrays of length $n$. The algorithm works as follows.</p><p>Initially there is an array of $n$ integers $a_1,\, a_2,\, \dots,\, a_n$. Then, $k$ steps are executed.</p><p>For each $1\le i\le k$, during the $i$-th step the subsequence of the array $a$ with indexes $j_{i,1}&lt; j_{i,2}&lt; \dots&lt; j_{i, q_i}$ is sorted, without changing the values with the remaining indexes. So, the subsequence $a_{j_{i,1}},\, a_{j_{i,2}},\, \dots,\, a_{j_{i,q_i}}$ is sorted and all other elements of $a$ are left untouched.</p><p>Andrea, being eager to share his discovery with the academic community, sent a short paper describing his algorithm to the journal "Annals of Sorting Algorithms" and you are the referee of the paper (that is, the person who must judge the correctness of the paper). You must decide whether Andrea's algorithm is correct, that is, if it sorts any array $a$ of $n$ integers.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $k$ ($1\le n\le 40$, $0\le k\le 10$) — the length of the arrays handled by Andrea's algorithm and the number of steps of Andrea's algorithm.</p><p>Then $k$ lines follow, each describing the subsequence considered in a step of Andrea's algorithm.</p><p>The $i$-th of these lines contains the integer $q_i$ ($1\le q_i\le n$) followed by $q_i$ integers $j_{i,1},\,j_{i,2},\,\dots,\, j_{i,q_i}$ ($1\le j_{i,1}&lt;j_{i,2}&lt;\cdots&lt;j_{i,q_i}\le n$) — the length of the subsequence considered in the $i$-th step and the indexes of the subsequence.</p></div><div class="output-specification"><p>If Andrea's algorithm is correct print <span class="tex-font-style-tt">ACCEPTED</span>, otherwise print <span class="tex-font-style-tt">REJECTED</span>.</p></div>

## Input

<p>The first line contains two integers $n$ and $k$ ($1\le n\le 40$, $0\le k\le 10$) — the length of the arrays handled by Andrea's algorithm and the number of steps of Andrea's algorithm.</p><p>Then $k$ lines follow, each describing the subsequence considered in a step of Andrea's algorithm.</p><p>The $i$-th of these lines contains the integer $q_i$ ($1\le q_i\le n$) followed by $q_i$ integers $j_{i,1},\,j_{i,2},\,\dots,\, j_{i,q_i}$ ($1\le j_{i,1}&lt;j_{i,2}&lt;\cdots&lt;j_{i,q_i}\le n$) — the length of the subsequence considered in the $i$-th step and the indexes of the subsequence.</p>

## Output

<p>If Andrea's algorithm is correct print <span class="tex-font-style-tt">ACCEPTED</span>, otherwise print <span class="tex-font-style-tt">REJECTED</span>.</p>





```input1
4 3
3 1 2 3
3 2 3 4
2 1 2
```




```input2
4 3
3 1 2 3
3 2 3 4
3 1 3 4
```




```input3
3 4
1 1
1 2
1 3
2 1 3
```




```input4
5 2
3 2 3 4
5 1 2 3 4 5
```




```output1
ACCEPTED
```




```output2
REJECTED
```




```output3
REJECTED
```




```output4
ACCEPTED
```



## Note

<p><span class="tex-font-style-bf">Explanation of the first sample:</span> The algorithm consists of $3$ steps. The first one sorts the subsequence $[a_1, a_2, a_3]$, the second one sorts the subsequence $[a_2, a_3, a_4]$, the third one sorts the subsequence $[a_1,a_2]$. For example, if initially $a=[6, 5, 6, 3]$, the algorithm transforms the array as follows (the subsequence that gets sorted is highlighted in red) $$ [{\color{red}6},{\color{red}5},{\color{red}6},3] \rightarrow [5, {\color{red}6}, {\color{red}6}, {\color{red}3}] \rightarrow [{\color{red}5}, {\color{red}3}, 6, 6] \rightarrow [3, 5, 6, 6] \,.$$ One can prove that, for any initial array $a$, at the end of the algorithm the array $a$ will be sorted.</p><p><span class="tex-font-style-bf">Explanation of the second sample:</span> The algorithm consists of $3$ steps. The first one sorts the subsequence $[a_1, a_2, a_3]$, the second one sorts the subsequence $[a_2, a_3, a_4]$, the third one sorts the subsequence $[a_1,a_3,a_4]$. For example, if initially $a=[6, 5, 6, 3]$, the algorithm transforms the array as follows (the subsequence that gets sorted is highlighted in red) $$ [{\color{red}6},{\color{red}5},{\color{red}6},3] \rightarrow [5, {\color{red}6}, {\color{red}6}, {\color{red}3}] \rightarrow [{\color{red}5}, 3, {\color{red}6}, {\color{red}6}] \rightarrow [5, 3, 6, 6] \,.$$ Notice that $a=[6,5,6,3]$ is an example of an array that is not sorted by the algorithm.</p><p><span class="tex-font-style-bf">Explanation of the third sample:</span> The algorithm consists of $4$ steps. The first $3$ steps do nothing because they sort subsequences of length $1$, whereas the fourth step sorts the subsequence $[a_1,a_3]$. For example, if initially $a=[5,6,4]$, the algorithm transforms the array as follows (the subsequence that gets sorted is highlighted in red) $$ [{\color{red}5},6,4] \rightarrow [5,{\color{red}6},4] \rightarrow [5,{\color{red}6},4] \rightarrow [{\color{red}5},6,{\color{red}4}]\rightarrow [4,6,5] \,.$$ Notice that $a=[5,6,4]$ is an example of an array that is not sorted by the algorithm.</p><p><span class="tex-font-style-bf">Explanation of the fourth sample:</span> The algorithm consists of $2$ steps. The first step sorts the subsequences $[a_2,a_3,a_4]$, the second step sorts the whole array $[a_1,a_2,a_3,a_4,a_5]$. For example, if initially $a=[9,8,1,1,1]$, the algorithm transforms the array as follows (the subsequence that gets sorted is highlighted in red) $$ [9,{\color{red}8},{\color{red}1},{\color{red}1},1] \rightarrow [{\color{red}9},{\color{red}1},{\color{red}1},{\color{red}8},{\color{red}1}] \rightarrow [1,1,1,8,9] \,.$$ Since in the last step the whole array is sorted, it is clear that, for any initial array $a$, at the end of the algorithm the array $a$ will be sorted.</p>
