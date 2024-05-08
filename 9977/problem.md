## Description

<div><p>There are $n$ containers of water lined up, numbered from left to right from $1$ to $n$. Each container can hold any amount of water; initially, the $i$-th container contains $a_i$ units of water. The sum of $a_i$ is divisible by $n$.</p><p>You can apply the following operation any (possibly zero) number of times: pour any amount of water from the $i$-th container to the $j$-th container, where $i$ must be <span class="tex-font-style-bf">less</span> than $j$ (i.e. $i&lt;j$). Any index can be chosen as $i$ or $j$ any number of times.</p><p>Determine whether it is possible to make the amount of water in all containers the same using this operation.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then the descriptions of the test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of containers with water.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($0 \le a_i \le 10^9$)&nbsp;— the amounts of water in the containers. It is guaranteed that the sum of $a_i$ in each test case does not exceed $2 \cdot 10^9$. Also, the sum of $a_i$ is divisible by $n$.</p><p>It is guaranteed that the sum of $n$ over all test cases in the input does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>Output $t$ lines, each of which is the answer to the corresponding test case. As the answer, output "<span class="tex-font-style-tt">YES</span>" if it is possible to make the amount of water in all containers the same using the described operation. Otherwise, output "<span class="tex-font-style-tt">NO</span>".</p><p>You can output each letter in any case (lowercase or uppercase). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be accepted as a positive answer.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then the descriptions of the test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of containers with water.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($0 \le a_i \le 10^9$)&nbsp;— the amounts of water in the containers. It is guaranteed that the sum of $a_i$ in each test case does not exceed $2 \cdot 10^9$. Also, the sum of $a_i$ is divisible by $n$.</p><p>It is guaranteed that the sum of $n$ over all test cases in the input does not exceed $2 \cdot 10^5$.</p>

## Output

<p>Output $t$ lines, each of which is the answer to the corresponding test case. As the answer, output "<span class="tex-font-style-tt">YES</span>" if it is possible to make the amount of water in all containers the same using the described operation. Otherwise, output "<span class="tex-font-style-tt">NO</span>".</p><p>You can output each letter in any case (lowercase or uppercase). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be accepted as a positive answer.</p>





```input1|2,3,6,7,10,11
6
1
43
2
1 3
5
4 5 2 1 3
3
1 2 3
7
4 5 5 0 6 4 4
7
6 5 5 1 3 4 4
```




```output1
YES
NO
YES
NO
NO
YES
```



## Note

<p>In the third test case of the example ($a=[4, 5, 2, 1, 3]$), you can proceed as follows:</p><ul> <li> pour $1$ unit of water from the first vessel to the fourth, then $a=[3, 5, 2, 2, 3]$; </li><li> pour $1$ unit of water from the second vessel to the third, then $a=[3, 4, 3, 2, 3]$; </li><li> pour $1$ unit of water from the second vessel to the fourth, then $a=[3, 3, 3, 3, 3]$. </li></ul>
