## Description

<div><p>After a successful field test, Heidi is considering deploying a trap along some Corridor, possibly not the first one. She wants to avoid meeting the Daleks inside the Time Vortex, so for abundance of caution she considers placing the traps <span class="tex-font-style-underline">only</span> along those Corridors that are <span class="tex-font-style-underline">not</span> going to be used according to the current Daleks' plan – which is to use a minimum spanning tree of Corridors. Heidi knows that all energy requirements for different Corridors are now different, and that the Daleks have a single unique plan which they are intending to use.</p><p>Your task is to calculate the number $E_{max}(c)$, which is defined in the same way as in the easy version – i.e., the largest $e \le 10^9$ such that if we changed the energy of corridor $c$ to $e$, the Daleks might use it – but now for <span class="tex-font-style-it">every</span> corridor that Heidi considers. </p></div><div class="input-specification"><p>The first line: number $n$ of destinations, number $m$ of Time Corridors ($2 \leq n \leq 10^5$, $n - 1 \leq m \leq 10^6$). The next $m$ lines: destinations $a$, $b$ and energy $e$ ($1 \leq a, b \leq n$, $a \neq b$, $0 \leq e \leq 10^9$).</p><p>No pair $\{a, b\}$ will repeat. The graph is guaranteed to be connected. All energy requirements $e$ are distinct.</p></div><div class="output-specification"><p>Output $m-(n-1)$ lines, each containing one integer: $E_{max}(c_i)$ for the $i$-th Corridor $c_i$ from the input that is not part of the current Daleks' plan (minimum spanning tree).</p></div>

## Input

<p>The first line: number $n$ of destinations, number $m$ of Time Corridors ($2 \leq n \leq 10^5$, $n - 1 \leq m \leq 10^6$). The next $m$ lines: destinations $a$, $b$ and energy $e$ ($1 \leq a, b \leq n$, $a \neq b$, $0 \leq e \leq 10^9$).</p><p>No pair $\{a, b\}$ will repeat. The graph is guaranteed to be connected. All energy requirements $e$ are distinct.</p>

## Output

<p>Output $m-(n-1)$ lines, each containing one integer: $E_{max}(c_i)$ for the $i$-th Corridor $c_i$ from the input that is not part of the current Daleks' plan (minimum spanning tree).</p>





```input1
3 3
1 2 8
2 3 3
3 1 4

```




```output1
4

```



## Note

<p>If $m = n-1$, then you need not output anything.</p>
