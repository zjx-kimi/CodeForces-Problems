## Description

<div><p>We're giving away nice huge bags containing number tiles! A bag we want to present to you contains $n$ tiles. Each of them has a single number written on it&nbsp;— either $1$ or $2$.</p><p>However, there is one condition you must fulfill in order to receive the prize. You will need to put all the tiles from the bag in a sequence, in any order you wish. We will then compute the sums of all prefixes in the sequence, and then count how many of these sums are prime numbers. If you want to keep the prize, you will need to maximize the number of primes you get.</p><p>Can you win the prize? Hurry up, the bags are waiting!</p></div><div class="input-specification"><p>The first line of the input contains a single integer $n$ ($1 \leq n \leq 200\,000$) — the number of number tiles in the bag. The following line contains $n$ space-separated integers $a_1, a_2, \dots, a_n$ ($a_i \in \{1, 2\}$) — the values written on the tiles.</p></div><div class="output-specification"><p>Output a permutation $b_1, b_2, \dots, b_n$ of the input sequence $(a_1, a_2, \dots, a_n)$ maximizing the number of the prefix sums being prime numbers. If there are multiple optimal permutations, output any.</p></div>

## Input

<p>The first line of the input contains a single integer $n$ ($1 \leq n \leq 200\,000$) — the number of number tiles in the bag. The following line contains $n$ space-separated integers $a_1, a_2, \dots, a_n$ ($a_i \in \{1, 2\}$) — the values written on the tiles.</p>

## Output

<p>Output a permutation $b_1, b_2, \dots, b_n$ of the input sequence $(a_1, a_2, \dots, a_n)$ maximizing the number of the prefix sums being prime numbers. If there are multiple optimal permutations, output any.</p>





```input1
5
1 2 1 2 1
```




```input2
9
1 1 2 1 1 1 2 1 1
```




```output1
1 1 1 2 2
```




```output2
1 1 1 2 1 1 1 2 1
```



## Note

<p>The first solution produces the prefix sums $1, \mathbf{\color{blue}{2}}, \mathbf{\color{blue}{3}}, \mathbf{\color{blue}{5}}, \mathbf{\color{blue}{7}}$ (four primes constructed), while the prefix sums in the second solution are $1, \mathbf{\color{blue}{2}}, \mathbf{\color{blue}{3}}, \mathbf{\color{blue}{5}}, 6, \mathbf{\color{blue}{7}}, 8, 10, \mathbf{\color{blue}{11}}$ (five primes). Primes are marked bold and blue. In each of these cases, the number of produced primes is maximum possible.</p>
