## Description

<div><p><span class="tex-font-style-bf">This is a complex version of the problem. This version has no additional restrictions on the number $k$.</span></p><p>The chief wizard of the Wizengamot once caught the evil wizard Drahyrt, but the evil wizard has returned and wants revenge on the chief wizard. So he stole <span class="tex-font-style-it">spell</span> $s$ from his student Harry.</p><p>The <span class="tex-font-style-it">spell</span>&nbsp;— is a $n$-length string of lowercase Latin letters.</p><p>Drahyrt wants to replace <span class="tex-font-style-it">spell</span> with an unforgivable curse&nbsp;— string $t$.</p><p>Dragirt, using ancient magic, can swap letters at a distance $k$ or $k+1$ in <span class="tex-font-style-it">spell</span> as many times as he wants. In other words, Drahyrt can change letters in positions $i$ and $j$ in <span class="tex-font-style-it">spell</span> $s$ if $|i-j|=k$ or $|i-j|=k+1$.</p><p>For example, if $k = 3, s = $ "<span class="tex-font-style-tt">talant</span>" and $t = $ "<span class="tex-font-style-tt">atltna</span>", Drahyrt can act as follows:</p><ul> <li> swap the letters at positions $1$ and $4$ to get <span class="tex-font-style-it">spell</span> "<span class="tex-font-style-tt">aaltnt</span>". </li><li> swap the letters at positions $2$ and $6$ to get <span class="tex-font-style-it">spell</span> "<span class="tex-font-style-tt">atltna</span>". </li></ul><p>You are given <span class="tex-font-style-it">spells</span> $s$ and $t$. Can Drahyrt change <span class="tex-font-style-it">spell</span> $s$ to $t$?</p></div><div class="input-specification"><p>The first line of input gives a single integer $T$ ($1 \le T \le 10^4$)&nbsp;— the number of test cases in the test.</p><p>Descriptions of the test cases are follow.</p><p>The first line contains two integers $n, k$ ($1 \le n \le 2 \cdot 10^5$, $1 \le k \le 2 \cdot 10^5$)&nbsp;— the length <span class="tex-font-style-it">spells</span> and the number $k$ such that Drahyrt can change letters in a spell at a distance $k$ or $k+1$.</p><p>The second line gives <span class="tex-font-style-it">spell</span> $s$&nbsp;— a string of length $n$ consisting of lowercase Latin letters.</p><p>The third line gives <span class="tex-font-style-it">spell</span> $t$&nbsp;— a string of length $n$ consisting of lowercase Latin letters.</p><p>It is guaranteed that the sum of $n$ values over all test cases does not exceed $2 \cdot 10^5$. Note that there is no limit on the sum of $k$ values over all test cases.</p></div><div class="output-specification"><p>For each test case, output on a separate line "<span class="tex-font-style-tt">YES</span>" if Drahyrt can change <span class="tex-font-style-it">spell</span> $s$ to $t$ and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, lines "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive answer).</p></div>

## Input

<p>The first line of input gives a single integer $T$ ($1 \le T \le 10^4$)&nbsp;— the number of test cases in the test.</p><p>Descriptions of the test cases are follow.</p><p>The first line contains two integers $n, k$ ($1 \le n \le 2 \cdot 10^5$, $1 \le k \le 2 \cdot 10^5$)&nbsp;— the length <span class="tex-font-style-it">spells</span> and the number $k$ such that Drahyrt can change letters in a spell at a distance $k$ or $k+1$.</p><p>The second line gives <span class="tex-font-style-it">spell</span> $s$&nbsp;— a string of length $n$ consisting of lowercase Latin letters.</p><p>The third line gives <span class="tex-font-style-it">spell</span> $t$&nbsp;— a string of length $n$ consisting of lowercase Latin letters.</p><p>It is guaranteed that the sum of $n$ values over all test cases does not exceed $2 \cdot 10^5$. Note that there is no limit on the sum of $k$ values over all test cases.</p>

## Output

<p>For each test case, output on a separate line "<span class="tex-font-style-tt">YES</span>" if Drahyrt can change <span class="tex-font-style-it">spell</span> $s$ to $t$ and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, lines "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive answer).</p>





```input1|2,3,4,8,9,10,14,15,16,20,21,22
7
6 3
talant
atltna
7 1
abacaba
aaaabbc
12 6
abracadabraa
avadakedavra
5 3
accio
cicao
5 4
lumos
molus
4 3
uwjt
twju
4 3
kvpx
vxpk
```




```output1
YES
YES
NO
YES
NO
YES
NO
```



## Note

<p>The first case is explained in the condition.</p><p>In the second case, we can swap adjacent letters, so we can sort the string using bubble sorting, for example.</p><p>In the third case, we can show that from the string $s$ we cannot get the string $t$ by swapping letters at a distance of $6$ or $7$.</p><p>In the fourth case, for example, the following sequence of transformations is appropriate:</p><ul> <li> "<span class="tex-font-style-tt">accio</span>" $\rightarrow$ "<span class="tex-font-style-tt">aocic</span>" $\rightarrow$ "<span class="tex-font-style-tt">cocia</span>" $\rightarrow$ "<span class="tex-font-style-tt">iocca</span>" $\rightarrow$ "<span class="tex-font-style-tt">aocci</span>" $\rightarrow$ "<span class="tex-font-style-tt">aicco</span>" $\rightarrow$ "<span class="tex-font-style-tt">cicao</span>" </li></ul><p>In the fifth case, we can show that it is impossible to get the string $s$ from the string $t$.</p><p>In the sixth example, it is enough to swap the two outermost letters.</p>
