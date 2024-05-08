## Description

<div><p>Alessia and Bernardo are discovering the world of competitive programming through the books of their university library.</p><p>The library consists of $m$ sections numbered from $1$ to $m$. Each section contains only books dedicated to a particular subject and different sections correspond to different subjects. In order to prevent the students from wandering in the library, the university has established a system of passes. Each pass has a length $y$ associated to it and allows access to an interval of $y$ consecutive sections in the library. During a visit, the student must choose exactly one book from one of these sections and leave the library. Each pass can be used only once.</p><p>At the moment Alessia and Bernardo have $n$ passes of lengths $x_1, \, x_2, \, \dots, \, x_n$. They have different opinions on the best way to improve: Alessia thinks that it is important to study many different topics, while Bernardo believes that it is important to study deeply at least one topic. So, Alessia wants to use the $n$ passes to get $n$ books on distinct topics, while Bernardo would like to get at least two books on the same topic.</p><p>They have reached the following agreement: for each of the following $n$ days, Alessia will choose a pass of length $y$ among those which are still available and an interval of $y$ sections in the library, and Bernardo will go into the library and will take exactly one book from one of those sections.</p><p>Can Bernardo manage to get at least two books on the same subject, or will Alessia be able to avoid it?</p><p>You should decide whether you want to be Alessia or Bernardo, and you have to fulfill the goal of your chosen character. The judge will impersonate the other character. Note that, even if at some moment Bernardo has already taken two books on the same subject, the interaction should go on until the end of the $n$ days.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $m$ ($1 \le n \le 100$, $n \le m \le 5000$) — the number of passes and the number of sections.</p><p>The second line contains $n$ integers $x_1, \, x_2, \, \dots, \, x_n$ ($1 \le x_i \le m$) — the lengths of the passes available.</p></div><div><h2>Interaction</h2><p>First, you should print a line containing either the string $\texttt{Alessia}$ or the string $\texttt{Bernardo}$ — the character that you want to impersonate. </p><p>Then, for each of the $n$ turns:</p><ul> <li> If you are taking the role of Alessia, print a single line consisting of two integers $y$ and $a$ ($1 \le a \le m - y + 1$) — you are choosing a pass of length $y$ and the interval of sections $[a, a + y - 1]$. Note that at least one pass of length $y$ must still be available. After this, read a single integer $b$ ($a \le b \le a + y - 1$) — the subject of the book selected by Bernardo.</li><li> If you are taking the role of Bernardo, read two integers $y$ and $a$ ($1 \le a \le m - y + 1$) — the length of the pass chosen by Alessia and the index of the first section of the interval. It is guaranteed that there is at least one pass of length $y$ available. Then, print a line consisting of a single integer $b$ ($a \le b \le a + y - 1$) — the subject from which you choose to take a book. </li></ul><p>If one of your interactions is malformed, the interactor terminates immediately and your program receives the verdict $\texttt{WRONG-ANSWER}$. Otherwise, you will receive the verdict according to the game's criteria described above.</p><p>After printing a line do not forget to <span class="tex-font-style-bf">end the line</span> and <span class="tex-font-style-bf">flush the output</span>. Otherwise, you will get the verdict $\texttt{TIMELIMIT}$. To flush the output, use:</p><ul> <li> $\texttt{fflush(stdout)}$ in C; </li><li> $\texttt{fflush(stdout)}$, $\texttt{cout &lt;}\texttt{&lt; flush}$ or $\texttt{cout.flush()}$ in C++; </li><li> $\texttt{System.out.flush()}$ in Java and Kotlin; </li><li> $\texttt{sys.stdout.flush()}$ in Python. </li></ul></div>

## Input

<p>The first line contains two integers $n$ and $m$ ($1 \le n \le 100$, $n \le m \le 5000$) — the number of passes and the number of sections.</p><p>The second line contains $n$ integers $x_1, \, x_2, \, \dots, \, x_n$ ($1 \le x_i \le m$) — the lengths of the passes available.</p>





```input1
5 14
3 7 2 3 10
```




```input2
4 10
4 1 6 4
```




```output1
-
```




```output2
-
```



## Note

<p>In the <span class="tex-font-style-bf">first sample</span>, it can be shown that Alessia can accomplish her goal. An example of interaction (after reading the input) follows:</p><p>$$ \begin{array}{|c|c|c|} \hline \textbf{Contestant} &amp; \textbf{Judge} &amp; \textbf{Explanation} \\ \hline \texttt{Alessia} &amp; &amp; \text{The program will act as Alessia} \\ \hline 3 \quad 11 &amp; &amp; \text{Choose $y = 3$ and $a = 11$} \\ \hline &amp; 13 &amp; \text{Judge selects $b = 13$} \\ \hline 10 \quad 2 &amp; &amp; \text{Choose $y = 10$ and $a = 2$} \\ \hline &amp; 9 &amp; \text{Judge selects $b = 9$} \\ \hline 7 \quad 1 &amp; &amp; \text{Choose $y = 7$ and $a = 1$} \\ \hline &amp; 4 &amp; \text{Judge selects $b = 4$} \\ \hline 2 \quad 10 &amp; &amp; \text{Choose $y = 2$ and $a = 10$} \\ \hline &amp; 10 &amp; \text{Judge selects $b = 10$} \\ \hline 3 \quad 6 &amp; &amp; \text{Choose $y = 3$ and $a = 6$} \\ \hline &amp; 7 &amp; \text{Judge selects $b = 7$} \\ \hline \end{array} $$</p><p>The program of the contestant wins because all the books chosen by Bernardo pertain to different topics. The actions performed by the contestant and the judge in this example of interaction may be non-optimal.</p><p>In the <span class="tex-font-style-bf">second sample</span>, it can be shown that Bernardo can manage to fulfil his goal. An example of interaction (after reading the input) follows:</p><p>$$ \begin{array}{|c|c|c|} \hline \textbf{Contestant} &amp; \textbf{Judge} &amp; \textbf{Explanation} \\ \hline \texttt{Bernardo} &amp; &amp; \text{The program will act as Bernardo} \\ \hline &amp; 4 \quad 1 &amp; \text{Judge chooses $y = 4$ and $a = 1$} \\ \hline 4 &amp; &amp; \text{Select $b = 4$} \\ \hline &amp; 1 \quad 10 &amp; \text{Judge chooses $y = 1$ and $a = 10$} \\ \hline 10 &amp; &amp; \text{Select $b = 10$} \\ \hline &amp; 6 \quad 3 &amp; \text{Judge chooses $y = 6$ and $a = 3$} \\ \hline 4 &amp; &amp; \text{Select $b = 4$} \\ \hline &amp; 4 \quad 5 &amp; \text{Judge chooses $y = 4$ and $a = 5$} \\ \hline 8 &amp; &amp; \text{Select $b = 8$} \\ \hline \end{array} $$</p><p>The program of the contestant wins because Bernardo has selected two books on topic number $4$. The actions performed by the contestant and the judge in this example of interaction may be non-optimal.</p>
