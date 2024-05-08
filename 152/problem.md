## Description

<div><p>You are given $N$ buttons (numbered from $1$ to $N$) and $N$ lamps (numbered from $1$ to $N$). Each lamp can either be on or off. Initially, lamp $i$ is on if $A_i = 1$, and off if $A_i = 0$.</p><p>Button $i$ is connected to lamp $i - 1$ (if $i &gt; 1$) and lamp $i + 1$ (if $i &lt; N$). In one move, you can press a button $i$ <span class="tex-font-style-bf">only if lamp $i$ is on</span>. When a button is pressed, the state of the lamps connected to this button is toggled. Formally, the lamps will be on if it was off previously, and the lamps will be off if it was on previously. Note that lamp $i$ is not connected to button $i$, thus, the state of lamp $i$ does not change if button $i$ is pressed.</p><p>After zero or more moves, you want lamp $i$ to be on if $B_i = 1$, and off if $B_i = 0$. Determine if it is possible to achieve this task.</p></div><div class="input-specification"><p>This problem has multiple test cases. The first line consists of an integer $T$ ($1 \leq T \leq 1000$), which represents the number of test cases. Each test case consists of three lines.</p><p>The first line of each test case consists of an integer $N$ ($3 \le N \le 200\,000$). The sum of $N$ over all test cases does not exceed $200\,000$.</p><p>The second line of each test case consists of a string $A$ of length $N$. Each character of $A$ can either be <span class="tex-font-style-tt">0</span> or <span class="tex-font-style-tt">1</span>. The $i$-th character represents the initial state of lamp $i$.</p><p>The third line of each test case consists of a string $A$ of length $N$. Each character of $B$ can either be <span class="tex-font-style-tt">0</span> or <span class="tex-font-style-tt">1</span>. The $i$-th character represents the desired final state of lamp $i$.</p></div><div class="output-specification"><p>For each test case, output <span class="tex-font-style-tt">YES</span> in a single line if the final state of all lamps can be reached after zero or more moves, or <span class="tex-font-style-tt">NO</span> otherwise.</p></div>

## Input

<p>This problem has multiple test cases. The first line consists of an integer $T$ ($1 \leq T \leq 1000$), which represents the number of test cases. Each test case consists of three lines.</p><p>The first line of each test case consists of an integer $N$ ($3 \le N \le 200\,000$). The sum of $N$ over all test cases does not exceed $200\,000$.</p><p>The second line of each test case consists of a string $A$ of length $N$. Each character of $A$ can either be <span class="tex-font-style-tt">0</span> or <span class="tex-font-style-tt">1</span>. The $i$-th character represents the initial state of lamp $i$.</p><p>The third line of each test case consists of a string $A$ of length $N$. Each character of $B$ can either be <span class="tex-font-style-tt">0</span> or <span class="tex-font-style-tt">1</span>. The $i$-th character represents the desired final state of lamp $i$.</p>

## Output

<p>For each test case, output <span class="tex-font-style-tt">YES</span> in a single line if the final state of all lamps can be reached after zero or more moves, or <span class="tex-font-style-tt">NO</span> otherwise.</p>





```input1
2
4
0101
0100
3
000
010
```




```input2
5
7
0101011
1111010
5
11111
00000
4
1101
1101
6
101010
100100
3
000
000
```




```output1
YES
NO
```




```output2
NO
NO
YES
YES
YES
```



## Note

<p><span class="tex-font-style-it">Explanation for the sample input/output #1</span></p><p>For the first test case, by pressing the buttons $4, 2, 4, 3, 1, 2$ in sequence, the condition of the buttons changes as: $0101 \rightarrow 0111 \rightarrow 1101 \rightarrow 1111 \rightarrow 1010 \rightarrow 1110 \rightarrow 0100$.</p><p>For the second test case, you are unable to press any button, hence it is impossible to reach the final state.</p>
