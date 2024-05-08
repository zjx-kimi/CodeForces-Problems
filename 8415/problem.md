## Description

<div><p>A country has <span class="tex-span"><i>n</i></span> cities. Initially, there is no road in the country. One day, the king decides to construct some roads connecting pairs of cities. Roads can be traversed either way. He wants those roads to be constructed in such a way that it is possible to go from each city to any other city by traversing at most two roads. You are also given <span class="tex-span"><i>m</i></span> pairs of cities — roads cannot be constructed between these pairs of cities.</p><p>Your task is to construct the minimum number of roads that still satisfy the above conditions. The constraints will guarantee that this is always possible.</p></div><div class="input-specification"><p>The first line consists of two integers <span class="tex-span"><i>n</i></span> and <span class="tex-span"><i>m</i></span> <img align="middle" class="tex-formula" src="file://cjYgHcE0.png" style="max-width: 100.0%;max-height: 100.0%;">.</p><p>Then <span class="tex-span"><i>m</i></span> lines follow, each consisting of two integers <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub></span> and <span class="tex-span"><i>b</i><sub class="lower-index"><i>i</i></sub></span> (<span class="tex-span">1 ≤ <i>a</i><sub class="lower-index"><i>i</i></sub>, <i>b</i><sub class="lower-index"><i>i</i></sub> ≤ <i>n</i></span>, <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub> ≠ <i>b</i><sub class="lower-index"><i>i</i></sub></span>), which means that it is not possible to construct a road connecting cities <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub></span> and <span class="tex-span"><i>b</i><sub class="lower-index"><i>i</i></sub></span>. Consider the cities are numbered from 1 to <span class="tex-span"><i>n</i></span>.</p><p>It is guaranteed that every pair of cities will appear at most once in the input.</p></div><div class="output-specification"><p>You should print an integer <span class="tex-span"><i>s</i></span>: the minimum number of roads that should be constructed, in the first line. Then <span class="tex-span"><i>s</i></span> lines should follow, each consisting of two integers <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub></span> and <span class="tex-span"><i>b</i><sub class="lower-index"><i>i</i></sub></span> (<span class="tex-span">1 ≤ <i>a</i><sub class="lower-index"><i>i</i></sub>, <i>b</i><sub class="lower-index"><i>i</i></sub> ≤ <i>n</i>, <i>a</i><sub class="lower-index"><i>i</i></sub> ≠ <i>b</i><sub class="lower-index"><i>i</i></sub></span>), which means that a road should be constructed between cities <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub></span> and <span class="tex-span"><i>b</i><sub class="lower-index"><i>i</i></sub></span>.</p><p>If there are several solutions, you may print any of them.</p></div>

## Input

<p>The first line consists of two integers <span class="tex-span"><i>n</i></span> and <span class="tex-span"><i>m</i></span> <img align="middle" class="tex-formula" src="file://cjYgHcE0.png" style="max-width: 100.0%;max-height: 100.0%;">.</p><p>Then <span class="tex-span"><i>m</i></span> lines follow, each consisting of two integers <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub></span> and <span class="tex-span"><i>b</i><sub class="lower-index"><i>i</i></sub></span> (<span class="tex-span">1 ≤ <i>a</i><sub class="lower-index"><i>i</i></sub>, <i>b</i><sub class="lower-index"><i>i</i></sub> ≤ <i>n</i></span>, <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub> ≠ <i>b</i><sub class="lower-index"><i>i</i></sub></span>), which means that it is not possible to construct a road connecting cities <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub></span> and <span class="tex-span"><i>b</i><sub class="lower-index"><i>i</i></sub></span>. Consider the cities are numbered from 1 to <span class="tex-span"><i>n</i></span>.</p><p>It is guaranteed that every pair of cities will appear at most once in the input.</p>

## Output

<p>You should print an integer <span class="tex-span"><i>s</i></span>: the minimum number of roads that should be constructed, in the first line. Then <span class="tex-span"><i>s</i></span> lines should follow, each consisting of two integers <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub></span> and <span class="tex-span"><i>b</i><sub class="lower-index"><i>i</i></sub></span> (<span class="tex-span">1 ≤ <i>a</i><sub class="lower-index"><i>i</i></sub>, <i>b</i><sub class="lower-index"><i>i</i></sub> ≤ <i>n</i>, <i>a</i><sub class="lower-index"><i>i</i></sub> ≠ <i>b</i><sub class="lower-index"><i>i</i></sub></span>), which means that a road should be constructed between cities <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub></span> and <span class="tex-span"><i>b</i><sub class="lower-index"><i>i</i></sub></span>.</p><p>If there are several solutions, you may print any of them.</p>





```input1
4 1
1 3

```




```output1
3
1 2
4 2
2 3

```



## Note

<p>This is one possible solution of the example: </p><center> <img class="tex-graphics" src="file://emFX1d3Y.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>These are examples of wrong solutions:</p><center> <img class="tex-graphics" src="file://nwshhwOo.png" style="max-width: 100.0%;max-height: 100.0%;"> </center> The above solution is wrong because it doesn't use the minimum number of edges (<span class="tex-span">4</span> vs <span class="tex-span">3</span>). In addition, it also tries to construct a road between cities <span class="tex-span">1</span> and <span class="tex-span">3</span>, while the input specifies that it is not allowed to construct a road between the pair.<center> <img class="tex-graphics" src="file://8aluQzFm.png" style="max-width: 100.0%;max-height: 100.0%;"> </center> The above solution is wrong because you need to traverse at least <span class="tex-span">3</span> roads to go from city <span class="tex-span">1</span> to city <span class="tex-span">3</span>, whereas in your country it must be possible to go from any city to another by traversing at most <span class="tex-span">2</span> roads.<center> <img class="tex-graphics" src="file://wBxUeOj8.png" style="max-width: 100.0%;max-height: 100.0%;"> </center> Finally, the above solution is wrong because it must be possible to go from any city to another, whereas it is not possible in this country to go from city <span class="tex-span">1</span> to <span class="tex-span">3</span>, <span class="tex-span">2</span> to <span class="tex-span">3</span>, and <span class="tex-span">4</span> to <span class="tex-span">3</span>.
