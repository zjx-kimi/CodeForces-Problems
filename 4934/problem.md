## Description

<div><p>Ira loves Spanish flamenco dance very much. She decided to start her own dance studio and found $n$ students, $i$th of whom has <span class="tex-font-style-it">level</span> $a_i$.</p><p>Ira can choose several of her students and set a dance with them. So she can set a huge number of dances, but she is only interested in <span class="tex-font-style-it">magnificent</span> dances. The dance is called <span class="tex-font-style-it">magnificent</span> if the following is true: </p><ul> <li> <span class="tex-font-style-bf">exactly</span> $m$ students participate in the dance; </li><li> <span class="tex-font-style-it">levels</span> of all dancers are <span class="tex-font-style-bf">pairwise distinct</span>; </li><li> <span class="tex-font-style-it">levels</span> of every two dancers have an absolute difference <span class="tex-font-style-bf">strictly less</span> than $m$. </li></ul><p>For example, if $m = 3$ and $a = [4, 2, 2, 3, 6]$, the following dances are <span class="tex-font-style-it">magnificent</span> (students participating in the dance are highlighted in red): $[\color{red}{4}, 2, \color{red}{2}, \color{red}{3}, 6]$, $[\color{red}{4}, \color{red}{2}, 2, \color{red}{3}, 6]$. At the same time dances $[\color{red}{4}, 2, 2, \color{red}{3}, 6]$, $[4, \color{red}{2}, \color{red}{2}, \color{red}{3}, 6]$, $[\color{red}{4}, 2, 2, \color{red}{3}, \color{red}{6}]$ are not <span class="tex-font-style-it">magnificent</span>.</p><p>In the dance $[\color{red}{4}, 2, 2, \color{red}{3}, 6]$ only $2$ students participate, although $m = 3$.</p><p>The dance $[4, \color{red}{2}, \color{red}{2}, \color{red}{3}, 6]$ involves students with <span class="tex-font-style-it">levels</span> $2$ and $2$, although <span class="tex-font-style-it">levels</span> of all dancers must be pairwise distinct.</p><p>In the dance $[\color{red}{4}, 2, 2, \color{red}{3}, \color{red}{6}]$ students with <span class="tex-font-style-it">levels</span> $3$ and $6$ participate, but $|3 - 6| = 3$, although $m = 3$.</p><p>Help Ira count the number of <span class="tex-font-style-it">magnificent</span> dances that she can set. Since this number can be very large, count it <span class="tex-font-style-bf">modulo</span> $10^9 + 7$. Two dances are considered different if the sets of students participating in them are different.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— number of testcases.</p><p>The first line of each testcase contains integers $n$ and $m$ ($1 \le m \le n \le 2 \cdot 10^5$)&nbsp;— the number of Ira students and the number of dancers in the <span class="tex-font-style-it">magnificent</span> dance.</p><p>The second line of each testcase contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— <span class="tex-font-style-it">levels</span> of students.</p><p>It is guaranteed that the sum of $n$ over all testcases <span class="tex-font-style-bf">does not exceed</span> $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each testcase, print a single integer&nbsp;— the number of <span class="tex-font-style-it">magnificent</span> dances. Since this number can be very large, print it <span class="tex-font-style-bf">modulo</span> $10^9 + 7$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— number of testcases.</p><p>The first line of each testcase contains integers $n$ and $m$ ($1 \le m \le n \le 2 \cdot 10^5$)&nbsp;— the number of Ira students and the number of dancers in the <span class="tex-font-style-it">magnificent</span> dance.</p><p>The second line of each testcase contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— <span class="tex-font-style-it">levels</span> of students.</p><p>It is guaranteed that the sum of $n$ over all testcases <span class="tex-font-style-bf">does not exceed</span> $2 \cdot 10^5$.</p>

## Output

<p>For each testcase, print a single integer&nbsp;— the number of <span class="tex-font-style-it">magnificent</span> dances. Since this number can be very large, print it <span class="tex-font-style-bf">modulo</span> $10^9 + 7$.</p>





```input1|2,3,6,7,10,11,14,15,18,19
9
7 4
8 10 10 9 6 11 7
5 3
4 2 2 3 6
8 2
1 5 2 2 3 1 3 3
3 3
3 3 3
5 1
3 4 3 10 7
12 3
5 2 1 1 4 3 5 5 5 2 7 5
1 1
1
3 2
1 2 3
2 2
1 2
```




```output1
5
2
10
0
5
11
1
2
1
```



## Note

<p>In the first testcase, Ira can set such <span class="tex-font-style-it">magnificent</span> dances: $[\color{red}{8}, 10, 10, \color{red}{9}, \color{red}{6}, 11, \color{red}{7}]$, $[\color{red}{8}, \color{red}{10}, 10, \color{red}{9}, 6, 11, \color{red}{7}]$, $[\color{red}{8}, 10, \color{red}{10}, \color{red}{9}, 6, 11, \color{red}{7}]$, $[\color{red}{8}, 10, \color{red}{10}, \color{red}{9}, 6, \color{red}{11}, 7]$, $[\color{red}{8}, \color{red}{10}, 10, \color{red}{9}, 6, \color{red}{11}, 7]$.</p><p>The second testcase is explained in the statements.</p>
