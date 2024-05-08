## Description

<div><p>There is an empty matrix $M$ of size $n\times m$.</p><p>Zhongkao examination is over, and Daniel would like to do some puzzle games. He is going to fill in the matrix $M$ using permutations of length $m$. That is, each row of $M$ must be a permutation of length $m^\dagger$.</p><p>Define the <span class="tex-font-style-it">value</span> of the $i$-th column in $M$ as $v_i=\operatorname{MEX}(M_{1,i},M_{2,i},\ldots,M_{n,i})^\ddagger$. Since Daniel likes diversity, the <span class="tex-font-style-it">beauty</span> of $M$ is $s=\operatorname{MEX}(v_1,v_2,\cdots,v_m)$.</p><p>You have to help Daniel fill in the matrix $M$ and <span class="tex-font-style-bf">maximize</span> its beauty.</p><p>$^\dagger$ A permutation of length $m$ is an array consisting of $m$ distinct integers from $0$ to $m-1$ in arbitrary order. For example, $[1,2,0,4,3]$ is a permutation, but $[0,1,1]$ is not a permutation ($1$ appears twice in the array), and $[0,1,3]$ is also not a permutation ($m-1=2$ but there is $3$ in the array).</p><p>$^\ddagger$ The $\operatorname{MEX}$ of an array is the smallest non-negative integer that does not belong to the array. For example, $\operatorname{MEX}(2,2,1)=0$ because $0$ does not belong to the array, and $\operatorname{MEX}(0,3,1,2)=4$ because $0$, $1$, $2$ and $3$ appear in the array, but $4$ does not.</p></div><div class="input-specification"><p>The first line of input contains a single integer $t$ ($1\le t\le 1000$) — the number of test cases. The description of test cases follows.</p><p>The only line of each test case contains two integers $n$ and $m$ ($1\le n,m\le 2\cdot 10^5$) — the size of the matrix.</p><p>It is guaranteed that the sum of $n\cdot m$ over all test cases does not exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, in the first line output a single integer — the maximum beauty of $M$.</p><p>Then output the matrix $M$ of size $n\times m$ — the matrix you find.</p><p>If there are multiple solutions, you may output any of them.</p></div>

## Input

<p>The first line of input contains a single integer $t$ ($1\le t\le 1000$) — the number of test cases. The description of test cases follows.</p><p>The only line of each test case contains two integers $n$ and $m$ ($1\le n,m\le 2\cdot 10^5$) — the size of the matrix.</p><p>It is guaranteed that the sum of $n\cdot m$ over all test cases does not exceed $2\cdot 10^5$.</p>

## Output

<p>For each test case, in the first line output a single integer — the maximum beauty of $M$.</p><p>Then output the matrix $M$ of size $n\times m$ — the matrix you find.</p><p>If there are multiple solutions, you may output any of them.</p>





```input1|2,4
4
4 3
1 16
6 6
2 1
```




```output1
3
1 0 2
0 2 1
1 0 2
0 2 1
2
14 7 15 4 10 0 8 6 1 2 3 5 9 11 12 13 
6
3 0 1 4 2 5 
5 2 1 0 4 3 
1 3 2 4 5 0 
4 1 3 2 5 0 
4 2 5 3 0 1 
2 4 0 5 1 3
0
0
0
```



## Note

<p>In the first test case:</p><ul> <li> $v_1=\operatorname{MEX}(1,0,1,0)=2$; </li><li> $v_2=\operatorname{MEX}(0,2,0,2)=1$; </li><li> $v_3=\operatorname{MEX}(2,1,2,1)=0$. </li></ul><p>Therefore, $s=\operatorname{MEX}(2,1,0)=3$. </p><p>It can be shown that $3$ is the maximum possible beauty of $M$.</p><p>In the second test case, any permutation will make $s=2$.</p><p>In the third test case:</p><ul> <li> $v_1=\operatorname{MEX}(3,5,1,4,4,2)=0$; </li><li> $v_2=\operatorname{MEX}(0,2,3,1,2,4)=5$; </li><li> $v_3=\operatorname{MEX}(1,1,2,3,5,0)=4$; </li><li> $v_4=\operatorname{MEX}(4,0,4,2,3,5)=1$; </li><li> $v_5=\operatorname{MEX}(2,4,5,5,0,1)=3$; </li><li> $v_6=\operatorname{MEX}(5,3,0,0,1,3)=2$. </li></ul><p>Therefore, $s=\operatorname{MEX}(0,5,4,1,3,2)=6$. </p>
