## Description

<div><p>Dasha, an excellent student, is studying at the best mathematical lyceum in the country. Recently, a mysterious stranger brought $n$ words consisting of small latin letters $s_1, s_2, \ldots, s_n$ to the lyceum. Since that day, Dasha has been tormented by <span class="tex-font-style-it">nightmares</span>.</p><p>Consider some pair of integers $\langle i, j \rangle$ ($1 \le i \le j \le n$). <span class="tex-font-style-it">A nightmare</span> is a string for which it is true:</p><ul> <li> It is obtained by concatenation $s_{i}s_{j}$; </li><li> Its length is <span class="tex-font-style-bf">odd</span>; </li><li> The number of different letters in it is <span class="tex-font-style-bf">exactly</span> $25$; </li><li> The number of occurrences of each letter that is in the word is <span class="tex-font-style-bf">odd</span>. </li></ul><p>For example, if $s_i=$ "abcdefg" and $s_j=$ "ijklmnopqrstuvwxyz", the pair $\langle i, j \rangle$ creates a <span class="tex-font-style-it">nightmare</span>.</p><p>Dasha will stop having <span class="tex-font-style-it">nightmares</span> if she counts their number. There are too many <span class="tex-font-style-it">nightmares</span>, so Dasha needs your help. Count the number of different <span class="tex-font-style-it">nightmares</span>.</p><p><span class="tex-font-style-it">Nightmares</span> are called different if the corresponding pairs $\langle i, j \rangle$ are different. The pairs $\langle i_1, j_1 \rangle$ and $\langle i_2, j_2 \rangle$ are called different if $i_1 \neq i_2$ <span class="tex-font-style-bf">or</span> $j_1 \neq j_2$.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of words.</p><p>The following $n$ lines contain the words $s_1, s_2, \ldots, s_n$, consisting of small latin letters.</p><p>It is guaranteed that the total length of words does not exceed $5 \cdot 10^6$.</p></div><div class="output-specification"><p>Print a single integer&nbsp;— the number of different <span class="tex-font-style-it">nightmares</span>.</p></div>

## Input

<p>The first line contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of words.</p><p>The following $n$ lines contain the words $s_1, s_2, \ldots, s_n$, consisting of small latin letters.</p><p>It is guaranteed that the total length of words does not exceed $5 \cdot 10^6$.</p>

## Output

<p>Print a single integer&nbsp;— the number of different <span class="tex-font-style-it">nightmares</span>.</p>





```input1|
10
ftl
abcdefghijklmnopqrstuvwxy
abcdeffghijkllmnopqrsttuvwxy
ffftl
aabbccddeeffgghhiijjkkllmmnnooppqqrrssttuuvvwwxxyy
thedevid
bcdefghhiiiijklmnopqrsuwxyz
gorillasilverback
abcdefg
ijklmnopqrstuvwxyz
```




```output1
5
```



## Note

<p>In the first test, <span class="tex-font-style-it">nightmares</span> are created by pairs $\langle 1, 3 \rangle$, $\langle 2, 5 \rangle$, $\langle 3, 4 \rangle$, $\langle 6, 7 \rangle$, $\langle 9, 10 \rangle$.</p>
