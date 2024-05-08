## Description

<div><p>There are three cards with letters $\texttt{a}$, $\texttt{b}$, $\texttt{c}$ placed in a row in some order. You can do the following operation <span class="tex-font-style-bf">at most once</span>: </p><ul> <li> Pick two cards, and swap them. </li></ul> Is it possible that the row becomes $\texttt{abc}$ after the operation? Output "<span class="tex-font-style-tt">YES</span>" if it is possible, and "<span class="tex-font-style-tt">NO</span>" otherwise.</div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 6$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains a single string consisting of each of the three characters $\texttt{a}$, $\texttt{b}$, and $\texttt{c}$ exactly once, representing the cards.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if you can make the row $\texttt{abc}$ with at most one operation, or "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 6$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains a single string consisting of each of the three characters $\texttt{a}$, $\texttt{b}$, and $\texttt{c}$ exactly once, representing the cards.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if you can make the row $\texttt{abc}$ with at most one operation, or "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p>





```input1|2,4,6
6
abc
acb
bac
bca
cab
cba
```




```output1
YES
YES
YES
NO
NO
YES
```



## Note

<p>In the first test case, we don't need to do any operations, since the row is already $\texttt{abc}$.</p><p>In the second test case, we can swap $\texttt{c}$ and $\texttt{b}$: $\texttt{acb} \to \texttt{abc}$.</p><p>In the third test case, we can swap $\texttt{b}$ and $\texttt{a}$: $\texttt{bac} \to \texttt{abc}$.</p><p>In the fourth test case, it is impossible to make $\texttt{abc}$ using <span class="tex-font-style-bf">at most one</span> operation.</p>
