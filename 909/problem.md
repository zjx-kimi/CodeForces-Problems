## Description

<div><p>The two siblings Alberto and Beatrice have to eat a spinach pizza together. However, none of them likes spinach, so they both want to eat as little as possible.</p><p>The pizza has the shape of a strictly convex polygon with $n$ vertices located at integer coordinates $(x_1, y_1), \, (x_2, y_2), \, \dots, \, (x_n, y_n)$ of the plane.</p><p>The siblings have decided to eat the pizza in the following way: taking turns, starting with Alberto, each sibling chooses a vertex of the remaining part of the pizza and eats out the triangle determined by its two neighboring edges. In this way, after each of the first $n - 3$ turns the pizza will have one less vertex. The game ends after the $(n - 2)$-th turn, when all the pizza has been eaten.</p><p>Assuming that Alberto and Beatrice choose the slices to eat optimally, which of the siblings manages to eat <span class="tex-font-style-bf">at most half</span> of the pizza? You should identify a sibling that has a strategy to do so and help them choose the slices appropriately. Note that it is possible that both Alberto and Beatrice end up eating exactly half of the area if they choose their slices optimally.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($4 \le n \le 100$) — the number of vertices.</p><p>The next $n$ lines contain two integers $x_i$ and $y_i$ each ($-10^6 \le x_i, y_i \le 10^6$) — the coordinates of the $i$-th vertex of the polygon representing the initial shape of the pizza.</p><p>It is guaranteed that the polygon is strictly convex and that its vertices are given in counterclockwise order.</p></div><div><h2>Interaction</h2><p>First, you should print a line containing either the string $\texttt{Alberto}$ or the string $\texttt{Beatrice}$ — the sibling that you will help to win.</p><p>Then, for the next $n - 2$ turns, you will alternate with the judge in choosing a slice of the pizza and removing it, starting with you if you chose to help Alberto, or starting with the judge if you chose to help Beatrice.</p><ul> <li> When it is your turn, print a single line containing an integer $p$ ($1 \leq p \leq n$) that has not been chosen before, indicating that you want to eat the slice determined by the vertex located at $(x_p, y_p)$. </li><li> When it is the judge's turn, read an integer $q$ ($1 \leq q \leq n$), indicating that the other player eats the slice determined by the vertex located at $(x_q, y_q)$. It is guaranteed that $q$ has not been chosen before. </li></ul><p>If one of your interactions is malformed, the interactor terminates immediately and your program receives the verdict $\texttt{WRONG-ANSWER}$. Otherwise, you will receive $\texttt{CORRECT}$ if at the end your player has eaten at most half of the pizza, and $\texttt{WRONG-ANSWER}$ otherwise.</p><p>After printing a line do not forget to <span class="tex-font-style-bf">end the line</span> and <span class="tex-font-style-bf">flush the output</span>. Otherwise, you will get the verdict $\texttt{TIMELIMIT}$. To flush the output, use:</p><ul> <li> $\texttt{fflush(stdout)}$ in C; </li><li> $\texttt{fflush(stdout)}$, $\texttt{cout &lt;}\texttt{&lt; flush}$ or $\texttt{cout.flush()}$ in C++; </li><li> $\texttt{System.out.flush()}$ in Java and Kotlin; </li><li> $\texttt{sys.stdout.flush()}$ in Python. </li></ul></div>

## Input

<p>The first line contains a single integer $n$ ($4 \le n \le 100$) — the number of vertices.</p><p>The next $n$ lines contain two integers $x_i$ and $y_i$ each ($-10^6 \le x_i, y_i \le 10^6$) — the coordinates of the $i$-th vertex of the polygon representing the initial shape of the pizza.</p><p>It is guaranteed that the polygon is strictly convex and that its vertices are given in counterclockwise order.</p>





```input1
4
0 0
6 1
5 3
1 4
```




```input2
6
0 0
2 0
3 2
2 4
0 4
-1 2
```




```input3
7
0 0
2 0
5 2
4 5
1 5
-1 4
-1 2
```




```output1
-
```




```output2
-
```




```output3
-
```



## Note

<p>In the <span class="tex-font-style-bf">first sample</span>, the pizza has area $15$. Alberto can eat less than half of the pizza by eating the slice around vertex $2$ (which has area $6.5$) or around vertex $3$ (which has area $3.5$).</p><center> <img class="tex-graphics" src="file://brJMsEFo.png" style="max-width: 100.0%;max-height: 100.0%;" width="491px"> </center><p>In the <span class="tex-font-style-bf">second sample</span>, it can be proved that both players will eat exactly half of the pizza if they eat optimally. Therefore it is possible to choose to help either Alberto or Beatrice.</p><p>In the <span class="tex-font-style-bf">third sample</span>, it is possible to show that only Beatrice has a strategy to eat at most half of the pizza. The following is an example of a valid interaction (after reading the input):</p><p>$$ \begin{array}{|c|c|c|} \hline \textbf{Contestant} &amp; \textbf{Judge} &amp; \textbf{Explanation} \\ \hline \texttt{Beatrice} &amp; &amp; \text{The contestant will help Beatrice} \\ \hline &amp; \texttt{7} &amp; \text{Alberto eats the triangle with vertices $6$, $7$, $1$ and area $1$} \\ \hline \texttt{2} &amp; &amp; \text{Beatrice eats the triangle with vertices $1$, $2$, $3$ and area $2$} \\ \hline &amp; \texttt{5} &amp; \text{Alberto eats the triangle with vertices $4$, $5$, $6$ and area $1.5$} \\ \hline \texttt{4} &amp; &amp; \text{Beatrice eats the triangle with vertices $3$, $4$, $6$ and area $8$} \\ \hline &amp; \texttt{6} &amp; \text{Alberto eats the triangle with vertices $3$, $6$, $1$ and area $11$} \\ \hline \end{array} $$ The total area eaten by Alberto is $13.5$ and the total area eaten by Beatrice is $10$, which is less than half the area of the whole pizza. The actions performed by the contestant and the judge in this example of interaction may be non-optimal. The process is illustrated below:</p><center> <img class="tex-graphics" src="file://WRq0sttS.png" style="max-width: 100.0%;max-height: 100.0%;" width="605px"> </center>
