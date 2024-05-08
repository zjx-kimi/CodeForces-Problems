## Description

<div><p>You are given an array $a_1, a_2, \dots, a_n$, consisting of $n$ integers.</p><p>You goal is to make is strictly increasing. To achieve that, you perform each of the following operations exactly once: </p><ul> <li> first, remove any element; </li><li> second, select any number of elements (possibly, none or all $n-1$) and add $1$ to them. </li></ul><p>Note that you are not allowed to rearrange the elements of the array.</p><p>For the resulting array $a'$, $a'_1 &lt; a'_2 &lt; \dots &lt; a'_{n-1}$ should hold. Determine if it's possible to achieve that.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a single integer $n$ ($2 \le n \le 2 \cdot 10^5$)&nbsp;— the number of elements of the array.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^6$).</p><p>The sum of $n$ over all testcases doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each testcase, print <span class="tex-font-style-tt">YES</span> if it's possible to remove one element and add $1$ to some elements (possibly, none or all), so that the array becomes strictly increasing. Otherwise, print <span class="tex-font-style-tt">NO</span>.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a single integer $n$ ($2 \le n \le 2 \cdot 10^5$)&nbsp;— the number of elements of the array.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^6$).</p><p>The sum of $n$ over all testcases doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>For each testcase, print <span class="tex-font-style-tt">YES</span> if it's possible to remove one element and add $1$ to some elements (possibly, none or all), so that the array becomes strictly increasing. Otherwise, print <span class="tex-font-style-tt">NO</span>.</p>





```input1|2,3,6,7,10,11,14,15
8
4
4 4 1 5
5
4 4 1 5 5
2
10 5
3
1 2 3
3
2 1 1
4
1 1 1 1
4
1 3 1 2
5
1 1 3 3 1
```




```output1
YES
NO
YES
YES
YES
NO
YES
YES
```



## Note

<p>In the first testcase, you can remove the third element and add $1$ to the second and the last element. $a'$ will become $[4, 5, 6]$, which is strictly increasing.</p><p>In the second testcase, there is no way to perform the operations, so that the result is strictly increasing.</p><p>In the third testcase, you can remove either of the elements.</p><p>In the fourth testcase, you are already given a strictly increasing array, but you still have to remove an element. The result $a'$ can be $[1, 3]$, for example.</p>
