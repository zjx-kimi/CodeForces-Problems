## Description

<div><p>You are playing a word puzzle. The puzzle starts with a $3$ by $3$ grid, where each cell contains either the letter <span class="tex-font-style-tt">A</span>, <span class="tex-font-style-tt">B</span>, or <span class="tex-font-style-tt">C</span>.</p><p>The goal of this puzzle is to find the lexicographically smallest possible word of length $3$. The word can be formed by choosing three different cells where the cell containing the first letter is adjacent to the cell containing the second letter, and the cell containing the second letter is adjacent to the cell containing the third letter.</p><p>Two cells are adjacent to each other if they share a border or a corner, as shown in the following illustration. Formally, if $(r, c)$ denotes the cell in the $r$-th row and $c$-th column, then cell $(r, c)$ is adjacent to cell $(r, c + 1)$, $(r - 1, c + 1)$, $(r - 1, c)$, $(r - 1, c - 1)$, $(r, c - 1)$, $(r + 1, c - 1)$, $(r + 1, c)$, and $(r + 1, c + 1)$.</p><center> <img class="tex-graphics" src="file://7GvzF2ck.png" style="max-width: 100.0%;max-height: 100.0%;" width="76px"> </center><p>Determine the lexicographically smallest possible word of length $3$ that you can find within the grid.</p><p>A string $s$ of length $n$ is lexicographically smaller than string $t$ of the same length if there exists an integer $1 \leq i \leq n$ such that $s_j = t_j$ for all $1 \leq j &lt; i$, and $s_i &lt; t_i$ in alphabetical order. The following illustration shows some examples on some grids and their the lexicographically smallest possible word of length $3$ that you can find within the grids.</p><center> <img class="tex-graphics" src="file://LP6wI9cT.png" style="max-width: 100.0%;max-height: 100.0%;" width="454px"> </center></div><div class="input-specification"><p>Input consists of three lines, each containing three letters, representing the puzzle grid. Each letter in the grid can only be either <span class="tex-font-style-tt">A</span>, <span class="tex-font-style-tt">B</span>, or <span class="tex-font-style-tt">C</span>.</p></div><div class="output-specification"><p>Output the lexicographically smallest possible word of length $3$ that you can find within the grid.</p></div>

## Input

<p>Input consists of three lines, each containing three letters, representing the puzzle grid. Each letter in the grid can only be either <span class="tex-font-style-tt">A</span>, <span class="tex-font-style-tt">B</span>, or <span class="tex-font-style-tt">C</span>.</p>

## Output

<p>Output the lexicographically smallest possible word of length $3$ that you can find within the grid.</p>





```input1
BCB
CAC
BCB
```




```input2
BCB
CCC
CCA
```




```input3
ACA
CBC
ACA
```




```input4
ACA
CAC
ACA
```




```input5
CCC
CBC
CCC
```




```output1
ABC
```




```output2
ACB
```




```output3
ABA
```




```output4
AAA
```




```output5
BCC
```


