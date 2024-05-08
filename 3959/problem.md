## Description

<div><p>With your help, Heidi has prepared a plan of trap placement and defence. Yet suddenly, the Doctor popped out of the TARDIS and told her that he had spied on the Daleks' preparations, and there is more of them than ever. Desperate times require desperate measures, so Heidi is going to risk meeting with the Daleks and she will consider placing a trap along <span class="tex-font-style-underline">any</span> Corridor.</p><p>This means she needs your help again in calculating $E_{max}(c)$ – the largest $e \le 10^9$ such that if we changed the energy requirement of $c$ to $e$, then the Daleks might use $c$ in their invasion – but this time for all Time Corridors.</p></div><div class="input-specification"><p>First line: number $n$ of destinations, number $m$ of corridors ($2 \leq n \leq 10^5$, $n - 1 \leq m \leq 10^6$). The next $m$ lines: destinations $a$, $b$ and energy $e$ ($1 \leq a, b \leq n$, $a \neq b$, $0 \leq e \leq 10^9$).</p><p>No pair $\{a, b\}$ will repeat. The graph is guaranteed to be connected. It is <span class="tex-font-style-underline">not</span> guaranteed that all energy requirements $e$ are distinct, or that the minimum spanning tree is unique.</p></div><div class="output-specification"><p>Output $m$ lines, each containing one integer: $E_{max}(c_i)$ for the $i$-th Corridor $c_i$ from the input.</p></div>

## Input

<p>First line: number $n$ of destinations, number $m$ of corridors ($2 \leq n \leq 10^5$, $n - 1 \leq m \leq 10^6$). The next $m$ lines: destinations $a$, $b$ and energy $e$ ($1 \leq a, b \leq n$, $a \neq b$, $0 \leq e \leq 10^9$).</p><p>No pair $\{a, b\}$ will repeat. The graph is guaranteed to be connected. It is <span class="tex-font-style-underline">not</span> guaranteed that all energy requirements $e$ are distinct, or that the minimum spanning tree is unique.</p>

## Output

<p>Output $m$ lines, each containing one integer: $E_{max}(c_i)$ for the $i$-th Corridor $c_i$ from the input.</p>





```input1
3 3
1 2 8
2 3 3
3 1 4

```




```output1
4
8
8

```


