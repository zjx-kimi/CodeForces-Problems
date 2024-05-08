## Description

<div><p>There is a string $s$ of length $n$ consisting of the characters '<span class="tex-font-style-tt">(</span>' and '<span class="tex-font-style-tt">)</span>'. You are walking on this string. You start by standing on top of the first character of $s$, and you want to make a sequence of moves such that you end on the $n$-th character. In one step, you can move one space to the left (if you are not standing on the first character), or one space to the right (if you are not standing on the last character). You may not stay in the same place, however you may visit any character, including the first and last character, <span class="tex-font-style-bf">any</span> number of times.</p><p>At each point in time, you write down the character you are currently standing on. We say the string is <span class="tex-font-style-it">walkable</span> if there exists some sequence of moves that take you from the first character to the last character, such that the string you write down is a regular bracket sequence.</p><p>A regular bracket sequence is a bracket sequence that can be transformed into a correct arithmetic expression by inserting characters '<span class="tex-font-style-tt">1</span>' and '<span class="tex-font-style-tt">+</span>' between the original characters of the sequence. For example, bracket sequences "<span class="tex-font-style-tt">()()</span>", "<span class="tex-font-style-tt">(())</span>" are regular (the resulting expressions are: "<span class="tex-font-style-tt">(1)+(1)</span>", "<span class="tex-font-style-tt">((1+1)+1)</span>"), and "<span class="tex-font-style-tt">)(</span>" and "<span class="tex-font-style-tt">(</span>" are not.</p><center><img class="tex-graphics" src="file://p2OFCoo5.png" style="max-width: 100.0%;max-height: 100.0%;"><span class="tex-font-size-small">One possible valid walk on $s=\mathtt{(())()))}$. The red dot indicates your current position, and the red string indicates the string you have written down. Note that the red string is a regular bracket sequence at the end of the process.</span></center><p>You are given $q$ queries. Each query flips the value of a character from '<span class="tex-font-style-tt">(</span>' to '<span class="tex-font-style-tt">)</span>' or vice versa. After each query, determine whether the string is walkable.</p><p>Queries are <span class="tex-font-style-bf">cumulative</span>, so the effects of each query carry on to future queries.</p></div><div class="input-specification"><p>The first line of the input contains two integers $n$ and $q$ ($1 \le n, q \le 2\cdot 10^5$)&nbsp;— the size of the string and the number of queries, respectively.</p><p>The second line of the input contains a string $s$ of size $n$, consisting of the characters '<span class="tex-font-style-tt">(</span>' and '<span class="tex-font-style-tt">)</span>'&nbsp;— the initial bracket string.</p><p>Each of the next $q$ lines contains a single integer $i$ ($1\le i \le n$)&nbsp;— the index of the character to flip for that query.</p></div><div class="output-specification"><p>For each query, print "<span class="tex-font-style-tt">YES</span>" if the string is walkable after that query, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p></div>

## Input

<p>The first line of the input contains two integers $n$ and $q$ ($1 \le n, q \le 2\cdot 10^5$)&nbsp;— the size of the string and the number of queries, respectively.</p><p>The second line of the input contains a string $s$ of size $n$, consisting of the characters '<span class="tex-font-style-tt">(</span>' and '<span class="tex-font-style-tt">)</span>'&nbsp;— the initial bracket string.</p><p>Each of the next $q$ lines contains a single integer $i$ ($1\le i \le n$)&nbsp;— the index of the character to flip for that query.</p>

## Output

<p>For each query, print "<span class="tex-font-style-tt">YES</span>" if the string is walkable after that query, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p>





```input1
10 9
(())()()))
9
7
2
6
3
6
7
4
8
```




```input2
3 2
(()
2
3
```




```output1
YES
YES
NO
NO
YES
NO
YES
NO
NO
```




```output2
NO
NO
```



## Note

<p>In the first example: </p><ul> <li> After the first query, the string is <span class="tex-font-style-tt">(())()()()</span>. This string is a regular bracket sequence, so it is walkable by simply moving to the right. </li><li> After the second query, the string is <span class="tex-font-style-tt">(())()))()</span>. If you move right once, then left once, then walk right until you hit the end of the string, you produce the string <span class="tex-font-style-tt">(((())()))()</span>, which is a regular bracket sequence. </li><li> After the third query, the string is <span class="tex-font-style-tt">()))()))()</span>. We can show that this string is not walkable. </li></ul> In the second example, the strings after the queries are <span class="tex-font-style-tt">())</span> and <span class="tex-font-style-tt">()(</span>, neither of which are walkable.
