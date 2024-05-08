## Description

<div><p>Drazil has many friends. Some of them are happy and some of them are unhappy. Drazil wants to make all his friends become happy. So he invented the following plan.</p><p>There are <span class="tex-span"><i>n</i></span> boys and <span class="tex-span"><i>m</i></span> girls among his friends. Let's number them from <span class="tex-span">0</span> to <span class="tex-span"><i>n</i> - 1</span> and <span class="tex-span">0</span> to <span class="tex-span"><i>m</i> - 1</span> separately. In <span class="tex-span"><i>i</i></span>-th day, Drazil invites <img align="middle" class="tex-formula" src="file://dsUcauYK.png" style="max-width: 100.0%;max-height: 100.0%;">-th boy and <img align="middle" class="tex-formula" src="file://rELlVbMT.png" style="max-width: 100.0%;max-height: 100.0%;">-th girl to have dinner together (as Drazil is programmer, <span class="tex-span"><i>i</i></span> starts from <span class="tex-span">0</span>). If one of those two people is happy, the other one will also become happy. Otherwise, those two people remain in their states. Once a person becomes happy (or if it is happy originally), he stays happy forever.</p><p>Drazil wants to know on which day all his friends become happy or to determine if they won't become all happy at all.</p></div><div class="input-specification"><p>The first line contains two integer <span class="tex-span"><i>n</i></span> and <span class="tex-span"><i>m</i></span> (<span class="tex-span">1 ≤ <i>n</i>, <i>m</i> ≤ 10<sup class="upper-index">9</sup></span>).</p><p>The second line contains integer <span class="tex-span"><i>b</i></span> (<span class="tex-span">0 ≤ <i>b</i> ≤ <i>min</i>(<i>n</i>, 10<sup class="upper-index">5</sup>)</span>), denoting the number of happy boys among friends of Drazil, and then follow <span class="tex-span"><i>b</i></span> distinct integers <span class="tex-span"><i>x</i><sub class="lower-index">1</sub>, <i>x</i><sub class="lower-index">2</sub>, ..., <i>x</i><sub class="lower-index"><i>b</i></sub></span> (<span class="tex-span">0 ≤ <i>x</i><sub class="lower-index"><i>i</i></sub> &lt; <i>n</i></span>), denoting the list of indices of happy boys.</p><p>The third line conatins integer <span class="tex-span"><i>g</i></span> (<span class="tex-span">0 ≤ <i>g</i> ≤ <i>min</i>(<i>m</i>, 10<sup class="upper-index">5</sup>)</span>), denoting the number of happy girls among friends of Drazil, and then follow <span class="tex-span"><i>g</i></span> distinct integers <span class="tex-span"><i>y</i><sub class="lower-index">1</sub>, <i>y</i><sub class="lower-index">2</sub>, ... , <i>y</i><sub class="lower-index"><i>g</i></sub></span> (<span class="tex-span">0 ≤ <i>y</i><sub class="lower-index"><i>j</i></sub> &lt; <i>m</i></span>), denoting the list of indices of happy girls.</p><p>It is guaranteed that there is at least one person that is unhappy among his friends.</p></div><div class="output-specification"><p>Print the number of the first day that all friends of Drazil become happy. If this day won't come at all, you print -1.</p></div>

## Input

<p>The first line contains two integer <span class="tex-span"><i>n</i></span> and <span class="tex-span"><i>m</i></span> (<span class="tex-span">1 ≤ <i>n</i>, <i>m</i> ≤ 10<sup class="upper-index">9</sup></span>).</p><p>The second line contains integer <span class="tex-span"><i>b</i></span> (<span class="tex-span">0 ≤ <i>b</i> ≤ <i>min</i>(<i>n</i>, 10<sup class="upper-index">5</sup>)</span>), denoting the number of happy boys among friends of Drazil, and then follow <span class="tex-span"><i>b</i></span> distinct integers <span class="tex-span"><i>x</i><sub class="lower-index">1</sub>, <i>x</i><sub class="lower-index">2</sub>, ..., <i>x</i><sub class="lower-index"><i>b</i></sub></span> (<span class="tex-span">0 ≤ <i>x</i><sub class="lower-index"><i>i</i></sub> &lt; <i>n</i></span>), denoting the list of indices of happy boys.</p><p>The third line conatins integer <span class="tex-span"><i>g</i></span> (<span class="tex-span">0 ≤ <i>g</i> ≤ <i>min</i>(<i>m</i>, 10<sup class="upper-index">5</sup>)</span>), denoting the number of happy girls among friends of Drazil, and then follow <span class="tex-span"><i>g</i></span> distinct integers <span class="tex-span"><i>y</i><sub class="lower-index">1</sub>, <i>y</i><sub class="lower-index">2</sub>, ... , <i>y</i><sub class="lower-index"><i>g</i></sub></span> (<span class="tex-span">0 ≤ <i>y</i><sub class="lower-index"><i>j</i></sub> &lt; <i>m</i></span>), denoting the list of indices of happy girls.</p><p>It is guaranteed that there is at least one person that is unhappy among his friends.</p>

## Output

<p>Print the number of the first day that all friends of Drazil become happy. If this day won't come at all, you print -1.</p>





```input1
2 3
0
1 0

```




```input2
2 4
1 0
1 2

```




```input3
2 3
1 0
1 1

```




```input4
99999 100000
2 514 415
2 50216 61205

```




```output1
4

```




```output2
-1

```




```output3
2

```




```output4
4970100515

```



## Note

<p>By <img align="middle" class="tex-formula" src="file://8zcbzpSP.png" style="max-width: 100.0%;max-height: 100.0%;"> we define the remainder of integer division of <span class="tex-span"><i>i</i></span> by <span class="tex-span"><i>k</i></span>.</p><p>In first sample case: </p><ul> <li> On the 0-th day, Drazil invites 0-th boy and 0-th girl. Because 0-th girl is happy at the beginning, 0-th boy become happy at this day. </li><li> On the 1-st day, Drazil invites 1-st boy and 1-st girl. They are both unhappy, so nothing changes at this day. </li><li> On the 2-nd day, Drazil invites 0-th boy and 2-nd girl. Because 0-th boy is already happy he makes 2-nd girl become happy at this day. </li><li> On the 3-rd day, Drazil invites 1-st boy and 0-th girl. 0-th girl is happy, so she makes 1-st boy happy. </li><li> On the 4-th day, Drazil invites 0-th boy and 1-st girl. 0-th boy is happy, so he makes the 1-st girl happy. So, all friends become happy at this moment. </li></ul>
