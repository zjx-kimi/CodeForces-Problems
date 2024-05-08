## Description

<div><p>A <span class="tex-font-style-it">Latin square</span> is a $3 \times 3$ grid made up of the letters $\texttt{A}$, $\texttt{B}$, and $\texttt{C}$ such that: </p><ul> <li> in each row, the letters $\texttt{A}$, $\texttt{B}$, and $\texttt{C}$ each appear once, and </li><li> in each column, the letters $\texttt{A}$, $\texttt{B}$, and $\texttt{C}$ each appear once. </li></ul> For example, one possible Latin square is shown below. $$\begin{bmatrix} \texttt{A} &amp; \texttt{B} &amp; \texttt{C} \\ \texttt{C} &amp; \texttt{A} &amp; \texttt{B} \\ \texttt{B} &amp; \texttt{C} &amp; \texttt{A} \\ \end{bmatrix}$$<p>You are given a Latin square, but one of the letters was replaced with a question mark $\texttt{?}$. Find the letter that was replaced.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \leq t \leq 108$)&nbsp;— the number of testcases.</p><p>Each test case contains three lines, each consisting of three characters, representing the Latin square. Each character is one of $\texttt{A}$, $\texttt{B}$, $\texttt{C}$, or $\texttt{?}$.</p><p>Each test case is a Latin square with exactly one of the letters replaced with a question mark $\texttt{?}$.</p></div><div class="output-specification"><p>For each test case, output the letter that was replaced.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \leq t \leq 108$)&nbsp;— the number of testcases.</p><p>Each test case contains three lines, each consisting of three characters, representing the Latin square. Each character is one of $\texttt{A}$, $\texttt{B}$, $\texttt{C}$, or $\texttt{?}$.</p><p>Each test case is a Latin square with exactly one of the letters replaced with a question mark $\texttt{?}$.</p>

## Output

<p>For each test case, output the letter that was replaced.</p>





```input1|2,3,4,8,9,10
3
ABC
C?B
BCA
BCA
CA?
ABC
?AB
BCA
ABC
```




```output1
A
B
C
```



## Note

<p>The correct Latin squares for the three test cases are shown below:</p><p>$$\begin{bmatrix} \texttt{A} &amp; \texttt{B} &amp; \texttt{C} \\ \texttt{C} &amp; \color{red}{\texttt{A}} &amp; \texttt{B} \\ \texttt{B} &amp; \texttt{C} &amp; \texttt{A} \\ \end{bmatrix} \quad \begin{bmatrix} \texttt{B} &amp; \texttt{C} &amp; \texttt{A} \\ \texttt{C} &amp; \texttt{A} &amp; \color{red}{\texttt{B}} \\ \texttt{A} &amp; \texttt{B} &amp; \texttt{C} \\ \end{bmatrix} \quad \begin{bmatrix} \color{red}{\texttt{C}} &amp; \texttt{A} &amp; \texttt{B} \\ \texttt{B} &amp; \texttt{C} &amp; \texttt{A} \\ \texttt{A} &amp; \texttt{B} &amp; \texttt{C} \\ \end{bmatrix}$$</p>
