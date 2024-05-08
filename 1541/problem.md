## Description

<div><p>A row of $n$ cells is given, all initially white. Using a stamp, you can stamp any two neighboring cells such that one becomes red and the other becomes blue. A stamp can be rotated, i.e. it can be used in both ways: as $\color{blue}{\texttt{B}}\color{red}{\texttt{R}}$ and as $\color{red}{\texttt{R}}\color{blue}{\texttt{B}}$.</p><p>During use, the stamp must completely fit on the given $n$ cells (it cannot be partially outside the cells). The stamp can be applied multiple times to the same cell. Each usage of the stamp recolors both cells that are under the stamp.</p><p>For example, one possible sequence of stamps to make the picture $\color{blue}{\texttt{B}}\color{red}{\texttt{R}}\color{blue}{\texttt{B}}\color{blue}{\texttt{B}}\texttt{W}$ could be $\texttt{WWWWW} \to \texttt{WW}\color{brown}{\underline{\color{red}{\texttt{R}}\color{blue}{\texttt{B}}}}\texttt{W} \to \color{brown}{\underline{\color{blue}{\texttt{B}}\color{red}{\texttt{R}}}}\color{red}{\texttt{R}}\color{blue}{\texttt{B}}\texttt{W} \to \color{blue}{\texttt{B}}\color{brown}{\underline{\color{red}{\texttt{R}}\color{blue}{\texttt{B}}}}\color{blue}{\texttt{B}}\texttt{W}$. Here $\texttt{W}$, $\color{red}{\texttt{R}}$, and $\color{blue}{\texttt{B}}$ represent a white, red, or blue cell, respectively, and the cells that the stamp is used on are marked with an underline.</p><p>Given a final picture, is it possible to make it using the stamp zero or more times?</p></div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains an integer $n$ ($1 \leq n \leq 10^5$)&nbsp;— the length of the picture.</p><p>The second line of each test case contains a string $s$&nbsp;— the picture you need to make. It is guaranteed that the length of $s$ is $n$ and that $s$ only consists of the characters $\texttt{W}$, $\texttt{R}$, and $\texttt{B}$, representing a white, red, or blue cell, respectively.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>Output $t$ lines, each of which contains the answer to the corresponding test case. As an answer, output "<span class="tex-font-style-tt">YES</span>" if it possible to make the picture using the stamp zero or more times, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains an integer $n$ ($1 \leq n \leq 10^5$)&nbsp;— the length of the picture.</p><p>The second line of each test case contains a string $s$&nbsp;— the picture you need to make. It is guaranteed that the length of $s$ is $n$ and that $s$ only consists of the characters $\texttt{W}$, $\texttt{R}$, and $\texttt{B}$, representing a white, red, or blue cell, respectively.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>Output $t$ lines, each of which contains the answer to the corresponding test case. As an answer, output "<span class="tex-font-style-tt">YES</span>" if it possible to make the picture using the stamp zero or more times, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p>





```input1
12
5
BRBBW
1
B
2
WB
2
RW
3
BRB
3
RBB
7
WWWWWWW
9
RBWBWRRBW
10
BRBRBRBRRB
12
BBBRWWRRRWBR
10
BRBRBRBRBW
5
RBWBW
```




```output1
YES
NO
NO
NO
YES
YES
YES
NO
YES
NO
YES
NO
```



## Note

<p>The first test case is explained in the statement.</p><p>For the second, third, and fourth test cases, it is not possible to stamp a single cell, so the answer is "<span class="tex-font-style-tt">NO</span>".</p><p>For the fifth test case, you can use the stamp as follows: $\texttt{WWW} \to \texttt{W}\color{brown}{\underline{\color{red}{\texttt{R}}\color{blue}{\texttt{B}}}} \to \color{brown}{\underline{\color{blue}{\texttt{B}}\color{red}{\texttt{R}}}}\color{blue}{\texttt{B}}$.</p><p>For the sixth test case, you can use the stamp as follows: $\texttt{WWW} \to \texttt{W}\color{brown}{\underline{\color{red}{\texttt{R}}\color{blue}{\texttt{B}}}} \to \color{brown}{\underline{\color{red}{\texttt{R}}\color{blue}{\texttt{B}}}}\color{blue}{\texttt{B}}$.</p><p>For the seventh test case, you don't need to use the stamp at all.</p>
