## Description

<div><p>One day, $n$ people ($n$ is an even number) met on a plaza and made two round dances, each round dance consists of exactly $\frac{n}{2}$ people. Your task is to find the number of ways $n$ people can make two round dances if each round dance consists of exactly $\frac{n}{2}$ people. Each person should belong to exactly one of these two round dances.</p><p>Round dance is a dance circle consisting of $1$ or more people. Two round dances are indistinguishable (equal) if one can be transformed to another by choosing the first participant. For example, round dances $[1, 3, 4, 2]$, $[4, 2, 1, 3]$ and $[2, 1, 3, 4]$ are indistinguishable.</p><p>For example, if $n=2$ then the number of ways is $1$: one round dance consists of the first person and the second one of the second person.</p><p>For example, if $n=4$ then the number of ways is $3$. Possible options:</p><ul> <li> one round dance — $[1,2]$, another — $[3,4]$; </li><li> one round dance — $[2,4]$, another — $[3,1]$; </li><li> one round dance — $[4,1]$, another — $[3,2]$. </li></ul><p>Your task is to find the number of ways $n$ people can make two round dances if each round dance consists of exactly $\frac{n}{2}$ people.</p></div><div class="input-specification"><p>The input contains one integer $n$ ($2 \le n \le 20$), $n$ is an even number.</p></div><div class="output-specification"><p>Print one integer — the number of ways to make two round dances. It is guaranteed that the answer fits in the $64$-bit integer data type.</p></div>

## Input

<p>The input contains one integer $n$ ($2 \le n \le 20$), $n$ is an even number.</p>

## Output

<p>Print one integer — the number of ways to make two round dances. It is guaranteed that the answer fits in the $64$-bit integer data type.</p>





```input1
2

```




```input2
4

```




```input3
8

```




```input4
20

```




```output1
1

```




```output2
3

```




```output3
1260

```




```output4
12164510040883200

```


