## Description

<div><p>Vlad found an array $a$ of $n$ integers and decided to sort it in non-decreasing order.</p><p>To do this, Vlad can apply the following operation any number of times:</p><ul> <li> Extract the first element of the array and insert it at the end; </li><li> Swap <span class="tex-font-style-bf">that</span> element with the previous one until it becomes the first or until it becomes <span class="tex-font-style-bf">strictly</span> greater than the previous one. </li></ul><p>Note that both actions are part of the operation, and for one operation, you <span class="tex-font-style-bf">must</span> apply both actions.</p><p>For example, if you apply the operation to the array [$4, 3, 1, 2, 6, 4$], it will change as follows:</p><ul><li> [$\color{red}{4}, 3, 1, 2, 6, 4$];</li><li> [$3, 1, 2, 6, 4, \color{red}{4}$];</li><li> [$3, 1, 2, 6, \color{red}{4}, 4$];</li><li> [$3, 1, 2, \color{red}{4}, 6, 4$].</li></ul><p>Vlad doesn't have time to perform all the operations, so he asks you to determine the minimum number of operations required to sort the array or report that it is impossible.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Descriptions of the test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the array.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, a_3, \dots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the elements of the array.</p><p>It is guaranteed that the sum of $n$ over all testcases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer — the minimum number of operations needed to sort the array. If it is impossible to do so, output $-1$ as the answer.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Descriptions of the test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the array.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, a_3, \dots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the elements of the array.</p><p>It is guaranteed that the sum of $n$ over all testcases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output a single integer — the minimum number of operations needed to sort the array. If it is impossible to do so, output $-1$ as the answer.</p>





```input1|2,3,6,7,10,11
5
5
6 4 1 2 5
7
4 5 3 7 8 6 2
6
4 3 1 2 6 4
4
5 2 4 2
3
2 2 3
```




```output1
2
6
-1
-1
0
```


