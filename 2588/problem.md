## Description

<div><div class="epigraph"><div class="epigraph-text"><span class="tex-font-style-it">What walks on four feet in the morning, two in the afternoon, and three at night?</span></div></div><p><span class="tex-font-style-it">This is an interactive problem. This problem doesn't support hacks.</span></p><p>Sphinx's duty is to guard the city of Thebes by making sure that no unworthy traveler crosses its gates. Only the ones who answer her riddle timely and correctly (or get an acc for short) are allowed to pass. As of those who fail, no one heard of them ever again...</p><p>So you don't have a choice but to solve the riddle. Sphinx has an array $a_1, a_2, \ldots, a_n$ of <span class="tex-font-style-bf">nonnegative</span> integers <span class="tex-font-style-bf">strictly smaller</span> than $2^b$ and asked you to find the maximum value among its elements. Of course, she will not show you the array, but she will give you $n$ and $b$. As it is impossible to answer this riddle blindly, you can ask her some questions. For given $i, y$, she'll answer you whether $a_i$ is <span class="tex-font-style-bf">bigger</span> than $y$. As sphinxes are not very patient, you can ask at most $3 \cdot (n + b) $ such questions.</p><p>Although cunning, sphinxes are honest. Even though the array <span class="tex-font-style-bf">can change</span> between your queries, answers to the previously asked questions will remain valid.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $b$ ($1 \leq n, b \leq 200$). The remaining parts of the input will be given throughout the interaction process.</p></div><div><h2>Interaction</h2><p>In each round your program must output a single line with an integer $i$ ($0 \leq i \leq n$) and a binary string of length <span class="tex-font-style-bf">exactly</span> $b$ denoting the <span class="tex-font-style-bf">binary representation</span> of $y$ (most significant bit first).</p><p>If $i &gt; 0$, this line encodes the question: <span class="tex-font-style-it">Is $a_i$ bigger than $y$?</span>. There should be at most $3 \cdot (n+b)$ such lines; after each of them, the interactor will print <span class="tex-font-style-tt">yes</span> or <span class="tex-font-style-tt">no</span> in a single line.</p><p>If $i = 0$, this is the last round of interaction, after which your program should terminate, and $y$ should be the maximal value among the elements of Sphinx's array. Note that this round <span class="tex-font-style-bf">does not</span> count to the query limit.</p><p>Note that the interactor <span class="tex-font-style-bf">is adaptive</span>.</p><p>After printing a query, do not forget to output the end of the line and flush the output. Otherwise, you will get <span class="tex-font-style-tt">Idleness limit exceeded</span>. To do this, use:</p><ul><p> </p><li> <span class="tex-font-style-tt">fflush(stdout)</span> or <span class="tex-font-style-tt">cout.flush()</span> in C++; </li><li> <span class="tex-font-style-tt">System.out.flush()</span> in Java; </li><li> <span class="tex-font-style-tt">flush(output)</span> in Pascal; </li><li> <span class="tex-font-style-tt">stdout.flush()</span> in Python; </li><li> see the documentation for other languages.</li></ul><p>If your solution does not correctly follow the interaction guideline above, it may receive an arbitrary verdict. Otherwise, your program will receive the <span class="tex-font-style-tt">Wrong Answer</span> judgment if it reports the wrong maximum.</p></div>

## Input

<p>The first line contains two integers $n$ and $b$ ($1 \leq n, b \leq 200$). The remaining parts of the input will be given throughout the interaction process.</p>





```input1
5 3

yes

no

no

no

no

yes
```




```input2
4 3

no

no

no

no
```




```input3
1 1
```




```output1
5 101

5 110

4 100

3 101

2 001

1 000

0 110
```




```output2
1 000

2 000

3 000

4 000

0 000
```




```output3
0 0
```



## Note

<p>In all examples, the sequence is <span class="tex-font-style-bf">fixed</span> beforehand.</p><p>In the first example, the sequence is $2, 1, 4, 0, 6$.</p><p>In the second example, the sequence is $0, 0, 0, 0$.</p><p>In the third example, the sequence is $0$.</p><p>Note that if the interactor was adaptive, then the interaction in the first and the third example would not be sufficient to return the correct value of maximum.</p>
