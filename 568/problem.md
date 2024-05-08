## Description

<div><p>Vlad was given an array $a$ of $n$ positive integers. Now he wants to build a <span class="tex-font-style-it">beautiful</span> array $b$ of length $n$ from it.</p><p>Vlad considers an array <span class="tex-font-style-it">beautiful</span> if all the numbers in it are positive and have the same parity. That is, all numbers in the <span class="tex-font-style-it">beautiful</span> array are <span class="tex-font-style-bf">greater</span> than zero and are either all even or all odd.</p><p>To build the array $b$, Vlad can assign each $b_i$ either the value $a_i$ or $a_i - a_j$, where any $j$ from $1$ to $n$ can be chosen.</p><p>To avoid trying to do the impossible, Vlad asks you to determine whether it is possible to build a <span class="tex-font-style-it">beautiful</span> array $b$ of length $n$ using his array $a$.</p></div><div class="input-specification"><p>The first line of input contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Then follow the descriptions of the test cases.</p><p>The first line of each case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the array $a$.</p><p>The second line of each case contains $n$ positive integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the elements of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>Output $t$ strings, each of which is the answer to the corresponding test case. As the answer, output "<span class="tex-font-style-tt">YES</span>" if Vlad can build a <span class="tex-font-style-it">beautiful</span> array $b$, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p></div>

## Input

<p>The first line of input contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Then follow the descriptions of the test cases.</p><p>The first line of each case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the array $a$.</p><p>The second line of each case contains $n$ positive integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the elements of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>Output $t$ strings, each of which is the answer to the corresponding test case. As the answer, output "<span class="tex-font-style-tt">YES</span>" if Vlad can build a <span class="tex-font-style-it">beautiful</span> array $b$, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p>





```input1|2,3,6,7,10,11,14,15
7
5
2 6 8 4 3
5
1 4 7 6 9
4
2 6 4 10
7
5 29 13 9 10000001 11 3
5
2 1 2 4 2
5
2 4 5 4 3
4
2 5 5 4
```




```output1
NO
YES
YES
YES
YES
NO
NO
```


