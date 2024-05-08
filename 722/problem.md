## Description

<div><p>Lara has a safe that is locked with a circle-shaped code lock that consists of a rotating arrow, a static circumference around the arrow, an input screen, and an input button.</p><p>The circumference of the lock is split into $k$ equal sections numbered from $1$ to $k$ in clockwise order. Arrow always points to one of the sections. Each section is marked with one of the first $k$ letters of the English alphabet. No two sections are marked with the same letter.</p><p>Due to the lock limitations, the safe's password is a string of length $n$ that consists of first $k$ letters of the English alphabet only. Lara enters the password by rotating the lock's arrow and pressing the input button. Initially, the lock's arrow points to section $1$ and the input screen is empty. In one second she can do one of the following actions. </p><ul> <li> Rotate the arrow one section clockwise. If the arrow was pointing at section $x &lt; k$ it will now point at section $x + 1$. If the arrow was pointing at section $k$ it will now point at section $1$. </li><li> Rotate the arrow one section counter-clockwise. If the arrow was pointing at section $x &gt; 1$ it will now point at section $x - 1$. If the arrow was pointing at section $1$ it will now point at section $k$. </li><li> Press the input button. The letter marked on the section that the arrow points to will be added to the content of the input screen. </li></ul> As soon as the content of the input screen matches the password, the safe will open. Lara always enters her password in the minimum possible time.<p>Lara has recently found out that the safe can be re-programmed. She can take the first $k$ letters of the English alphabet and assign them to the sectors in any order she likes. Now she wants to re-arrange the letters in a way that will minimize the number of seconds it takes her to input the password. Compute this minimum number of seconds and the number of ways to assign letters, for which this minimum number of seconds is achieved.</p><p>Two ways to assign letters to sectors are considered to be distinct if there exists at least one sector $i$ that is assigned different letters.</p></div><div class="input-specification"><p>The first line of the input contains two integers $k$ and $n$ ($2 \leq k \leq 16$, $2 \leq n \leq 100\,000$)&nbsp;— the number of sectors on the lock's circumference and the length of Lara's password, respectively.</p><p>The second line of the input contains a string of length $n$ that consists of the first $k$ lowercase letters of the English alphabet only. This string is the password.</p></div><div class="output-specification"><p>On the first line print minimum possible number of seconds it can take Lara to enter the password and open the safe if she assigns letters to sectors optimally.</p><p>On the second line print the number of ways to assign letters optimally.</p></div>

## Input

<p>The first line of the input contains two integers $k$ and $n$ ($2 \leq k \leq 16$, $2 \leq n \leq 100\,000$)&nbsp;— the number of sectors on the lock's circumference and the length of Lara's password, respectively.</p><p>The second line of the input contains a string of length $n$ that consists of the first $k$ lowercase letters of the English alphabet only. This string is the password.</p>

## Output

<p>On the first line print minimum possible number of seconds it can take Lara to enter the password and open the safe if she assigns letters to sectors optimally.</p><p>On the second line print the number of ways to assign letters optimally.</p>





```input1
3 10
abcabcabca
```




```input2
4 20
bcbcbcbcadadadadcbda
```




```input3
4 6
adcbda
```




```output1
19
2
```




```output2
40
2
```




```output3
12
4
```



## Note

<p>The initial states of optimal arrangements for the first example are shown in the figure below.</p><center> <img class="tex-graphics" src="file://05aEU7VC.png" style="max-width: 100.0%;max-height: 100.0%;" width="189px"> </center><p>The initial states of optimal arrangements for the second example are shown in the figure below.</p><center> <img class="tex-graphics" src="file://NQipWjGu.png" style="max-width: 100.0%;max-height: 100.0%;" width="189px"> </center><p>The initial states of optimal arrangements for the third example are shown in the figure below.</p><center> <img class="tex-graphics" src="file://H0FsgQH6.png" style="max-width: 100.0%;max-height: 100.0%;" width="416px"> </center>
