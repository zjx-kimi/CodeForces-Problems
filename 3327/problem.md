## Description

<div><p>Tired of boring office work, Denis decided to open a fast food restaurant.</p><p>On the first day he made $a$ portions of dumplings, $b$ portions of cranberry juice and $c$ pancakes with condensed milk.</p><p>The peculiarity of Denis's restaurant is the procedure of ordering food. For each visitor Denis himself chooses a set of dishes that this visitor will receive. When doing so, Denis is guided by the following rules:</p><ul> <li> every visitor should receive at least one dish (dumplings, cranberry juice, pancakes with condensed milk are all considered to be dishes); </li><li> each visitor should receive no more than one portion of dumplings, no more than one portion of cranberry juice and no more than one pancake with condensed milk; </li><li> all visitors should receive different sets of dishes. </li></ul><p>What is the maximum number of visitors Denis can feed?</p></div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \le t \le 500$)&nbsp;— the number of test cases to solve.</p><p>Each of the remaining $t$ lines contains integers $a$, $b$ and $c$ ($0 \leq a, b, c \leq 10$)&nbsp;— the number of portions of dumplings, the number of portions of cranberry juice and the number of condensed milk pancakes Denis made.</p></div><div class="output-specification"><p>For each test case print a single integer&nbsp;— the maximum number of visitors Denis can feed.</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \le t \le 500$)&nbsp;— the number of test cases to solve.</p><p>Each of the remaining $t$ lines contains integers $a$, $b$ and $c$ ($0 \leq a, b, c \leq 10$)&nbsp;— the number of portions of dumplings, the number of portions of cranberry juice and the number of condensed milk pancakes Denis made.</p>

## Output

<p>For each test case print a single integer&nbsp;— the maximum number of visitors Denis can feed.</p>





```input1
7
1 2 1
0 0 0
9 1 7
2 2 3
2 3 2
3 2 2
4 4 4

```




```output1
3
0
4
5
5
5
7

```



## Note

<p>In the first test case of the example, Denis can feed the first visitor with dumplings, give the second a portion of cranberry juice, and give the third visitor a portion of cranberry juice and a pancake with a condensed milk.</p><p>In the second test case of the example, the restaurant Denis is not very promising: he can serve no customers.</p><p>In the third test case of the example, Denise can serve four visitors. The first guest will receive a full lunch of dumplings, a portion of cranberry juice and a pancake with condensed milk. The second visitor will get only dumplings. The third guest will receive a pancake with condensed milk, and the fourth guest will receive a pancake and a portion of dumplings. Please note that Denis hasn't used all of the prepared products, but is unable to serve more visitors.</p>
