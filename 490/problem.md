## Description

<div><p>There are $n$ nails driven into the wall, the $i$-th nail is driven $a_i$ meters above the ground, one end of the $b_i$ meters long rope is tied to it. All nails hang at different heights one above the other. One candy is tied to all ropes at once. Candy is tied to end of a rope that is not tied to a nail.</p><p>To take the candy, you need to lower it to the ground. To do this, Rudolph can cut some ropes, one at a time. Help Rudolph find the minimum number of ropes that must be cut to get the candy.</p><p>The figure shows an example of the first test:</p><center>  <img class="tex-graphics" src="file://WxwyxifZ.png" style="max-width: 100.0%;max-height: 100.0%;" width="300px"> </center></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains one integer $n$ ($1 \le n \le 50$)&nbsp;— the number of nails.</p><p>The $i$-th of the next $n$ lines contains two integers $a_i$ and $b_i$ ($1 \le a_i, b_i \le 200$)&nbsp;— the height of the $i$-th nail and the length of the rope tied to it, all $a_i$ are different.</p><p>It is guaranteed that the data is not contradictory, it is possible to build a configuration described in the statement.</p></div><div class="output-specification"><p>For each test case print one integer&nbsp;— the minimum number of ropes that need to be cut to make the candy fall to the ground.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains one integer $n$ ($1 \le n \le 50$)&nbsp;— the number of nails.</p><p>The $i$-th of the next $n$ lines contains two integers $a_i$ and $b_i$ ($1 \le a_i, b_i \le 200$)&nbsp;— the height of the $i$-th nail and the length of the rope tied to it, all $a_i$ are different.</p><p>It is guaranteed that the data is not contradictory, it is possible to build a configuration described in the statement.</p>

## Output

<p>For each test case print one integer&nbsp;— the minimum number of ropes that need to be cut to make the candy fall to the ground.</p>





```input1|2,3,4,5,11,12,13,14,15,16
4
3
4 3
3 1
1 2
4
9 2
5 2
7 7
3 4
5
11 7
5 10
12 9
3 2
1 5
3
5 6
4 5
7 7
```




```output1
2
2
3
0
```


