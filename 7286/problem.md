## Description

<div><p>Vasya had two arrays consisting of non-negative integers: <span class="tex-span"><i>a</i></span> of size <span class="tex-span"><i>n</i></span> and <span class="tex-span"><i>b</i></span> of size <span class="tex-span"><i>m</i></span>. Vasya chose a positive integer <span class="tex-span"><i>k</i></span> and created an <span class="tex-span"><i>n</i> × <i>m</i></span> matrix <span class="tex-span"><i>v</i></span> using the following formula:</p><center class="tex-equation"><img align="middle" class="tex-formula" src="file://AYw779fX.png" style="max-width: 100.0%;max-height: 100.0%;"></center><p>Vasya wrote down matrix <span class="tex-span"><i>v</i></span> on a piece of paper and put it in the table.</p><p>A year later Vasya was cleaning his table when he found a piece of paper containing an <span class="tex-span"><i>n</i> × <i>m</i></span> matrix <span class="tex-span"><i>w</i></span>. He remembered making a matrix one day by the rules given above but he was not sure if he had found the paper with the matrix <span class="tex-span"><i>v</i></span> from those days. Your task is to find out if the matrix <span class="tex-span"><i>w</i></span> that you've found could have been obtained by following these rules and if it could, then for what numbers <span class="tex-span"><i>k</i>, <i>a</i><sub class="lower-index">1</sub>, <i>a</i><sub class="lower-index">2</sub>, ..., <i>a</i><sub class="lower-index"><i>n</i></sub>, <i>b</i><sub class="lower-index">1</sub>, <i>b</i><sub class="lower-index">2</sub>, ..., <i>b</i><sub class="lower-index"><i>m</i></sub></span> it is possible.</p></div><div class="input-specification"><p>The first line contains integers <span class="tex-span"><i>n</i></span> and <span class="tex-span"><i>m</i></span> (<span class="tex-span">1 ≤ <i>n</i>, <i>m</i> ≤ 100</span>), separated by a space — the number of rows and columns in the found matrix, respectively. </p><p>The <span class="tex-span"><i>i</i></span>-th of the following lines contains numbers <span class="tex-span"><i>w</i><sub class="lower-index"><i>i</i>, 1</sub>, <i>w</i><sub class="lower-index"><i>i</i>, 2</sub>, ..., <i>w</i><sub class="lower-index"><i>i</i>, <i>m</i></sub></span> (<span class="tex-span">0 ≤ <i>w</i><sub class="lower-index"><i>i</i>, <i>j</i></sub> ≤ 10<sup class="upper-index">9</sup></span>), separated by spaces — the elements of the <span class="tex-span"><i>i</i></span>-th row of matrix <span class="tex-span"><i>w</i></span>.</p></div><div class="output-specification"><p>If the matrix <span class="tex-span"><i>w</i></span> could not have been obtained in the manner described above, print "<span class="tex-font-style-tt">NO</span>" (without quotes) in the single line of output.</p><p>Otherwise, print four lines.</p><p>In the first line print "<span class="tex-font-style-tt">YES</span>" (without quotes).</p><p>In the second line print an integer <span class="tex-span"><i>k</i></span> (<span class="tex-span">1 ≤ <i>k</i> ≤ 10<sup class="upper-index">18</sup></span>). Note that each element of table <span class="tex-span"><i>w</i></span> should be in range between <span class="tex-span">0</span> and <span class="tex-span"><i>k</i> - 1</span> inclusively.</p><p>In the third line print <span class="tex-span"><i>n</i></span> integers <span class="tex-span"><i>a</i><sub class="lower-index">1</sub>, <i>a</i><sub class="lower-index">2</sub>, ..., <i>a</i><sub class="lower-index"><i>n</i></sub></span> (<span class="tex-span">0 ≤ <i>a</i><sub class="lower-index"><i>i</i></sub> ≤ 10<sup class="upper-index">18</sup></span>), separated by spaces.</p><p>In the fourth line print <span class="tex-span"><i>m</i></span> integers <span class="tex-span"><i>b</i><sub class="lower-index">1</sub>, <i>b</i><sub class="lower-index">2</sub>, ..., <i>b</i><sub class="lower-index"><i>m</i></sub></span> (<span class="tex-span">0 ≤ <i>b</i><sub class="lower-index"><i>i</i></sub> ≤ 10<sup class="upper-index">18</sup></span>), separated by spaces.</p></div>

