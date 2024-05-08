## Description

<div><p>Little Susie listens to fairy tales before bed every day. Today's fairy tale was about wood cutters and the little girl immediately started imagining the choppers cutting wood. She imagined the situation that is described below.</p><p>There are <span class="tex-span"><i>n</i></span> trees located along the road at points with coordinates <span class="tex-span"><i>x</i><sub class="lower-index">1</sub>, <i>x</i><sub class="lower-index">2</sub>, ..., <i>x</i><sub class="lower-index"><i>n</i></sub></span>. Each tree has its height <span class="tex-span"><i>h</i><sub class="lower-index"><i>i</i></sub></span>. Woodcutters can cut down a tree and fell it to the left or to the right. After that it occupies one of the segments <span class="tex-span">[<i>x</i><sub class="lower-index"><i>i</i></sub> - <i>h</i><sub class="lower-index"><i>i</i></sub>, <i>x</i><sub class="lower-index"><i>i</i></sub>]</span> or <span class="tex-span">[<i>x</i><sub class="lower-index"><i>i</i></sub>;<i>x</i><sub class="lower-index"><i>i</i></sub> + <i>h</i><sub class="lower-index"><i>i</i></sub>]</span>. The tree that is not cut down occupies a single point with coordinate <span class="tex-span"><i>x</i><sub class="lower-index"><i>i</i></sub></span>. Woodcutters can fell a tree if the segment to be occupied by the fallen tree doesn't contain any occupied point. The woodcutters want to process as many trees as possible, so Susie wonders, what is the maximum number of trees to fell. </p></div><div class="input-specification"><p>The first line contains integer <span class="tex-span"><i>n</i></span> (<span class="tex-span">1 ≤ <i>n</i> ≤ 10<sup class="upper-index">5</sup></span>) — the number of trees.</p><p>Next <span class="tex-span"><i>n</i></span> lines contain pairs of integers <span class="tex-span"><i>x</i><sub class="lower-index"><i>i</i></sub>, <i>h</i><sub class="lower-index"><i>i</i></sub></span> (<span class="tex-span">1 ≤ <i>x</i><sub class="lower-index"><i>i</i></sub>, <i>h</i><sub class="lower-index"><i>i</i></sub> ≤ 10<sup class="upper-index">9</sup></span>) — the coordinate and the height of the <span class="tex-span"><i>і</i></span>-th tree.</p><p>The pairs are given in the order of ascending <span class="tex-span"><i>x</i><sub class="lower-index"><i>i</i></sub></span>. No two trees are located at the point with the same coordinate.</p></div><div class="output-specification"><p>Print a single number — the maximum number of trees that you can cut down by the given rules.</p></div>

## Input

<p>The first line contains integer <span class="tex-span"><i>n</i></span> (<span class="tex-span">1 ≤ <i>n</i> ≤ 10<sup class="upper-index">5</sup></span>) — the number of trees.</p><p>Next <span class="tex-span"><i>n</i></span> lines contain pairs of integers <span class="tex-span"><i>x</i><sub class="lower-index"><i>i</i></sub>, <i>h</i><sub class="lower-index"><i>i</i></sub></span> (<span class="tex-span">1 ≤ <i>x</i><sub class="lower-index"><i>i</i></sub>, <i>h</i><sub class="lower-index"><i>i</i></sub> ≤ 10<sup class="upper-index">9</sup></span>) — the coordinate and the height of the <span class="tex-span"><i>і</i></span>-th tree.</p><p>The pairs are given in the order of ascending <span class="tex-span"><i>x</i><sub class="lower-index"><i>i</i></sub></span>. No two trees are located at the point with the same coordinate.</p>

## Output

<p>Print a single number — the maximum number of trees that you can cut down by the given rules.</p>





```input1
5
1 2
2 1
5 10
10 9
19 1

```




```input2
5
1 2
2 1
5 10
10 9
20 1

```




```output1
3

```




```output2
4

```



## Note

<p>In the first sample you can fell the trees like that: </p><ul> <li> fell the <span class="tex-span">1</span>-st tree to the left — now it occupies segment <span class="tex-span">[ - 1;1]</span> </li><li> fell the <span class="tex-span">2</span>-nd tree to the right — now it occupies segment <span class="tex-span">[2;3]</span> </li><li> leave the <span class="tex-span">3</span>-rd tree — it occupies point <span class="tex-span">5</span> </li><li> leave the <span class="tex-span">4</span>-th tree — it occupies point <span class="tex-span">10</span> </li><li> fell the <span class="tex-span">5</span>-th tree to the right — now it occupies segment <span class="tex-span">[19;20]</span> </li></ul><p>In the second sample you can also fell <span class="tex-span">4</span>-th tree to the right, after that it will occupy segment <span class="tex-span">[10;19]</span>.</p>
