## Description

<div><p>Rudolph drew a beautiful Christmas tree and decided to print the picture. However, the ink in the cartridge often runs out at the most inconvenient moment. Therefore, Rudolph wants to calculate in advance how much green ink he will need.</p><p>The tree is a vertical trunk with <span class="tex-font-style-bf">identical</span> triangular branches at different heights. The thickness of the trunk is negligible.</p><p>Each branch is an isosceles triangle with base $d$ and height $h$, whose base is perpendicular to the trunk. The triangles are arranged upward at an angle, and the trunk passes exactly in the middle. The base of the $i$-th triangle is located at a height of $y_i$.</p><p>The figure below shows an example of a tree with $d = 4, h = 2$ and three branches with bases at heights $[1, 4, 5]$.</p><center>  <img class="tex-graphics" src="file://aXS4gOBJ.png" style="max-width: 100.0%;max-height: 100.0%;" width="225px"> </center><p>Help Rudolph calculate the total area of the tree branches.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Then follow the descriptions of the test cases.</p><p>The first line of each test case contains three integers $n, d, h$ ($1 \le n, d, h \le 2 \cdot 10^5$)&nbsp;— the number of branches, the length of the base, and the height of the branches, respectively.</p><p>The second line of each test case contains $n$ integers $y_i$ $(1 \le y_i \le 10^9, y_1 &lt; y_2 &lt; ... &lt; y_n)$ — the heights of the bases of the branches.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single real number on a separate line — the total area of the tree branches. The answer will be considered correct if its absolute or relative error does not exceed $10^{-6}$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Then follow the descriptions of the test cases.</p><p>The first line of each test case contains three integers $n, d, h$ ($1 \le n, d, h \le 2 \cdot 10^5$)&nbsp;— the number of branches, the length of the base, and the height of the branches, respectively.</p><p>The second line of each test case contains $n$ integers $y_i$ $(1 \le y_i \le 10^9, y_1 &lt; y_2 &lt; ... &lt; y_n)$ — the heights of the bases of the branches.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output a single real number on a separate line — the total area of the tree branches. The answer will be considered correct if its absolute or relative error does not exceed $10^{-6}$.</p>





```input1|2,3,6,7,10,11
5
3 4 2
1 4 5
1 5 1
3
4 6 6
1 2 3 4
2 1 200000
1 200000
2 4 3
9 11
```




```output1
11
2.5
34.5
199999.9999975
11.333333
```


