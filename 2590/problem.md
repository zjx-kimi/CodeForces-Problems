## Description

<div><div class="epigraph"><div class="epigraph-text"> <span class="tex-font-style-it">Whoso in ignorance draws near to them and hears the Sirens' voice, he nevermore returns.</span><p>Homer, <span class="tex-font-style-it">Odyssey</span></p></div></div><p>In the times of Jason and the Argonauts, it was well known that sirens use the sound of their songs to lure sailors into their demise. Yet only a few knew that every time sirens call a sailor by his name, his will weakens, making him more vulnerable. </p><p>For the purpose of this problem, both siren songs and names of the sailors will be represented as strings of lowercase English letters. The more times the sailor's name occurs as a contiguous substring of the song, the greater danger he is in.</p><p>Jason found out that sirens can sing one of the $n+1$ songs, which have the following structure: let $s_i$ ($0 \leq i \leq n$) be the $i$-th song and $t$ be a string of length $n$, then for every $i &lt; n$: $s_{i+1} = s_i t_i s_i$. In other words $i+1$-st song is the concatenation of $i$-th song, $i$-th letter ($0$-indexed) of $t$ and the $i$-th song. </p><p>Fortunately, he also knows $s_0$ and $t$. Jason wonders how many times a sailor's name is mentioned in a particular song. Answer $q$ queries: given the sailor's name ($w$) and the index of a song ($i$) output the number of occurrences of $w$ in $s_i$ as a substring. As this number can be quite large, output its remainder modulo $10^9+7$.</p></div><div class="input-specification"><p>In the first line of input there are two integers $n$, $q$ ( $ 1 \leq n, q \leq 10^5$) meaning that there are $n+1$ songs and $q$ queries. In the next two lines strings $s_0$ and $t$ follow ($1 \leq |s_0| \leq 100, |t| = n$). </p><p>Next $q$ lines describe the queries; each one contains an integer $k$ ($ 0 \leq k \leq n$), the index of the song sung by the sirens, and a non-empty string $w$, which is the name of a sailor. All strings in this problem consist only of lowercase English letters, and the sum of lengths of sailors' names does not exceed $10^6$.</p></div><div class="output-specification"><p>Output $q$ lines, $i$-th of them should contain the remainder modulo $10^9+7$ of the number of occurrences of $w$ in $s_k$.</p></div>

## Input

<p>In the first line of input there are two integers $n$, $q$ ( $ 1 \leq n, q \leq 10^5$) meaning that there are $n+1$ songs and $q$ queries. In the next two lines strings $s_0$ and $t$ follow ($1 \leq |s_0| \leq 100, |t| = n$). </p><p>Next $q$ lines describe the queries; each one contains an integer $k$ ($ 0 \leq k \leq n$), the index of the song sung by the sirens, and a non-empty string $w$, which is the name of a sailor. All strings in this problem consist only of lowercase English letters, and the sum of lengths of sailors' names does not exceed $10^6$.</p>

## Output

<p>Output $q$ lines, $i$-th of them should contain the remainder modulo $10^9+7$ of the number of occurrences of $w$ in $s_k$.</p>





```input1
3 3
aa
bcd
2 aba
3 ca
3 aa
```




```input2
4 5
aba
bbac
1 a
3 baca
3 ab
2 bab
4 aba
```




```output1
2
2
8
```




```output2
4
0
14
6
28
```



## Note

<p>In the first example songs of the sirens are as follows: </p><ul> <li> Song $0$: <span class="tex-font-style-tt">aa</span> </li><li> Song $1$: <span class="tex-font-style-tt">aabaa</span> </li><li> Song $2$: <span class="tex-font-style-tt">aabaacaabaa</span> </li><li> Song $3$: <span class="tex-font-style-tt">aabaacaabaadaabaacaabaa</span> </li></ul>
