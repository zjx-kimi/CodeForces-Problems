## Description

<div><p>There is a grid, consisting of $2$ rows and $n$ columns. The rows are numbered from $1$ to $2$ from top to bottom. The columns are numbered from $1$ to $n$ from left to right. Each cell of the grid contains an arrow pointing either to the left or to the right. No arrow points outside the grid.</p><p>There is a robot that starts in a cell $(1, 1)$. Every second, the following two actions happen one after another: </p><ol> <li> Firstly, the robot moves left, right, down or up (<span class="tex-font-style-bf">it can't try to go outside the grid, and can't skip a move</span>); </li><li> then it moves along the arrow that is placed in the current cell (the cell it ends up after its move). </li></ol><p>Your task is to determine whether the robot can reach the cell $(2, n)$.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer ($2 \le n \le 2 \cdot 10^5$).</p><p>The second line contains a string consisting of exactly $n$ characters <span class="tex-font-style-tt">&lt;</span> and/or <span class="tex-font-style-tt">&gt;</span>&nbsp;— the first row of the grid.</p><p>The third line contains a string consisting of exactly $n$ characters <span class="tex-font-style-tt">&lt;</span> and/or <span class="tex-font-style-tt">&gt;</span>&nbsp;— the second row of the grid.</p><p>Additional constraints on the input: </p><ul> <li> $n$ is even; </li><li> there are no arrows pointing outside the grid; </li><li> the sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$. </li></ul></div><div class="output-specification"><p>For each test case, print <span class="tex-font-style-tt">YES</span> if the robot can reach the cell $(2, n)$; otherwise, print <span class="tex-font-style-tt">NO</span>.</p><p>You can print each letter in any case. For example, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span>, <span class="tex-font-style-tt">YeS</span> will all be recognized as positive answer.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer ($2 \le n \le 2 \cdot 10^5$).</p><p>The second line contains a string consisting of exactly $n$ characters <span class="tex-font-style-tt">&lt;</span> and/or <span class="tex-font-style-tt">&gt;</span>&nbsp;— the first row of the grid.</p><p>The third line contains a string consisting of exactly $n$ characters <span class="tex-font-style-tt">&lt;</span> and/or <span class="tex-font-style-tt">&gt;</span>&nbsp;— the second row of the grid.</p><p>Additional constraints on the input: </p><ul> <li> $n$ is even; </li><li> there are no arrows pointing outside the grid; </li><li> the sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$. </li></ul>

## Output

<p>For each test case, print <span class="tex-font-style-tt">YES</span> if the robot can reach the cell $(2, n)$; otherwise, print <span class="tex-font-style-tt">NO</span>.</p><p>You can print each letter in any case. For example, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span>, <span class="tex-font-style-tt">YeS</span> will all be recognized as positive answer.</p>





```input1|2,3,4,8,9,10
4
4
&gt;&gt;&lt;&lt;
&gt;&gt;&gt;&lt;
2
&gt;&lt;
&gt;&lt;
4
&gt;&gt;&gt;&lt;
&gt;&gt;&lt;&lt;
6
&gt;&gt;&lt;&lt;&gt;&lt;
&gt;&lt;&gt;&gt;&gt;&lt;
```




```output1
YES
YES
NO
YES
```



## Note

<p>In the first example, one of the possible paths looks as follows: $(1, 1) \rightarrow (1, 2) \rightarrow (1, 3) \rightarrow (2, 3) \rightarrow (2, 4)$.</p><p>In the second example, one of the possible paths looks as follows: $(1, 1) \rightarrow (2, 1) \rightarrow (2, 2)$.</p><p>In the third example, there is no way to reach the cell $(2, 4)$.</p><p>In the fourth example, one of the possible paths looks as follows: $(1, 1) \rightarrow (2, 1) \rightarrow (2, 2) \rightarrow (1, 2) \rightarrow (1, 3) \rightarrow (2, 3) \rightarrow (2, 4) \rightarrow (2, 5) \rightarrow (2, 6)$.</p>
