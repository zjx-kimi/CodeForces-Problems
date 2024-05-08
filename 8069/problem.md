## Description

<div><p>Vadim is really keen on travelling. Recently he heard about kayaking activity near his town and became very excited about it, so he joined a party of kayakers.</p><p>Now the party is ready to start its journey, but firstly they have to choose kayaks. There are <span class="tex-span">2·<i>n</i></span> people in the group (including Vadim), and they have exactly <span class="tex-span"><i>n</i> - 1</span> tandem kayaks (each of which, obviously, can carry two people) and <span class="tex-span">2</span> single kayaks. <span class="tex-span"><i>i</i></span>-th person's weight is <span class="tex-span"><i>w</i><sub class="lower-index"><i>i</i></sub></span>, and weight is an important matter in kayaking — if the difference between the weights of two people that sit in the same tandem kayak is too large, then it can crash. And, of course, people want to distribute their seats in kayaks in order to minimize the chances that kayaks will crash.</p><p>Formally, the instability of a single kayak is always <span class="tex-span">0</span>, and the instability of a tandem kayak is the absolute difference between weights of the people that are in this kayak. Instability of the whole journey is the total instability of all kayaks.</p><p>Help the party to determine minimum possible total instability! </p></div><div class="input-specification"><p>The first line contains one number <span class="tex-span"><i>n</i></span> (<span class="tex-span">2 ≤ <i>n</i> ≤ 50</span>).</p><p>The second line contains <span class="tex-span">2·<i>n</i></span> integer numbers <span class="tex-span"><i>w</i><sub class="lower-index">1</sub></span>, <span class="tex-span"><i>w</i><sub class="lower-index">2</sub></span>, ..., <span class="tex-span"><i>w</i><sub class="lower-index">2<i>n</i></sub></span>, where <span class="tex-span"><i>w</i><sub class="lower-index"><i>i</i></sub></span> is weight of person <span class="tex-span"><i>i</i></span> (<span class="tex-span">1 ≤ <i>w</i><sub class="lower-index"><i>i</i></sub> ≤ 1000</span>).</p></div><div class="output-specification"><p>Print minimum possible total instability.</p></div>

## Input

<p>The first line contains one number <span class="tex-span"><i>n</i></span> (<span class="tex-span">2 ≤ <i>n</i> ≤ 50</span>).</p><p>The second line contains <span class="tex-span">2·<i>n</i></span> integer numbers <span class="tex-span"><i>w</i><sub class="lower-index">1</sub></span>, <span class="tex-span"><i>w</i><sub class="lower-index">2</sub></span>, ..., <span class="tex-span"><i>w</i><sub class="lower-index">2<i>n</i></sub></span>, where <span class="tex-span"><i>w</i><sub class="lower-index"><i>i</i></sub></span> is weight of person <span class="tex-span"><i>i</i></span> (<span class="tex-span">1 ≤ <i>w</i><sub class="lower-index"><i>i</i></sub> ≤ 1000</span>).</p>

## Output

<p>Print minimum possible total instability.</p>





```input1
2
1 2 3 4

```




```input2
4
1 3 4 6 3 4 100 200

```




```output1
1

```




```output2
5

```


