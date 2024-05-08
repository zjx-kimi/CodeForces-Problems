## Description

<div><p><span class="tex-font-style-it">This is an interactive problem. If you are unsure how interactive problems work, then it is recommended to read <a href="https://codeforces.com/blog/entry/45307">the guide for participants</a>.</span></p><p>Before the last stage of the exam, the director conducted an interview. He gave Gon $n$ piles of stones, the $i$-th pile having $a_i$ stones.</p><p>Each stone is identical and weighs $1$ grams, except for one special stone that is part of an unknown pile and weighs $2$ grams.</p><center> <img class="tex-graphics" src="file://KtXLnXLX.png" style="max-width: 100.0%;max-height: 100.0%;"> <span class="tex-font-size-small">A picture of the first test case. Pile $2$ has the special stone. The piles have weights of $1,3,3,4,5$, respectively.</span> </center><p>Gon can only ask the director questions of one kind: he can choose $k$ piles, and the director will tell him the total weight of the piles chosen. More formally, Gon can choose an integer $k$ ($1 \leq k \leq n$) and $k$ unique piles $p_1, p_2, \dots, p_k$ ($1 \leq p_i \leq n$), and the director will return the total weight $m_{p_1} + m_{p_2} + \dots + m_{p_k}$, where $m_i$ denotes the weight of pile $i$. </p><p>Gon is tasked with finding the pile that contains the special stone. However, the director is busy. Help Gon find this pile in at most $\mathbf{30}$ queries.</p></div><div class="input-specification"><p>The input data contains several test cases. The first line contains one integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 2 \cdot 10^5$)&nbsp;— the number of piles.</p><p>The second line of each test case contains $n$ integers $a_i$ ($1 \leq a_i \leq 10^4$)&nbsp;— the number of stones in each pile.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p><p>After reading the input for each test case, proceed with the interaction as follows.</p></div><div><h2>Interaction</h2><p>You can perform the operation at most $\mathbf{30}$ times to guess the pile. </p><p>To make a guess, print a line with the following format: </p><ul> <li> $\texttt{?}\ k \ p_1 \ p_2 \ p_3 \ ... \ p_{k-1}\ p_k$ ($1 \leq k \leq n$; $1 \leq p_i \leq n$; all $p_i$ are distinct)&nbsp;— the indices of the piles.</li></ul> After each operation, you should read a line containing a single integer $x$&nbsp;— the sum of weights of the chosen piles. (Formally, $x = m_{p_1} + m_{p_2} + \dots + m_{p_k}$.)<p>When you know the index of the pile with the special stone, print one line in the following format: $\texttt{!}\ m$ ($1 \leq m \leq n$).</p><p>After that, move on to the next test case, or terminate the program if there are no more test cases remaining.</p><p>If your program performs more than $30$ operations for one test case or makes an invalid query, you may receive a <span class="tex-font-style-tt">Wrong Answer</span> verdict.</p><p>After you print a query or the answer, please remember to output the end of the line and flush the output. Otherwise, you may get <span class="tex-font-style-tt">Idleness limit exceeded</span> or some other verdict. To do this, use the following: </p><ul> <li> <span class="tex-font-style-tt">fflush(stdout)</span> or <span class="tex-font-style-tt">cout.flush()</span> in C++; </li><li> <span class="tex-font-style-tt">System.out.flush()</span> in Java; </li><li> <span class="tex-font-style-tt">flush(output)</span> in Pascal; </li><li> <span class="tex-font-style-tt">stdout.flush()</span> in Python; </li><li> see the documentation for other languages. </li></ul><p>It is additionally recommended to read the <a href="https://codeforces.com/blog/entry/45307">interactive problems guide for participants</a>.</p><p><span class="tex-font-style-bf">Hacks</span></p><p>To make a hack, use the following format.</p><p>The first line should contain a single integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases.</p><p>The first line of each test case should contain two integers $n, m$ ($1 \leq n \leq 2 \cdot 10^5$)&nbsp;– the number of piles and the pile with the special stone.</p><p>The second line of each test case should contain $n$ integers $a_i$ ($1 \leq a_i \leq 10^4$)&nbsp;— the number of stones in each pile.</p><p>Note that the interactor is <span class="tex-font-style-bf">not</span> adaptive, meaning that the answer is known before the participant asks the queries and doesn't depend on the queries asked by the participant.</p></div>

## Input

<p>The input data contains several test cases. The first line contains one integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 2 \cdot 10^5$)&nbsp;— the number of piles.</p><p>The second line of each test case contains $n$ integers $a_i$ ($1 \leq a_i \leq 10^4$)&nbsp;— the number of stones in each pile.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p><p>After reading the input for each test case, proceed with the interaction as follows.</p>





```input1
2
5
1 2 3 4 5

11

6

3

7
1 2 3 5 3 4 2

12

6
```




```output1
? 4 1 2 3 4

? 2 2 3

? 1 2

! 2

? 4 2 3 5 6

? 2 1 4

! 7
```



## Note

<p>In the first test case, the stone with weight two is located in pile $2$, as shown in the picture. We perform the following interaction: </p><ul> <li> $\texttt{? 4 1 2 3 4}$&nbsp;— ask the total weight of piles $1$, $2$, $3$, and $4$. The total weight we receive back is $1+3+3+4=11$. </li><li> $\texttt{? 2 2 3}$&nbsp;— ask the total weight of piles $2$ and $3$. The total weight we receive back is $3+3=6$. </li><li> $\texttt{? 1 2}$&nbsp;— ask the total weight of pile $2$. The total weight we receive back is $3$. </li><li> $\texttt{! 2}$&nbsp;— we have figured out that pile $2$ contains the special stone, so we output it and move on to the next test case. </li></ul><p>In the second test case, the stone with weight two is located on index $7$. We perform the following interaction: </p><ul> <li> $\texttt{? 4 2 3 5 6}$&nbsp;— ask the total weight of piles $2$, $3$, $5$, and $6$. The total weight we receive back is $2+3+3+4=12$. </li><li> $\texttt{? 2 1 4}$&nbsp;— ask the total weight of piles $1$ and $4$. The total weight we receive back is $1+5=6$. </li><li> $\texttt{! 7}$&nbsp;— we have somehow figured out that pile $7$ contains the special stone, so we output it and end the interaction. </li></ul>
