## Description

<div><p>Let's call a positive integer <span class="tex-font-style-it">good</span> if there is no digit <span class="tex-font-style-tt">0</span> in its decimal representation.</p><p>For an array of a <span class="tex-font-style-it">good</span> numbers $a$, one found out that the sum of some two neighboring elements is equal to $x$ (i.e. $x = a_i + a_{i + 1}$ for some $i$). $x$ had turned out to be a <span class="tex-font-style-it">good</span> number as well.</p><p>Then the elements of the array $a$ were written out one after another without separators into one string $s$. For example, if $a = [12, 5, 6, 133]$, then $s = 1256133$.</p><p>You are given a string $s$ and a number $x$. Your task is to determine the positions in the string that correspond to the adjacent elements of the array that have sum $x$. If there are several possible answers, you can print any of them.</p></div><div class="input-specification"><p>The first line contains the string $s$ ($2 \le |s| \le 5 \cdot 10^5$).</p><p>The second line contains an integer $x$ ($2 \le x &lt; 10^{200000}$).</p><p>An additional constraint on the input: the answer always exists, i.e you can always select two adjacent substrings of the string $s$ so that if you convert these substrings to integers, their sum is equal to $x$.</p></div><div class="output-specification"><p>In the first line, print two integers $l_1$, $r_1$, meaning that the first term of the sum ($a_i$) is in the string $s$ from position $l_1$ to position $r_1$.</p><p>In the second line, print two integers $l_2$, $r_2$, meaning that the second term of the sum ($a_{i + 1}$) is in the string $s$ from position $l_2$ to position $r_2$.</p></div>

## Input

<p>The first line contains the string $s$ ($2 \le |s| \le 5 \cdot 10^5$).</p><p>The second line contains an integer $x$ ($2 \le x &lt; 10^{200000}$).</p><p>An additional constraint on the input: the answer always exists, i.e you can always select two adjacent substrings of the string $s$ so that if you convert these substrings to integers, their sum is equal to $x$.</p>

## Output

<p>In the first line, print two integers $l_1$, $r_1$, meaning that the first term of the sum ($a_i$) is in the string $s$ from position $l_1$ to position $r_1$.</p><p>In the second line, print two integers $l_2$, $r_2$, meaning that the second term of the sum ($a_{i + 1}$) is in the string $s$ from position $l_2$ to position $r_2$.</p>





```input1
1256133
17
```




```input2
9544715561
525
```




```input3
239923
5
```




```input4
1218633757639
976272
```




```output1
1 2
3 3
```




```output2
2 3
4 6
```




```output3
1 1
2 2
```




```output4
2 7
8 13
```



## Note

<p>In the first example $s[1;2] = 12$ and $s[3;3] = 5$, $12+5=17$.</p><p>In the second example $s[2;3] = 54$ and $s[4;6] = 471$, $54+471=525$.</p><p>In the third example $s[1;1] = 2$ and $s[2;2] = 3$, $2+3=5$.</p><p>In the fourth example $s[2;7] = 218633$ and $s[8;13] = 757639$, $218633+757639=976272$.</p>
