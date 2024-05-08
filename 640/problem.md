## Description

<div><p>Anton plays his favorite game "Defense of The Ancients 2" for his favorite hero&nbsp;— The Butcher. Now he wants to make his own dinner. To do this he will take a rectangle of height $h$ and width $w$, then make a vertical or horizontal cut so that both resulting parts have integer sides. After that, he will put one of the parts in the box and cut the other again, and so on.</p><p>More formally, a rectangle of size $h \times w$ can be cut into two parts of sizes $x \times w$ and $(h - x) \times w$, where $x$ is an integer from $1$ to $(h - 1)$, or into two parts of sizes $h \times y$ and $h \times (w - y)$, where $y$ is an integer from $1$ to $(w - 1)$.</p><p>He will repeat this operation $n - 1$ times, and then put the remaining rectangle into the box too. Thus, the box will contain $n$ rectangles, of which $n - 1$ rectangles were put in the box as a result of the cuts, and the $n$-th rectangle is the one that the Butcher has left after all $n - 1$ cuts.</p><p>Unfortunately, Butcher forgot the numbers $h$ and $w$, but he still has $n$ rectangles mixed in random order. Note that Butcher <span class="tex-font-style-bf">didn't rotate the rectangles</span>, but only shuffled them. Now he wants to know all possible pairs $(h, w)$ from which this set of rectangles can be obtained. And you have to help him do it!</p><p>It is guaranteed that there exists at least one pair $(h, w)$ from which this set of rectangles can be obtained.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of rectangles obtained.</p><p>The $i$-th of the next $n$ lines contains two integers $a_i$ and $b_i$ ($1 \le a_i, b_i \le 10^6$)&nbsp;— the height and width of the $i$-th rectangle.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, on the first line output a single integer $m$&nbsp;— the number of pairs $(h, w)$ denoting the sizes of rectangles from which the given rectangles can be obtained. Two rectangles are considered different if they have different heights or widths.</p><p>On each of the following $m$ lines print output integers $h_i$ and $w_i$&nbsp;— the height and width of the rectangle from which the given rectangles can be obtained. You can output the rectangles in any order.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of rectangles obtained.</p><p>The $i$-th of the next $n$ lines contains two integers $a_i$ and $b_i$ ($1 \le a_i, b_i \le 10^6$)&nbsp;— the height and width of the $i$-th rectangle.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, on the first line output a single integer $m$&nbsp;— the number of pairs $(h, w)$ denoting the sizes of rectangles from which the given rectangles can be obtained. Two rectangles are considered different if they have different heights or widths.</p><p>On each of the following $m$ lines print output integers $h_i$ and $w_i$&nbsp;— the height and width of the rectangle from which the given rectangles can be obtained. You can output the rectangles in any order.</p>





```input1|2,3,4,5,10,11
4
3
1 2
3 5
1 3
3
1 1
1 1
1 1
1
10 10
4
3 2
5 5
2 2
8 7
```




```output1
1
4 5
2
1 3
3 1
1
10 10
1
13 7
```



## Note

<p>In the first test case, Butcher could only have a rectangle of size $4 \times 5$. Then the cuts could look like this (first the green cut was made, then the red one):</p><center> <img class="tex-graphics" src="file://vmMBH9oH.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>In the second test case, Butcher could have either a rectangle of $1 \times 3$ or $3 \times 1$. The cuts would have looked like this (first the green cut was made, then the red cut):</p><center> <img class="tex-graphics" src="file://mHbSoAej.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>In the third test case, Butcher did not make any cuts, so the rectangle is $10 \times 10$.</p>
