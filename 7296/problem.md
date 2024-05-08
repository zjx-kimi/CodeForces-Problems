## Description

<div><p>Amr bought a new video game "Guess Your Way Out!". The goal of the game is to find an exit from the maze that looks like a perfect binary tree of height <span class="tex-span"><i>h</i></span>. The player is initially standing at the root of the tree and the exit from the tree is located at some leaf node. </p><p>Let's index all the leaf nodes from the left to the right from 1 to <span class="tex-span">2<sup class="upper-index"><i>h</i></sup></span>. The exit is located at some node <span class="tex-span"><i>n</i></span> where <span class="tex-span">1 ≤ <i>n</i> ≤ 2<sup class="upper-index"><i>h</i></sup></span>, the player doesn't know where the exit is so he has to guess his way out!</p><p>Amr follows simple algorithm to choose the path. Let's consider infinite command string "<span class="tex-font-style-tt">LRLRLRLRL...</span>" (consisting of alternating characters '<span class="tex-font-style-tt">L</span>' and '<span class="tex-font-style-tt">R</span>'). Amr sequentially executes the characters of the string using following rules:</p><ul> <li> Character '<span class="tex-font-style-tt">L</span>' means "go to the left child of the current node"; </li><li> Character '<span class="tex-font-style-tt">R</span>' means "go to the right child of the current node"; </li><li> If the destination node is already visited, Amr skips current command, otherwise he moves to the destination node; </li><li> If Amr skipped two consecutive commands, he goes back to the parent of the current node before executing next command; </li><li> If he reached a leaf node that is not the exit, he returns to the parent of the current node; </li><li> If he reaches an exit, the game is finished. </li></ul><p>Now Amr wonders, if he follows this algorithm, how many nodes he is going to visit before reaching the exit?</p></div><div class="input-specification"><p>Input consists of two integers <span class="tex-span"><i>h</i>, <i>n</i></span> (<span class="tex-span">1 ≤ <i>h</i> ≤ 50</span>, <span class="tex-span">1 ≤ <i>n</i> ≤ 2<sup class="upper-index"><i>h</i></sup></span>).</p></div><div class="output-specification"><p>Output a single integer representing the number of nodes (excluding the exit node) Amr is going to visit before reaching the exit by following this algorithm.</p></div>

## Input

<p>Input consists of two integers <span class="tex-span"><i>h</i>, <i>n</i></span> (<span class="tex-span">1 ≤ <i>h</i> ≤ 50</span>, <span class="tex-span">1 ≤ <i>n</i> ≤ 2<sup class="upper-index"><i>h</i></sup></span>).</p>

## Output

<p>Output a single integer representing the number of nodes (excluding the exit node) Amr is going to visit before reaching the exit by following this algorithm.</p>





```input1
1 2

```




```input2
2 3

```




```input3
3 6

```




```input4
10 1024

```




```output1
2
```




```output2
5
```




```output3
10
```




```output4
2046
```



## Note

<p>A perfect binary tree of height <span class="tex-span"><i>h</i></span> is a binary tree consisting of <span class="tex-span"><i>h</i> + 1</span> levels. Level <span class="tex-span">0</span> consists of a single node called <span class="tex-font-style-it">root</span>, level <span class="tex-span"><i>h</i></span> consists of <span class="tex-span">2<sup class="upper-index"><i>h</i></sup></span> nodes called <span class="tex-font-style-it">leaves</span>. Each node that is not a leaf has exactly two children, <span class="tex-font-style-it">left</span> and <span class="tex-font-style-it">right</span> one. </p><p>Following picture illustrates the sample test number <span class="tex-span">3</span>. Nodes are labeled according to the order of visit.</p><p><img class="tex-graphics" src="file://vjgiHybv.png" style="max-width: 100.0%;max-height: 100.0%;"></p>
