## Description

<div><p>There are $n$ slimes placed in a line. The slimes are numbered from $1$ to $n$ in order from left to right. The size of the $i$-th slime is $a_i$.</p><p>Every second, the following happens: <span class="tex-font-style-bf">exactly one</span> slime eats one of its neighbors and increases its size by the eaten neighbor's size. A slime can eat its neighbor only if it is strictly bigger than this neighbor. If there is no slime which is strictly bigger than one of its neighbors, the process ends.</p><p>For example, suppose $n = 5$, $a = [2, 2, 3, 1, 4]$. The process can go as follows:</p><ul> <li> first, the $3$-rd slime eats the $2$-nd slime. The size of the $3$-rd slime becomes $5$, the $2$-nd slime is eaten. </li><li> then, the $3$-rd slime eats the $1$-st slime (they are neighbors since the $2$-nd slime is already eaten). The size of the $3$-rd slime becomes $7$, the $1$-st slime is eaten. </li><li> then, the $5$-th slime eats the $4$-th slime. The size of the $5$-th slime becomes $5$, the $4$-th slime is eaten. </li><li> then, the $3$-rd slime eats the $5$-th slime (they are neighbors since the $4$-th slime is already eaten). The size of the $3$-rd slime becomes $12$, the $5$-th slime is eaten. </li></ul><p>For each slime, calculate the minimum number of seconds it takes for this slime to be eaten by another slime (among all possible ways the process can go), or report that it is impossible.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 3 \cdot 10^5$)&nbsp;— the number of slimes.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$).</p><p>The sum of $n$ over all test cases doesn't exceed $3 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print $n$ integers. The $i$-th integer should be equal to the minimum number of seconds it takes for the $i$-th slime to be eaten by another slime or <span class="tex-font-style-tt">-1</span> if it is impossible.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 3 \cdot 10^5$)&nbsp;— the number of slimes.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$).</p><p>The sum of $n$ over all test cases doesn't exceed $3 \cdot 10^5$.</p>

## Output

<p>For each test case, print $n$ integers. The $i$-th integer should be equal to the minimum number of seconds it takes for the $i$-th slime to be eaten by another slime or <span class="tex-font-style-tt">-1</span> if it is impossible.</p>





```input1|2,3,6,7
4
4
3 2 4 2
3
1 2 3
5
2 2 3 1 1
7
4 2 3 6 1 1 8
```




```output1
2 1 2 1 
1 1 -1 
2 1 -1 1 2 
2 1 1 3 1 1 4
```


