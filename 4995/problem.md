## Description

<div><p>You are given an array of integers. Vasya can permute (change order) its integers. He wants to do it so that as many as possible integers will become on a place where a smaller integer used to stand. Help Vasya find the maximal number of such integers.</p><p>For instance, if we are given an array $[10, 20, 30, 40]$, we can permute it so that it becomes $[20, 40, 10, 30]$. Then on the first and the second positions the integers became larger ($20&gt;10$, $40&gt;20$) and did not on the third and the fourth, so for this permutation, the number that Vasya wants to maximize equals $2$. Read the note for the first example, there is one more demonstrative test case.</p><p>Help Vasya to permute integers in such way that the number of positions in a new array, where integers are greater than in the original one, is maximal.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($1 \leq n \leq 10^5$)&nbsp;— the length of the array.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$)&nbsp;— the elements of the array.</p></div><div class="output-specification"><p>Print a single integer&nbsp;— the maximal number of the array's elements which after a permutation will stand on the position where a smaller element stood in the initial array.</p></div>

## Input

<p>The first line contains a single integer $n$ ($1 \leq n \leq 10^5$)&nbsp;— the length of the array.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$)&nbsp;— the elements of the array.</p>

## Output

<p>Print a single integer&nbsp;— the maximal number of the array's elements which after a permutation will stand on the position where a smaller element stood in the initial array.</p>





```input1
7
10 1 1 1 5 5 3

```




```input2
5
1 1 1 1 1

```




```output1
4

```




```output2
0

```



## Note

<p>In the first sample, one of the best permutations is $[1, 5, 5, 3, 10, 1, 1]$. On the positions from second to fifth the elements became larger, so the answer for this permutation is 4.</p><p>In the second sample, there is no way to increase any element with a permutation, so the answer is 0.</p>
