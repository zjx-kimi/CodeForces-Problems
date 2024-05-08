## Description

<div><p>Let $c_1, c_2, \ldots, c_n$ be a permutation of integers $1, 2, \ldots, n$. Consider all subsegments of this permutation containing an integer $x$. Given an integer $m$, we call the integer $x$ <span class="tex-font-style-it">good</span> if there are exactly $m$ different values of maximum on these subsegments.</p><p>Cirno is studying mathematics, and the teacher asks her to count the number of permutations of length $n$ with exactly $k$ <span class="tex-font-style-it">good</span> numbers.</p><p>Unfortunately, Cirno isn't good at mathematics, and she can't answer this question. Therefore, she asks you for help.</p><p>Since the answer may be very big, you only need to tell her the number of permutations modulo $p$.</p><p>A permutation is an array consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation ($2$ appears twice in the array) and $[1,3,4]$ is also not a permutation ($n=3$ but there is $4$ in the array).</p><p>A sequence $a$ is a subsegment of a sequence $b$ if $a$ can be obtained from $b$ by deletion of several (possibly, zero or all) elements from the beginning and several (possibly, zero or all) elements from the end.</p></div><div class="input-specification"><p>The first line contains four integers $n, m, k, p$ ($1 \le n \le 100, 1 \le m \le n, 1 \le k \le n, 1 \le p \le 10^9$).</p></div><div class="output-specification"><p>Output the number of permutations modulo $p$.</p></div>

## Input

<p>The first line contains four integers $n, m, k, p$ ($1 \le n \le 100, 1 \le m \le n, 1 \le k \le n, 1 \le p \le 10^9$).</p>

## Output

<p>Output the number of permutations modulo $p$.</p>





```input1
4 3 2 10007
```




```input2
6 4 1 769626776
```




```input3
66 11 9 786747482
```




```input4
99 30 18 650457567
```




```output1
4
```




```output2
472
```




```output3
206331312
```




```output4
77365367
```



## Note

<p>In the first test case, there are four permutations: $[1, 3, 2, 4]$, $[2, 3, 1, 4]$, $[4, 1, 3, 2]$ and $[4, 2, 3, 1]$.</p><p>Take permutation $[1, 3, 2, 4]$ as an example:</p><p>For number $1$, all subsegments containing it are: $[1]$, $[1, 3]$, $[1, 3, 2]$ and $[1, 3, 2, 4]$, and there're three different maxima $1$, $3$ and $4$.</p><p>Similarly, for number $3$, there're two different maxima $3$ and $4$. For number $2$, there're three different maxima $2$, $3$ and $4$. And for number $4$, there're only one, that is $4$ itself.</p>
