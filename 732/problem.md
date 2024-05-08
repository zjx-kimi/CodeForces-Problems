## Description

<div> Philip is very fond of tasks on the lines. He had already solved all the problems known to him, but this was not enough for him. Therefore, Philip decided to come up with his own task.<p>To do this, he took the string $t$ and a set of $n$ strings $s_1$, $s_2$, $s_3$, ..., $s_n$. Philip has $m$ queries, in the $i$th of them, Philip wants to take a substring of the string $t$ from $l_i$th to $r_i$th character, and count the number of its substrings that match some string from the set. More formally, Philip wants to count the number of pairs of positions $a$, $b$, such that $l_i \le a \le b \le r_i$, and the substring of the string $t$ from $a$th to $b$th character coincides with some string $s_j$ from the set.</p><p>A substring of the string $t$ from $a$th to $b$th character is a string obtained from $t$ by removing the $a - 1$ character from the beginning and $|t| - b$ characters from the end, where $|t|$ denotes the length of the string $t$.</p><p>Philip has already solved this problem, but can you? </p></div><div class="input-specification"><p>The first line contains two positive integers $n$ and $m$ ($1 \le n, m \le 500\,000$)&nbsp;— the number of rows in the set and the number of queries.</p><p>The second line contains a single string $t$ consisting of lowercase letters of the English alphabet ($1 \le |t| \le 5 \cdot 10^6$).</p><p>The following $n$ lines describe the strings from the set. In the $i$th of them, a single string $s_i$ is given, consisting of lowercase letters of the English alphabet. Denote by $S$ the total length of all strings from the set. It is guaranteed that $S \le 10^6$, as well as that all strings of $s_i$ are different.</p><p>In the following lines, queries are entered. The $i$th of them contains two positive integers $l_i$ and $r_i$ ($1 \le l_i \le r_i \le |t|$)&nbsp;— the left and right border of the substring $t$ from the $i$-th query. </p></div><div class="output-specification"><p>In a single line, print $m$ integers, $i$th of them should be equal to the answers to the $i$th query. </p></div>

## Input

<p>The first line contains two positive integers $n$ and $m$ ($1 \le n, m \le 500\,000$)&nbsp;— the number of rows in the set and the number of queries.</p><p>The second line contains a single string $t$ consisting of lowercase letters of the English alphabet ($1 \le |t| \le 5 \cdot 10^6$).</p><p>The following $n$ lines describe the strings from the set. In the $i$th of them, a single string $s_i$ is given, consisting of lowercase letters of the English alphabet. Denote by $S$ the total length of all strings from the set. It is guaranteed that $S \le 10^6$, as well as that all strings of $s_i$ are different.</p><p>In the following lines, queries are entered. The $i$th of them contains two positive integers $l_i$ and $r_i$ ($1 \le l_i \le r_i \le |t|$)&nbsp;— the left and right border of the substring $t$ from the $i$-th query. </p>

## Output

<p>In a single line, print $m$ integers, $i$th of them should be equal to the answers to the $i$th query. </p>





```input1
3 5
abacaba
aba
a
ac
1 7
1 3
2 7
2 5
4 5
```




```input2
4 4
abcdca
ab
ca
bcd
openolympiad
1 5
2 2
2 6
1 6
```




```output1
7 3 5 3 1
```




```output2
2 0 2 3
```



## Note

<p>In the first example, the first query requires the entire string to count the number of substrings that are included in the set. The substrings $[1, 3]$ and $[4, 6]$ coincide with the string "aba". The substrings match with the string "a" $[1, 1]$, $[3, 3]$, $[5, 5]$, $[7, 7]$. The substring $[3, 4]$ matches the string "ac". In total, it turns out that 7 substrings of the string "abacaba" match the strings from the set.</p><p>In the second query, a substring from position 1 to position 3 is taken from the source string, this is the string "aba". The string "aba" enters it 1 time, the string "a" enters it 2 times and the string "ac" does not enter it once as a substring.  In the third query, a substring from the 2nd to the 7th position is taken from the source string, this is the string "bacaba". The string "aba" is included in it 1 time, the string "a" is included 3 times and the string "ac" is included 1 time as a substring. </p>
