## Description

<div><p><span class="tex-font-style-bf">This is an interactive problem.</span></p><p>There is an array $a_1, a_2, \dots, a_n$ of $n$ integers hidden from you. Your task is to find the smallest element of the array.</p><p>To do this, you can ask several queries. In each query, you can pick two integers $l$ and $r$ ($1 \leq l \leq r \leq n$). In return, you will be given the value of $\max(a_l, a_{l+1}, \dots, a_r)$. In other words, you will be told the <span class="tex-font-style-bf">maximum</span> value of the subarray from $a_l$ to $a_r$.</p><p>Find the minimum of the array. You can ask at most $\mathbf{624}$ queries.</p><p>It is guaranteed that the values $a_1, a_2, \dots, a_n$ are chosen uniformly at random between $0$ and $2^{32}-1$ (inclusive).</p></div><div><h2>Interaction</h2><p>Begin the interaction by reading an integer $n$ ($1 \le n \le 10^4$) on a separate line.</p><p>To ask a query, print a line in the form $\texttt{?}\;\;l\;\;r$ ($1 \le l \le r \le n$). Then you should read a single line containing the answer to your query.</p><p>After you have determined the answer, print a line in the form $\texttt{!}\;\;x$ where $x$ is the minimum value.</p><p>After printing a query do not forget to output the end of line and flush the output. Otherwise, you will get <span class="tex-font-style-tt">Idleness limit exceeded</span>. To do this, use:</p><ul> <li> <span class="tex-font-style-tt">fflush(stdout)</span> or <span class="tex-font-style-tt">cout.flush()</span> in C++; </li><li> <span class="tex-font-style-tt">System.out.flush()</span> in Java; </li><li> <span class="tex-font-style-tt">flush(output)</span> in Pascal; </li><li> <span class="tex-font-style-tt">stdout.flush()</span> in Python; </li><li> see the documentation for other languages. </li></ul><p>Answer $\texttt{-1}$ means that you made an invalid query. Exit immediately after receiving $\texttt{-1}$ and you will see <span class="tex-font-style-tt">Wrong answer</span> verdict. Otherwise, you can get an arbitrary verdict because your solution will continue to read from a closed stream.</p></div>





```input1
3

1295320727

984617979

1295320727

167316954
```




```output1
? 1 3

? 1 1

? 2 2

? 3 3

! 167316954
```


