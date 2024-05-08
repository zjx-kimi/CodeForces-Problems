## Description

<div><p>Monocarp always starts his morning with a good ol' sandwich. Sandwiches Monocarp makes always consist of bread, cheese and/or ham.</p><p>A sandwich always follows the formula: </p><ul> <li> a piece of bread </li><li> a slice of cheese or ham </li><li> a piece of bread </li><li> $\dots$ </li><li> a slice of cheese or ham </li><li> a piece of bread </li></ul><p>So it always has bread on top and at the bottom, and it alternates between bread and filling, where filling is a slice of either cheese or ham. Each piece of bread and each slice of cheese or ham is called a layer.</p><p>Today Monocarp woke up and discovered that he has $b$ pieces of bread, $c$ slices of cheese and $h$ slices of ham. What is the maximum number of layers his morning sandwich can have?</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of testcases.</p><p>Each testcase consists of three integers $b, c$ and $h$ ($2 \le b \le 100$; $1 \le c, h \le 100$)&nbsp;— the number of pieces of bread, slices of cheese and slices of ham, respectively.</p></div><div class="output-specification"><p>For each testcase, print a single integer&nbsp;— the maximum number of layers Monocarp's morning sandwich can have.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of testcases.</p><p>Each testcase consists of three integers $b, c$ and $h$ ($2 \le b \le 100$; $1 \le c, h \le 100$)&nbsp;— the number of pieces of bread, slices of cheese and slices of ham, respectively.</p>

## Output

<p>For each testcase, print a single integer&nbsp;— the maximum number of layers Monocarp's morning sandwich can have.</p>





```input1|2,4
3
2 1 1
10 1 2
3 7 8
```




```output1
3
7
5
```



## Note

<p>In the first testcase, Monocarp can arrange a sandwich with three layers: either a piece of bread, a slice of cheese and another piece of bread, or a piece of bread, a slice of ham and another piece of bread.</p><p>In the second testcase, Monocarp has a lot of bread, but not too much filling. He can arrange a sandwich with four pieces of bread, one slice of cheese and two slices of ham.</p><p>In the third testcase, it's the opposite&nbsp;— Monocarp has a lot of filling, but not too much bread. He can arrange a sandwich with three pieces of bread and two slices of cheese, for example.</p>
