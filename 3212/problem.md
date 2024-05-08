## Description

<div><p>Nastya just made a huge mistake and dropped a whole package of rice on the floor. Mom will come soon. If she sees this, then Nastya will be punished.</p><p>In total, Nastya dropped $n$ grains. Nastya read that each grain weighs some integer number of grams from $a - b$ to $a + b$, inclusive (numbers $a$ and $b$ are known), and the whole package of $n$ grains weighs from $c - d$ to $c + d$ grams, inclusive (numbers $c$ and $d$ are known). The weight of the package is the sum of the weights of all $n$ grains in it.</p><p>Help Nastya understand if this information can be correct. In other words, check whether each grain can have such a mass that the $i$-th grain weighs some integer number $x_i$ $(a - b \leq x_i \leq a + b)$, and in total they weigh from $c - d$ to $c + d$, inclusive ($c - d \leq \sum\limits_{i=1}^{n}{x_i} \leq c + d$).</p></div><div class="input-specification"><p>The input consists of multiple test cases. The first line contains a single integer $t$ $(1 \leq t \leq 1000)$ &nbsp;— the number of test cases. </p><p>The next $t$ lines contain descriptions of the test cases, each line contains $5$ integers: $n$ $(1 \leq n \leq 1000)$ &nbsp;— the number of grains that Nastya counted and $a, b, c, d$ $(0 \leq b &lt; a \leq 1000, 0 \leq d &lt; c \leq 1000)$ &nbsp;— numbers that determine the possible weight of one grain of rice (from $a - b$ to $a + b$) and the possible total weight of the package (from $c - d$ to $c + d$).</p></div><div class="output-specification"><p>For each test case given in the input print "Yes", if the information about the weights is not inconsistent, and print "No" if $n$ grains with masses from $a - b$ to $a + b$ cannot make a package with a total mass from $c - d$ to $c + d$.</p></div>

## Input

<p>The input consists of multiple test cases. The first line contains a single integer $t$ $(1 \leq t \leq 1000)$ &nbsp;— the number of test cases. </p><p>The next $t$ lines contain descriptions of the test cases, each line contains $5$ integers: $n$ $(1 \leq n \leq 1000)$ &nbsp;— the number of grains that Nastya counted and $a, b, c, d$ $(0 \leq b &lt; a \leq 1000, 0 \leq d &lt; c \leq 1000)$ &nbsp;— numbers that determine the possible weight of one grain of rice (from $a - b$ to $a + b$) and the possible total weight of the package (from $c - d$ to $c + d$).</p>

## Output

<p>For each test case given in the input print "Yes", if the information about the weights is not inconsistent, and print "No" if $n$ grains with masses from $a - b$ to $a + b$ cannot make a package with a total mass from $c - d$ to $c + d$.</p>





```input1
5
7 20 3 101 18
11 11 10 234 2
8 9 7 250 122
19 41 21 321 10
3 10 8 6 1
```




```output1
Yes
No
Yes
No
Yes
```



## Note

<p>In the first test case of the example, we can assume that each grain weighs $17$ grams, and a pack $119$ grams, then really Nastya could collect the whole pack.</p><p>In the third test case of the example, we can assume that each grain weighs $16$ grams, and a pack $128$ grams, then really Nastya could collect the whole pack.</p><p>In the fifth test case of the example, we can be assumed that $3$ grains of rice weigh $2$, $2$, and $3$ grams, and a pack is $7$ grams, then really Nastya could collect the whole pack.</p><p>In the second and fourth test cases of the example, we can prove that it is impossible to determine the correct weight of all grains of rice and the weight of the pack so that the weight of the pack is equal to the total weight of all collected grains.</p>
