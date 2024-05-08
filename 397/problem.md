## Description

<div><p>You are given an array of integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le n$). You can perform the following operation several (possibly, zero) times:</p><ul> <li> pick an arbitrary $i$ and perform <span class="tex-font-style-tt">swap</span>$(a_i, a_{a_i})$. </li></ul><p>How many distinct arrays is it possible to attain? Output the answer modulo $(10^9 + 7)$.</p></div><div class="input-specification"><p>The first line contains an integer $n$ ($1 \le n \le 10^6$).</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1\le a_i\le n$).</p></div><div class="output-specification"><p>Output the number of attainable arrays modulo $(10^9 + 7)$.</p></div>

## Input

<p>The first line contains an integer $n$ ($1 \le n \le 10^6$).</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1\le a_i\le n$).</p>

## Output

<p>Output the number of attainable arrays modulo $(10^9 + 7)$.</p>





```input1|
3
1 1 2
```




```input2|
4
2 1 4 3
```




```input3|
6
2 3 1 1 1 2
```




```output1
2
```




```output2
4
```




```output3
18
```



## Note

<p>In the first example, the initial array is $[1, 1, 2]$. If we perform the operation with $i = 3$, we swap $a_3$ and $a_2$, obtaining $[1, 2, 1]$. One can show that there are no other attainable arrays.</p><p>In the second example, the four attainable arrays are $[2, 1, 4, 3]$, $[1, 2, 4, 3]$, $[1, 2, 3, 4]$, $[2, 1, 3, 4]$. One can show that there are no other attainable arrays.</p>
