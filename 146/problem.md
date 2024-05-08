## Description

<div><p>You meet two new friends who are twins. The name of the elder twin is $A$, which consists of $N$ characters. While the name of the younger twin is $B$, which consists of $M$ characters. It is known that $N \leq M$.</p><p>You want to call each of them with a nickname. For the elder twin, you want to pick any permutation of $A$ as the nickname. For the younger twin, you want to remove exactly $M - N$ characters from any permutation of $B$. Denote the nicknames of the elder twin and the younger twin as $A'$ and $B'$, respectively.</p><p>You want the nicknames to satisfy the following requirement. For each $i$ that satisfies $1 \leq i \leq N$, $B'_i$ must be equal to either $A'_i$ or the next letter that follows alphabetically after $A'_i$ (if such a next letter exists).</p><p>Determine the number of different pairs of nicknames $(A', B')$ that satisfy the requirement. Two pairs of nicknames are considered different if at least one of the nicknames are different. As the result might be large, find the answer modulo $998\,244\,353$.</p></div><div class="input-specification"><p>The first line consists of two integers $N$ $M$ ($1 \leq N \leq M \leq 200\,000$).</p><p>The second line consists of a string $A$ of length $N$.</p><p>The third line consists of a string $B$ of length $M$.</p><p>All strings consist of only upper-case letters.</p></div><div class="output-specification"><p>Output a single integer representing number of different pairs $(A', B')$ that satisfy the requirement, modulo $998\,244\,353$.</p></div>

## Input

<p>The first line consists of two integers $N$ $M$ ($1 \leq N \leq M \leq 200\,000$).</p><p>The second line consists of a string $A$ of length $N$.</p><p>The third line consists of a string $B$ of length $M$.</p><p>All strings consist of only upper-case letters.</p>

## Output

<p>Output a single integer representing number of different pairs $(A', B')$ that satisfy the requirement, modulo $998\,244\,353$.</p>





```input1
3 4
AMA
ANAB
```




```input2
5 8
BINUS
BINANUSA
```




```input3
15 30
BINUSUNIVERSITY
BINANUSANTARAUNIVERSITYJAKARTA
```




```input4
4 4
UDIN
ASEP
```




```output1
9
```




```output2
120
```




```output3
151362308
```




```output4
0
```



## Note

<p><span class="tex-font-style-it">Explanation for the sample input/output #1</span></p><p>The $9$ pairs are:</p><ul> <li> (<span class="tex-font-style-tt">AAM</span>, <span class="tex-font-style-tt">AAN</span>), </li><li> (<span class="tex-font-style-tt">AAM</span>, <span class="tex-font-style-tt">ABN</span>), </li><li> (<span class="tex-font-style-tt">AAM</span>, <span class="tex-font-style-tt">BAN</span>), </li><li> (<span class="tex-font-style-tt">AMA</span>, <span class="tex-font-style-tt">ANA</span>), </li><li> (<span class="tex-font-style-tt">AMA</span>, <span class="tex-font-style-tt">ANB</span>), </li><li> (<span class="tex-font-style-tt">AMA</span>, <span class="tex-font-style-tt">BNA</span>), </li><li> (<span class="tex-font-style-tt">MAA</span>, <span class="tex-font-style-tt">NAA</span>), </li><li> (<span class="tex-font-style-tt">MAA</span>, <span class="tex-font-style-tt">NAB</span>), and </li><li> (<span class="tex-font-style-tt">MAA</span>, <span class="tex-font-style-tt">NBA</span>). </li></ul><p><span class="tex-font-style-it">Explanation for the sample input/output #2</span></p><p>The $120$ pairs are the pairs where $A'$ is a permutation of <span class="tex-font-style-tt">BINUS</span> and $B' = A'$.</p>
