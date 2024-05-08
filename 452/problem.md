## Description

<div><p>Miriany's matchstick is a $2 \times n$ grid that needs to be filled with characters <span class="tex-font-style-tt">A</span> or <span class="tex-font-style-tt">B</span>. </p><p>He has already filled in the first row of the grid and would like you to fill in the second row. You must do so in a way such that the number of <span class="tex-font-style-it">adjacent pairs of cells with different characters</span>$^\dagger$ is equal to $k$. If it is impossible, report so.</p><p>$^\dagger$ An <span class="tex-font-style-it">adjacent pair of cells with different characters</span> is a pair of cells $(r_1, c_1)$ and $(r_2, c_2)$ ($1 \le r_1, r_2 \le 2$, $1 \le c_1, c_2 \le n$) such that $|r_1 - r_2| + |c_1 - c_2| = 1$ and the characters in $(r_1, c_1)$ and $(r_2, c_2)$ are different.</p></div><div class="input-specification"><p>The first line consists of an integer $t$, the number of test cases ($1 \leq t \leq 1000$). The description of the test cases follows.</p><p>The first line of each test case has two integers, $n$ and $k$ ($1 \leq n \leq 2 \cdot 10^5, 0 \leq k \leq 3 \cdot n$)&nbsp;– the number of columns of the matchstick, and the number of adjacent pairs of cells with different characters required.</p><p>The following line contains string $s$ of $n$ characters ($s_i$ is either <span class="tex-font-style-it">A</span> or <span class="tex-font-style-it">B</span>)&nbsp;– Miriany's top row of the matchstick.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, if there is no way to fill the second row with the number of adjacent pairs of cells with different characters equals $k$, output "<span class="tex-font-style-tt">NO</span>". </p><p>Otherwise, output "<span class="tex-font-style-tt">YES</span>". Then, print $n$ characters that a valid bottom row for Miriany's matchstick consists of. If there are several answers, output any of them.</p></div>

## Input

<p>The first line consists of an integer $t$, the number of test cases ($1 \leq t \leq 1000$). The description of the test cases follows.</p><p>The first line of each test case has two integers, $n$ and $k$ ($1 \leq n \leq 2 \cdot 10^5, 0 \leq k \leq 3 \cdot n$)&nbsp;– the number of columns of the matchstick, and the number of adjacent pairs of cells with different characters required.</p><p>The following line contains string $s$ of $n$ characters ($s_i$ is either <span class="tex-font-style-it">A</span> or <span class="tex-font-style-it">B</span>)&nbsp;– Miriany's top row of the matchstick.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, if there is no way to fill the second row with the number of adjacent pairs of cells with different characters equals $k$, output "<span class="tex-font-style-tt">NO</span>". </p><p>Otherwise, output "<span class="tex-font-style-tt">YES</span>". Then, print $n$ characters that a valid bottom row for Miriany's matchstick consists of. If there are several answers, output any of them.</p>





```input1|2,3,6,7
4
10 1
ABBAAABBAA
4 5
AAAA
9 17
BAAABBAAB
4 9
ABAB
```




```output1
NO
YES
BABB
YES
ABABAABAB
NO
```



## Note

<p>In the first test case, it can be proved that there exists no possible way to fill in row $2$ of the grid such that $k = 1$. </p><p>For the second test case, <span class="tex-font-style-tt">BABB</span> is one possible answer.</p><p>The grid below is the result of filling in <span class="tex-font-style-tt">BABB</span> as the second row.</p><center> $\begin{array}{|c|c|} \hline A &amp; A &amp; A &amp; A \cr \hline B &amp; A &amp; B &amp; B \cr \hline \end{array}$ </center><p>The pairs of different characters are shown below in red:</p><center> $\begin{array}{|c|c|} \hline \color{red}{A} &amp; A &amp; A &amp; A \cr \hline \color{red}{B} &amp; A &amp; B &amp; B \cr \hline \end{array}$<p><span class="tex-font-style-tt">—————————————————</span></p><p>$\begin{array}{|c|c|} \hline A &amp; A &amp; \color{red}{A} &amp; A \cr \hline B &amp; A &amp; \color{red}{B} &amp; B \cr \hline \end{array}$</p><p><span class="tex-font-style-tt">—————————————————</span></p><p>$\begin{array}{|c|c|} \hline A &amp; A &amp; A &amp; \color{red}{A} \cr \hline B &amp; A &amp; B &amp; \color{red}{B} \cr \hline \end{array}$</p><p><span class="tex-font-style-tt">—————————————————</span></p><p>$\begin{array}{|c|c|} \hline A &amp; A &amp; A &amp; A \cr \hline \color{red}{B} &amp; \color{red}{A} &amp; B &amp; B \cr \hline \end{array}$</p><p><span class="tex-font-style-tt">—————————————————</span></p><p>$\begin{array}{|c|c|} \hline A &amp; A &amp; A &amp; A \cr \hline B &amp; \color{red}{A} &amp; \color{red}{B} &amp; B \cr \hline \end{array}$</p></center><p>There are a total of $5$ pairs, which satisfies $k$.</p>
