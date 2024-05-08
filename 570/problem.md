## Description

<div><p>Vlad decided to compose a melody on his guitar. Let's represent the melody as a sequence of notes corresponding to the characters 'a', 'b', 'c', 'd', 'e', 'f', and 'g'.</p><p>However, Vlad is not very experienced in playing the guitar and can only record <span class="tex-font-style-bf">exactly two</span> notes at a time. Vlad wants to obtain the melody $s$, and to do this, he can merge the recorded melodies together. In this case, the last sound of the first melody must match the first sound of the second melody.</p><p>For example, if Vlad recorded the melodies <span class="tex-font-style-tt">"ab"</span> and <span class="tex-font-style-tt">"ba"</span>, he can merge them together and obtain the melody <span class="tex-font-style-tt">"aba"</span>, and then merge the result with <span class="tex-font-style-tt">"ab"</span> to get <span class="tex-font-style-tt">"abab"</span>.</p><p>Help Vlad determine the <span class="tex-font-style-bf">minimum</span> number of melodies consisting of two notes that he needs to record in order to obtain the melody $s$.</p></div><div class="input-specification"><p>The first line of input contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Following that are the descriptions of the test cases.</p><p>The first line of each test case contains an integer $n$ ($2 \le n \le 50$)&nbsp;— the length of the melody $s$.</p><p>The second line of each test case contains a string $s$ of length $n$, consisting of characters 'a', 'b', 'c', 'd', 'e', 'f', 'g'.</p></div><div class="output-specification"><p>Output $t$ integers, each representing the answer for the corresponding test case. As the answer output <span class="tex-font-style-bf">minimum</span> number of melodies consisting of two notes that Vlad needs to record.</p></div>

## Input

<p>The first line of input contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Following that are the descriptions of the test cases.</p><p>The first line of each test case contains an integer $n$ ($2 \le n \le 50$)&nbsp;— the length of the melody $s$.</p><p>The second line of each test case contains a string $s$ of length $n$, consisting of characters 'a', 'b', 'c', 'd', 'e', 'f', 'g'.</p>

## Output

<p>Output $t$ integers, each representing the answer for the corresponding test case. As the answer output <span class="tex-font-style-bf">minimum</span> number of melodies consisting of two notes that Vlad needs to record.</p>





```input1|2,3,6,7,10,11
5
4
abab
7
abacaba
6
aaaaaa
7
abcdefg
5
babdd
```




```output1
2
4
1
6
4
```



## Note

<p>In the first sample, you need to record the melodies <span class="tex-font-style-tt">"ab"</span> and <span class="tex-font-style-tt">"ba"</span>, as described in the problem statement.</p><p>In the second sample, you need to record the melodies <span class="tex-font-style-tt">"ab"</span>, <span class="tex-font-style-tt">"ba"</span>, <span class="tex-font-style-tt">"ac"</span>, and <span class="tex-font-style-tt">"ca"</span>.</p><p>In the third sample, the only necessary melody is <span class="tex-font-style-tt">"aa"</span>.</p>
