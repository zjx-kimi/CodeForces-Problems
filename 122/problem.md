## Description

<div><p>The first location in the <span class="tex-font-style-it">brand new critically acclaimed fantasy action RPG "Ancient Staff"</span> is a poisonous swamp. The swamp has some lily pads growing in it. It can be represented as a $2 \times n$ grid ($2$ rows and $n$ columns), where each cell is either empty or has a lily pad in it.</p><p>There are exactly $n$ lily pads in a swamp&nbsp;— <span class="tex-font-style-bf">one in each column</span>. A frog is sitting on top of every lily pad. In one move, every frog must jump to an adjacent by a side cell.</p><p>After the move, no frog can be outside the grid and no two frogs can share the same lily pad. Two frogs from adjacent cells can't jump towards each other (i.e. swap cells).</p><p>If a frog jumps to a lily pad, it survives. Otherwise, it falls into a poisonous swamp and gets devoured by an eldritch creature living on its bottom.</p><p>You can choose the direction each frogs jumps at. Determine the maximum number of frogs that can survive after one move.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The first line of the testcase contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of columns in a swamp grid.</p><p>Each of the following two lines contains a description of a row of a swamp&nbsp;— a string, consisting of exactly $n$ characters. Each character is either a dot ('.'), denoting a swamp cell, or an asterisk ('*'), denoting a lily pad with a frog.</p><p>In each column, there is exactly one dot and exactly one asterisk. The sum of $n$ over all testcases doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each testcase, print a single integer&nbsp;— the maximum number of frogs that can survive after one move, if you choose the direction each frogs jumps at.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The first line of the testcase contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of columns in a swamp grid.</p><p>Each of the following two lines contains a description of a row of a swamp&nbsp;— a string, consisting of exactly $n$ characters. Each character is either a dot ('.'), denoting a swamp cell, or an asterisk ('*'), denoting a lily pad with a frog.</p><p>In each column, there is exactly one dot and exactly one asterisk. The sum of $n$ over all testcases doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>For each testcase, print a single integer&nbsp;— the maximum number of frogs that can survive after one move, if you choose the direction each frogs jumps at.</p>





```input1|2,3,4,8,9,10
3
5
*..**
.**..
1
*
.
3
...
***
```




```output1
2
0
2
```



## Note

<p>The $i$-th frog is the frog on the lily pad in the $i$-th column.</p><p>In the first testcase: </p><ul> <li> the first frog can't survive because there's no adjacent lily pad; </li><li> the second and the third frogs can jump right and up, respectively,&nbsp;— there's no way to save them both at the same time; </li><li> the fourth and the fifth frogs can jump left and left, respectively,&nbsp;— there's no way to save them both at the same time; note, however, that the third and the fourth frogs will end up in the same cell in the swamp, which is not prohibited. </li></ul>
