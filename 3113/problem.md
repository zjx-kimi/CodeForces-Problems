## Description

<div><p>Levian works as an accountant in a large company. Levian knows how much the company has earned in each of the $n$ consecutive months — in the $i$-th month the company had income equal to $a_i$ (positive income means profit, negative income means loss, zero income means no change). Because of the general self-isolation, the first $\lceil \tfrac{n}{2} \rceil$ months income might have been completely unstable, but then everything stabilized and for the last $\lfloor \tfrac{n}{2} \rfloor$ months <span class="tex-font-style-bf">the income was the same</span>.</p><p>Levian decided to tell the directors $n-k+1$ numbers — the total income of the company for each $k$ consecutive months. In other words, for each $i$ between $1$ and $n-k+1$ he will say the value $a_i + a_{i+1} + \ldots + a_{i + k - 1}$. For example, if $a=[-1, 0, 1, 2, 2]$ and $k=3$ he will say the numbers $0, 3, 5$.</p><p>Unfortunately, if at least one total income reported by Levian is not a profit (income $\le 0$), the directors will get angry and fire the failed accountant.</p><p>Save Levian's career: find any such $k$, that for each $k$ months in a row the company had made a profit, or report that it is impossible.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($2 \le n \le 5\cdot 10^5$) — the number of months for which Levian must account.</p><p>The second line contains $\lceil{\frac{n}{2}}\rceil$ integers $a_1, a_2, \ldots, a_{\lceil{\frac{n}{2}}\rceil}$, where $a_i$ ($-10^9 \le a_i \le 10^9$) — the income of the company in the $i$-th month.</p><p>Third line contains a single integer $x$ ($-10^9 \le x \le 10^9$) — income in every month from $\lceil{\frac{n}{2}}\rceil + 1$ to $n$.</p></div><div class="output-specification"><p>In a single line, print the appropriate integer $k$ or $-1$, if it does not exist.</p><p>If there are multiple possible answers, you can print any.</p></div>

## Input

<p>The first line contains a single integer $n$ ($2 \le n \le 5\cdot 10^5$) — the number of months for which Levian must account.</p><p>The second line contains $\lceil{\frac{n}{2}}\rceil$ integers $a_1, a_2, \ldots, a_{\lceil{\frac{n}{2}}\rceil}$, where $a_i$ ($-10^9 \le a_i \le 10^9$) — the income of the company in the $i$-th month.</p><p>Third line contains a single integer $x$ ($-10^9 \le x \le 10^9$) — income in every month from $\lceil{\frac{n}{2}}\rceil + 1$ to $n$.</p>

## Output

<p>In a single line, print the appropriate integer $k$ or $-1$, if it does not exist.</p><p>If there are multiple possible answers, you can print any.</p>





```input1
3
2 -1
2
```




```input2
5
2 2 -8
2
```




```input3
6
-2 -2 6
-1
```




```output1
2
```




```output2
-1
```




```output3
4
```



## Note

<p>In the first example, $k=2$ and $k=3$ satisfy: in the first case, Levian will report the numbers $1, 1$, and in the second case — one number $3$.</p><p>In the second example, there is no such $k$.</p><p>In the third example, the only answer is $k=4$: he will report the numbers $1,2,3$.</p>