## Input

<p>The first line contains integers <span class="tex-span"><i>n</i></span> and <span class="tex-span"><i>m</i></span> (<span class="tex-span">1 ≤ <i>n</i>, <i>m</i> ≤ 100</span>), separated by a space — the number of rows and columns in the found matrix, respectively. </p><p>The <span class="tex-span"><i>i</i></span>-th of the following lines contains numbers <span class="tex-span"><i>w</i><sub class="lower-index"><i>i</i>, 1</sub>, <i>w</i><sub class="lower-index"><i>i</i>, 2</sub>, ..., <i>w</i><sub class="lower-index"><i>i</i>, <i>m</i></sub></span> (<span class="tex-span">0 ≤ <i>w</i><sub class="lower-index"><i>i</i>, <i>j</i></sub> ≤ 10<sup class="upper-index">9</sup></span>), separated by spaces — the elements of the <span class="tex-span"><i>i</i></span>-th row of matrix <span class="tex-span"><i>w</i></span>.</p>

## Output

<p>If the matrix <span class="tex-span"><i>w</i></span> could not have been obtained in the manner described above, print "<span class="tex-font-style-tt">NO</span>" (without quotes) in the single line of output.</p><p>Otherwise, print four lines.</p><p>In the first line print "<span class="tex-font-style-tt">YES</span>" (without quotes).</p><p>In the second line print an integer <span class="tex-span"><i>k</i></span> (<span class="tex-span">1 ≤ <i>k</i> ≤ 10<sup class="upper-index">18</sup></span>). Note that each element of table <span class="tex-span"><i>w</i></span> should be in range between <span class="tex-span">0</span> and <span class="tex-span"><i>k</i> - 1</span> inclusively.</p><p>In the third line print <span class="tex-span"><i>n</i></span> integers <span class="tex-span"><i>a</i><sub class="lower-index">1</sub>, <i>a</i><sub class="lower-index">2</sub>, ..., <i>a</i><sub class="lower-index"><i>n</i></sub></span> (<span class="tex-span">0 ≤ <i>a</i><sub class="lower-index"><i>i</i></sub> ≤ 10<sup class="upper-index">18</sup></span>), separated by spaces.</p><p>In the fourth line print <span class="tex-span"><i>m</i></span> integers <span class="tex-span"><i>b</i><sub class="lower-index">1</sub>, <i>b</i><sub class="lower-index">2</sub>, ..., <i>b</i><sub class="lower-index"><i>m</i></sub></span> (<span class="tex-span">0 ≤ <i>b</i><sub class="lower-index"><i>i</i></sub> ≤ 10<sup class="upper-index">18</sup></span>), separated by spaces.</p>





```input1
2 3
1 2 3
2 3 4

```




```input2
2 2
1 2
2 0

```




```input3
2 2
1 2
2 1

```




```output1
YES
1000000007
0 1 
1 2 3
```




```output2
YES
3
0 1 
1 2
```




```output3
NO

```



## Note

<p>By <img align="middle" class="tex-formula" src="file://XgP9HTo5.png" style="max-width: 100.0%;max-height: 100.0%;"> we denote the remainder of integer division of <span class="tex-span"><i>b</i></span> by <span class="tex-span"><i>c</i></span>.</p><p>It is guaranteed that if there exists some set of numbers <span class="tex-span"><i>k</i>, <i>a</i><sub class="lower-index">1</sub>, ..., <i>a</i><sub class="lower-index"><i>n</i></sub>, <i>b</i><sub class="lower-index">1</sub>, ..., <i>b</i><sub class="lower-index"><i>m</i></sub></span>, that you could use to make matrix <span class="tex-span"><i>w</i></span>, then there also exists a set of numbers that meets the limits <span class="tex-span">1 ≤ <i>k</i> ≤ 10<sup class="upper-index">18</sup></span>, <span class="tex-span">1 ≤ <i>a</i><sub class="lower-index"><i>i</i></sub> ≤ 10<sup class="upper-index">18</sup></span>, <span class="tex-span">1 ≤ <i>b</i><sub class="lower-index"><i>i</i></sub> ≤ 10<sup class="upper-index">18</sup></span> in the output format. In other words, these upper bounds are introduced only for checking convenience purposes.</p>
