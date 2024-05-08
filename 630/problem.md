## Description

<div><p>A regular bracket sequence is a bracket sequence that can be transformed into a correct arithmetic expression by inserting characters "<span class="tex-font-style-tt">1</span>" and "<span class="tex-font-style-tt">+</span>" between the original characters of the sequence. For example:</p><ul> <li> bracket sequences "<span class="tex-font-style-tt">()()</span>" and "<span class="tex-font-style-tt">(())</span>" are regular (the resulting expressions are: "<span class="tex-font-style-tt">(1)+(1)</span>" and "<span class="tex-font-style-tt">((1+1)+1)</span>"); </li><li> bracket sequences "<span class="tex-font-style-tt">)(</span>", "<span class="tex-font-style-tt">(</span>" and "<span class="tex-font-style-tt">)</span>" are not. </li></ul><p>You are given a regular bracket sequence. In one move, you can remove a pair of <span class="tex-font-style-bf">adjacent</span> brackets such that the left one is an opening bracket and the right one is a closing bracket. Then concatenate the resulting parts without changing the order. The cost of this move is the number of brackets to the right of the right bracket of this pair.</p><p>The <span class="tex-font-style-it">cost</span> of the regular bracket sequence is the smallest total cost of the moves required to make the sequence empty.</p><p>Actually, you are not removing any brackets. Instead, you are given a regular bracket sequence and an integer $k$. You can perform the following operation <span class="tex-font-style-bf">at most $k$ times</span>: </p><ul> <li> extract some bracket from the sequence and insert it back at any position (between any two brackets, at the start or at the end; possibly, at the same place it was before). </li></ul><p>After all operations are performed, the bracket sequence has to be regular. What is the smallest possible <span class="tex-font-style-it">cost</span> of the resulting regular bracket sequence?</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a single integer $k$ ($0 \le k \le 5$)&nbsp;— the maximum number of operations you can perform.</p><p>The second line contains a non-empty regular bracket sequence, it consists only of characters '<span class="tex-font-style-tt">(</span>' and '<span class="tex-font-style-tt">)</span>'.</p><p>The total length of the regular bracket sequences over all testcases doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each testcase, print a single integer&nbsp;— the smallest possible <span class="tex-font-style-it">cost</span> of the regular bracket sequence after you perform at most $k$ operations on it.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a single integer $k$ ($0 \le k \le 5$)&nbsp;— the maximum number of operations you can perform.</p><p>The second line contains a non-empty regular bracket sequence, it consists only of characters '<span class="tex-font-style-tt">(</span>' and '<span class="tex-font-style-tt">)</span>'.</p><p>The total length of the regular bracket sequences over all testcases doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>For each testcase, print a single integer&nbsp;— the smallest possible <span class="tex-font-style-it">cost</span> of the regular bracket sequence after you perform at most $k$ operations on it.</p>





```input1|2,3,6,7,10,11,14,15
7
0
()
0
(())
1
(())
5
()
1
(()()(()))
2
((())()(()())((())))
3
((())()(()())((())))
```




```output1
0
1
0
0
1
4
2
```


