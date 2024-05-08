## Description

<div><p><span class="tex-font-style-bf">The only difference between easy and hard versions is the maximum number of queries. In this version, you are allowed to ask at most $1000$ queries.</span></p><p><span class="tex-font-style-it">This is an interactive problem.</span></p><p>You are playing a game. The circle is divided into $n$ sectors, sectors are numbered from $1$ to $n$ in some order. You are in the adjacent room and do not know either the number of sectors or their numbers. There is also an arrow that initially points to some sector. Initially, the host tells you the number of the sector to which the arrow points. After that, you can ask the host to move the arrow $k$ sectors counterclockwise or clockwise at most $1000$ times. And each time you are told the number of the sector to which the arrow points.</p><p>Your task is to determine the integer $n$&nbsp;— the number of sectors in at most $1000$ queries.</p><p>It is guaranteed that $1 \le n \le 10^6$.</p></div><div class="input-specification"><p>The input consists of a single integer $x$ ($1 \le x \le n$)&nbsp;— the number of the initial sector.</p></div><div class="output-specification"><p>After you determine the integer $n$&nbsp;— the number of sectors, you should output "! n" ($1 \le n \le 10^6$). After that the program should immediately terminate.</p><p>Note that, printing the answer does not count as a query.</p><p>It is guaranteed that the integer $n$ and the numbers of the sectors are fixed initially and will not be changed by the jury program depending on the queries.</p></div><div><h2>Interaction</h2><p>After reading the description of the input, you may ask queries. Queries can be of two types:</p><ol> <li> "+ k" ($0 \le k \le 10^9$)&nbsp;— ask to move the arrow $k$ sectors clockwise. </li><li> "- k" ($0 \le k \le 10^9$)&nbsp;— ask to move the arrow $k$ sectors counterclockwise. </li></ol><p>After each query, you should read an integer $x$ ($1 \le x \le n$)&nbsp;— the number of the current sector to which the arrow points.</p><p>You are allowed to make at most $1000$ queries in total.</p><p>If you make too many queries, you will get <span class="tex-font-style-it">Wrong answer</span>.</p><p>After printing a query or the answer, do not forget to output a the end of line and flush the output. Otherwise, you will get <span class="tex-font-style-it">Idleness limit exceeded</span>. To do this, use: </p><ul> <li> <span class="tex-font-style-it">fflush(stdout)</span> or <span class="tex-font-style-it">cout.flush()</span> in C++; </li><li> <span class="tex-font-style-it">System.out.flush()</span> in Java; </li><li> <span class="tex-font-style-it">flush(output)</span> in Pascal; </li><li> <span class="tex-font-style-it">stdout.flush()</span> in Python; </li><li> see the documentation for other languages. </li></ul></div>

## Input

<p>The input consists of a single integer $x$ ($1 \le x \le n$)&nbsp;— the number of the initial sector.</p>

## Output

<p>After you determine the integer $n$&nbsp;— the number of sectors, you should output "! n" ($1 \le n \le 10^6$). After that the program should immediately terminate.</p><p>Note that, printing the answer does not count as a query.</p><p>It is guaranteed that the integer $n$ and the numbers of the sectors are fixed initially and will not be changed by the jury program depending on the queries.</p>





```input1
1

5

6

7

2

10

9

8

4

3

1
```




```output1
+ 1

+ 1

+ 1

+ 1

+ 1

+ 1

+ 1

+ 1

+ 1

+ 1

! 10
```



## Note

<p><span class="tex-font-style-bf">Hacks</span></p><p>To hack, use the following test format.</p><p>In the first line, output a single integer $n$ ($1 \le n \le 10^6$)&nbsp;— the number of sectors.</p><p>In the second line, output $n$ different integers $1 \le a_1, a_2, \dots, a_n \le n$&nbsp;— the numbers of the sectors in clockwise order, the arrow initially points to the sector with the number $a_1$.</p>
