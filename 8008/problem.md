## Description

<div><p>Every superhero has been given a power value by the Felicity Committee. The avengers crew wants to maximize the average power of the superheroes in their team by performing certain operations.</p><p>Initially, there are $n$ superheroes in avengers team having powers $a_1, a_2, \ldots, a_n$, respectively. In one operation, they can remove one superhero from their team (if there are at least two) or they can increase the power of a superhero by $1$. They can do at most $m$ operations. Also, on a particular superhero at most $k$ operations can be done.</p><p>Can you help the avengers team to maximize the average power of their crew?</p></div><div class="input-specification"><p>The first line contains three integers $n$, $k$ and $m$ ($1 \le n \le 10^{5}$, $1 \le k \le 10^{5}$, $1 \le m \le 10^{7}$)&nbsp;— the number of superheroes, the maximum number of times you can increase power of a particular superhero, and the total maximum number of operations.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^{6}$)&nbsp;— the initial powers of the superheroes in the cast of avengers.</p></div><div class="output-specification"><p>Output a single number&nbsp;— the maximum final average power.</p><p>Your answer is considered correct if its absolute or relative error does not exceed $10^{-6}$.</p><p>Formally, let your answer be $a$, and the jury's answer be $b$. Your answer is accepted if and only if $\frac{|a - b|}{\max{(1, |b|)}} \le 10^{-6}$.</p></div>

## Input

<p>The first line contains three integers $n$, $k$ and $m$ ($1 \le n \le 10^{5}$, $1 \le k \le 10^{5}$, $1 \le m \le 10^{7}$)&nbsp;— the number of superheroes, the maximum number of times you can increase power of a particular superhero, and the total maximum number of operations.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^{6}$)&nbsp;— the initial powers of the superheroes in the cast of avengers.</p>

## Output

<p>Output a single number&nbsp;— the maximum final average power.</p><p>Your answer is considered correct if its absolute or relative error does not exceed $10^{-6}$.</p><p>Formally, let your answer be $a$, and the jury's answer be $b$. Your answer is accepted if and only if $\frac{|a - b|}{\max{(1, |b|)}} \le 10^{-6}$.</p>





```input1
2 4 6
4 7
```




```input2
4 2 6
1 3 2 3
```




```output1
11.00000000000000000000
```




```output2
5.00000000000000000000
```



## Note

<p>In the first example, the maximum average is obtained by deleting the first element and increasing the second element four times.</p><p>In the second sample, one of the ways to achieve maximum average is to delete the first and the third element and increase the second and the fourth elements by $2$ each.</p>
