## Description

<div><p>Kristina has a matrix of size $n$ by $n$, filled with lowercase Latin letters. The value of $n$ is <span class="tex-font-style-bf">even</span>.</p><p>She wants to change some characters so that her matrix becomes a <span class="tex-font-style-it">perfect square</span>. A matrix is called a <span class="tex-font-style-it">perfect square</span> if it remains unchanged when rotated $90^\circ$ clockwise <span class="tex-font-style-bf">once</span>.</p><p>Here is an example of rotating a matrix by $90^\circ$:</p><center> <img class="tex-graphics" src="file://7XvgtrHW.png" style="max-width: 100.0%;max-height: 100.0%;">   </center><p>In one operation, Kristina can choose any cell and replace its value with the next character in the alphabet. If the character is equal to "<span class="tex-font-style-tt">z</span>", its value <span class="tex-font-style-bf">does not change</span>.</p><p>Find the <span class="tex-font-style-bf">minimum</span> number of operations required to make the matrix a <span class="tex-font-style-it">perfect square</span>.</p><p>For example, if the $4$ by $4$ matrix looks like this:</p><p>$$\matrix{ a &amp; b &amp; b &amp; a \cr b &amp; c &amp; \textbf{b} &amp; b \cr b &amp; c &amp; c &amp; b\cr a &amp; b &amp; b &amp; a \cr }$$</p><p>then it is enough to apply $1$ operation to the letter <span class="tex-font-style-bf">b</span>, highlighted in bold.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^2$)&nbsp;— the number of test cases.</p><p>Then follows the description of each test case.</p><p>The first line of each test case contains a single <span class="tex-font-style-bf">even</span> integer $n$ ($2 \le n \le 10^3$)&nbsp;— the number of rows and columns in the matrix.</p><p>Then follows $n$ lines, each containing exactly $n$ lowercase Latin letters.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^3$.</p></div><div class="output-specification"><p>For each test case, output a single number on a separate line: the <span class="tex-font-style-bf">minimum</span> number of operations required for Kristina to obtain a <span class="tex-font-style-it">perfect square</span>.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^2$)&nbsp;— the number of test cases.</p><p>Then follows the description of each test case.</p><p>The first line of each test case contains a single <span class="tex-font-style-bf">even</span> integer $n$ ($2 \le n \le 10^3$)&nbsp;— the number of rows and columns in the matrix.</p><p>Then follows $n$ lines, each containing exactly $n$ lowercase Latin letters.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^3$.</p>

## Output

<p>For each test case, output a single number on a separate line: the <span class="tex-font-style-bf">minimum</span> number of operations required for Kristina to obtain a <span class="tex-font-style-it">perfect square</span>.</p>





```input1|2,3,4,5,6,10,11,12,13,14,15,16,22,23,24,25,26
5
4
abba
bcbb
bccb
abba
2
ab
ba
6
codefo
rcesco
deforc
escode
forces
codefo
4
baaa
abba
baba
baab
4
bbaa
abba
aaba
abba
```




```output1
1
2
181
5
9
```



## Note

<p>The first test case is explained in the problem statement.</p>
