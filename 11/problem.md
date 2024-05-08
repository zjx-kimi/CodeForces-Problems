## Description

<div><p>A sequence of brackets is called balanced if one can turn it into a valid math expression by adding characters <span class="tex-font-style-tt">'+'</span> and <span class="tex-font-style-tt">'1'</span>. For example, sequences <span class="tex-font-style-tt">'(())()', '()',</span> and <span class="tex-font-style-tt">'(()(()))'</span> are balanced, while <span class="tex-font-style-tt">')(', '(()',</span> and <span class="tex-font-style-tt">'(()))('</span> are not.</p><p>A subsequence is a sequence that can be derived from the given sequence by deleting zero or more elements without changing the order of the remaining elements.</p><p>You are given three integers $n$, $m$ and $k$. Find the number of sequences consisting of $n$ <span class="tex-font-style-tt">'('</span> and $m$ <span class="tex-font-style-tt">')'</span>, such that the longest balanced subsequence is of length $2 \cdot k$. Since the answer can be large calculate it modulo $1\,000\,000\,007$ ($10^9 + 7$).</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 3 \cdot 10^3$). Description of the test cases follows.</p><p>The first line of each test case contains three integers $n$, $m$ and $k$ ($1 \le n, m, k \le 2 \cdot 10^3$)</p></div><div class="output-specification"><p>For each test case, print one integer — the answer to the problem.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 3 \cdot 10^3$). Description of the test cases follows.</p><p>The first line of each test case contains three integers $n$, $m$ and $k$ ($1 \le n, m, k \le 2 \cdot 10^3$)</p>

## Output

<p>For each test case, print one integer — the answer to the problem.</p>





```input1|2,4
3
2 2 2
3 2 3
3 2 1
```




```output1
2
0
4
```



## Note

<p>For the first test case <span class="tex-font-style-tt">"()()", "(())"</span> are the $2$ sequences</p><p>For the second test case no sequence is possible.</p><p>For the third test case <span class="tex-font-style-tt">")((()", ")(()(", ")()((", "())(("</span> are the $4$ sequences.</p>
