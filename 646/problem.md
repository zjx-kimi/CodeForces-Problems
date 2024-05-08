## Description

<div><p>There is a toy machine with toys arranged in two rows of $n$ cells each ($n$ is odd).</p><center> <img class="tex-graphics" src="file://bsy7AT9U.png" style="max-width: 100.0%;max-height: 100.0%;" width="567px"> <span class="tex-font-style-it">Initial state for $n=9$.</span> </center><p>Initially, $n-2$ toys are placed in the non-corner cells of the top row. The bottom row is initially empty, and its leftmost, rightmost, and central cells are blocked. There are $4$ buttons to control the toy machine: left, right, up, and down marked by the letters <span class="tex-font-style-tt">L</span>, <span class="tex-font-style-tt">R</span>, <span class="tex-font-style-tt">U</span>, and <span class="tex-font-style-tt">D</span> correspondingly.</p><p>When pressing <span class="tex-font-style-tt">L</span>, <span class="tex-font-style-tt">R</span>, <span class="tex-font-style-tt">U</span>, or <span class="tex-font-style-tt">D</span>, all the toys will be moved simultaneously in the corresponding direction and will only stop if they push into another toy, the wall or a blocked cell. Your goal is to move the $k$-th toy into the leftmost cell of the top row. The toys are numbered from $1$ to $n-2$ from left to right. Given $n$ and $k$, find a solution that uses at most $1\,000\,000$ button presses.</p><p>To test out the toy machine, a <a href="https://assets.codeforces.com/files/56ff21637146a30d/game.html"><span class="tex-font-style-bf">web page</span></a> is available that lets you play the game in real time. </p></div><div class="input-specification"><p>The first and only line contains two integers, $n$ and $k$ ($5 \le n \le 100\,000$, $n$ is odd, $1 \le k \le n-2$)&nbsp;— the number of cells in a row, and the index of the toy that has to be moved to the leftmost cell of the top row.</p></div><div class="output-specification"><p>On a single line, output a description of the button presses as a string of at most $1\,000\,000$ characters. The string should only contain the characters <span class="tex-font-style-tt">L</span>, <span class="tex-font-style-tt">R</span>, <span class="tex-font-style-tt">U</span>, and <span class="tex-font-style-tt">D</span>. The $i$-th character in the string is the $i$-th button that is pressed. After all the button presses are performed, the $k$-th toy should be in the leftmost cell of the top row.</p><p>If there are multiple solutions, print any. The number of button presses does not have to be minimized.</p></div>

## Input

<p>The first and only line contains two integers, $n$ and $k$ ($5 \le n \le 100\,000$, $n$ is odd, $1 \le k \le n-2$)&nbsp;— the number of cells in a row, and the index of the toy that has to be moved to the leftmost cell of the top row.</p>

## Output

<p>On a single line, output a description of the button presses as a string of at most $1\,000\,000$ characters. The string should only contain the characters <span class="tex-font-style-tt">L</span>, <span class="tex-font-style-tt">R</span>, <span class="tex-font-style-tt">U</span>, and <span class="tex-font-style-tt">D</span>. The $i$-th character in the string is the $i$-th button that is pressed. After all the button presses are performed, the $k$-th toy should be in the leftmost cell of the top row.</p><p>If there are multiple solutions, print any. The number of button presses does not have to be minimized.</p>





```input1
5 1
```




```input2
7 2
```




```output1
RDL
```




```output2
RDL
```



## Note

<p>In the first example, there will be $5-2 = 3$ toys. The first toy needs to end up in the leftmost cell of the top row. The moves <span class="tex-font-style-tt">RDL</span> will achieve this, see the picture for a better understanding. Another possible solution would be to do one button press <span class="tex-font-style-tt">L</span>.</p><center> <img class="tex-graphics" src="file://tygdrfIt.png" style="max-width: 100.0%;max-height: 100.0%;" width="567px"> <span class="tex-font-style-it">Visualization of the moves for the first example.</span> </center>
