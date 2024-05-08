## Description

<div><p>There are <span class="tex-span"><i>n</i></span> balls. They are arranged in a row. Each ball has a color (for convenience an integer) and an integer value. The color of the <span class="tex-span"><i>i</i></span>-th ball is <span class="tex-span"><i>c</i><sub class="lower-index"><i>i</i></sub></span> and the value of the <span class="tex-span"><i>i</i></span>-th ball is <span class="tex-span"><i>v</i><sub class="lower-index"><i>i</i></sub></span>.</p><p>Squirrel Liss chooses some balls and makes a new sequence without changing the relative order of the balls. She wants to maximize the value of this sequence.</p><p>The value of the sequence is defined as the sum of following values for each ball (where <span class="tex-span"><i>a</i></span> and <span class="tex-span"><i>b</i></span> are given constants):</p><ul> <li> If the ball is not in the beginning of the sequence and the color of the ball is same as previous ball's color, add (the value of the ball) <span class="tex-span"> × </span> <span class="tex-span"><i>a</i></span>. </li><li> Otherwise, add (the value of the ball) <span class="tex-span"> × </span> <span class="tex-span"><i>b</i></span>. </li></ul><p>You are given <span class="tex-span"><i>q</i></span> queries. Each query contains two integers <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub></span> and <span class="tex-span"><i>b</i><sub class="lower-index"><i>i</i></sub></span>. For each query find the maximal value of the sequence she can make when <span class="tex-span"><i>a</i> = <i>a</i><sub class="lower-index"><i>i</i></sub></span> and <span class="tex-span"><i>b</i> = <i>b</i><sub class="lower-index"><i>i</i></sub></span>.</p><p>Note that the new sequence can be <span class="tex-font-style-bf">empty</span>, and the value of an empty sequence is defined as zero.</p></div><div class="input-specification"><p>The first line contains two integers <span class="tex-span"><i>n</i></span> and <span class="tex-span"><i>q</i></span> (<span class="tex-span">1 ≤ <i>n</i> ≤ 10<sup class="upper-index">5</sup>;&nbsp;1 ≤ <i>q</i> ≤ 500</span>). The second line contains <span class="tex-span"><i>n</i></span> integers: <span class="tex-span"><i>v</i><sub class="lower-index">1</sub>, <i>v</i><sub class="lower-index">2</sub>, ..., <i>v</i><sub class="lower-index"><i>n</i></sub></span> (<span class="tex-span">|<i>v</i><sub class="lower-index"><i>i</i></sub>| ≤ 10<sup class="upper-index">5</sup></span>). The third line contains <span class="tex-span"><i>n</i></span> integers: <span class="tex-span"><i>c</i><sub class="lower-index">1</sub>, <i>c</i><sub class="lower-index">2</sub>, ..., <i>c</i><sub class="lower-index"><i>n</i></sub></span> (<span class="tex-span">1 ≤ <i>c</i><sub class="lower-index"><i>i</i></sub> ≤ <i>n</i></span>).</p><p>The following <span class="tex-span"><i>q</i></span> lines contain the values of the constants <span class="tex-span"><i>a</i></span> and <span class="tex-span"><i>b</i></span> for queries. The <span class="tex-span"><i>i</i></span>-th of these lines contains two integers <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub></span> and <span class="tex-span"><i>b</i><sub class="lower-index"><i>i</i></sub></span> (<span class="tex-span">|<i>a</i><sub class="lower-index"><i>i</i></sub>|, |<i>b</i><sub class="lower-index"><i>i</i></sub>| ≤ 10<sup class="upper-index">5</sup></span>).</p><p>In each line integers are separated by single spaces.</p></div><div class="output-specification"><p>For each query, output a line containing an integer — the answer to the query. The <span class="tex-span"><i>i</i></span>-th line contains the answer to the <span class="tex-span"><i>i</i></span>-th query in the input order.</p><p>Please, do not write the <span class="tex-font-style-tt">%lld</span> specifier to read or write 64-bit integers in С++. It is preferred to use the <span class="tex-font-style-tt">cin</span>, <span class="tex-font-style-tt">cout</span> streams or the <span class="tex-font-style-tt">%I64d</span> specifier.</p></div>

## Input

<p>The first line contains two integers <span class="tex-span"><i>n</i></span> and <span class="tex-span"><i>q</i></span> (<span class="tex-span">1 ≤ <i>n</i> ≤ 10<sup class="upper-index">5</sup>;&nbsp;1 ≤ <i>q</i> ≤ 500</span>). The second line contains <span class="tex-span"><i>n</i></span> integers: <span class="tex-span"><i>v</i><sub class="lower-index">1</sub>, <i>v</i><sub class="lower-index">2</sub>, ..., <i>v</i><sub class="lower-index"><i>n</i></sub></span> (<span class="tex-span">|<i>v</i><sub class="lower-index"><i>i</i></sub>| ≤ 10<sup class="upper-index">5</sup></span>). The third line contains <span class="tex-span"><i>n</i></span> integers: <span class="tex-span"><i>c</i><sub class="lower-index">1</sub>, <i>c</i><sub class="lower-index">2</sub>, ..., <i>c</i><sub class="lower-index"><i>n</i></sub></span> (<span class="tex-span">1 ≤ <i>c</i><sub class="lower-index"><i>i</i></sub> ≤ <i>n</i></span>).</p><p>The following <span class="tex-span"><i>q</i></span> lines contain the values of the constants <span class="tex-span"><i>a</i></span> and <span class="tex-span"><i>b</i></span> for queries. The <span class="tex-span"><i>i</i></span>-th of these lines contains two integers <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub></span> and <span class="tex-span"><i>b</i><sub class="lower-index"><i>i</i></sub></span> (<span class="tex-span">|<i>a</i><sub class="lower-index"><i>i</i></sub>|, |<i>b</i><sub class="lower-index"><i>i</i></sub>| ≤ 10<sup class="upper-index">5</sup></span>).</p><p>In each line integers are separated by single spaces.</p>

## Output

<p>For each query, output a line containing an integer — the answer to the query. The <span class="tex-span"><i>i</i></span>-th line contains the answer to the <span class="tex-span"><i>i</i></span>-th query in the input order.</p><p>Please, do not write the <span class="tex-font-style-tt">%lld</span> specifier to read or write 64-bit integers in С++. It is preferred to use the <span class="tex-font-style-tt">cin</span>, <span class="tex-font-style-tt">cout</span> streams or the <span class="tex-font-style-tt">%I64d</span> specifier.</p>





```input1
6 3
1 -2 3 4 0 -1
1 2 1 2 1 1
5 1
-2 1
1 0

```




```input2
4 1
-3 6 -1 2
1 2 3 1
1 -1

```




```output1
20
9
4

```




```output2
5

```



## Note

<p>In the first example, to achieve the maximal value:</p><ul> <li> In the first query, you should select 1st, 3rd, and 4th ball. </li><li> In the second query, you should select 3rd, 4th, 5th and 6th ball. </li><li> In the third query, you should select 2nd and 4th ball. </li></ul><p>Note that there may be other ways to achieve the maximal value.</p>
