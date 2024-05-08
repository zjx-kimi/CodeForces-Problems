## Description

<div><p><span class="tex-font-style-bf">This is the easy version of the problem. The only differences between the two versions of this problem are the constraints on $k$. You can make hacks only if all versions of the problem are solved.</span></p><p>You are given integers $n$, $p$ and $k$. $p$ is guaranteed to be a prime number. </p><p>For each $r$ from $0$ to $k$, find the number of $n \times n$ matrices $A$ of the field$^\dagger$ of integers modulo $p$ such that the rank$^\ddagger$ of $A$ is exactly $r$. Since these values are big, you are only required to output them modulo $998\,244\,353$.</p><p>$^\dagger$ <a href="https://en.wikipedia.org/wiki/Field_(mathematics)">https://en.wikipedia.org/wiki/Field_(mathematics)</a></p><p>$^\ddagger$ <a href="https://en.wikipedia.org/wiki/Rank_(linear_algebra)">https://en.wikipedia.org/wiki/Rank_(linear_algebra)</a></p></div><div class="input-specification"><p>The first line of input contains three integers $n$, $p$ and $k$ ($1 \leq n \leq 10^{18}$, $2 \leq p &lt; 998\,244\,353$, $0 \leq k \leq 5000$).</p><p>It is guaranteed that $p$ is a prime number.</p></div><div class="output-specification"><p>Output $k+1$ integers, the answers for each $r$ from $0$ to $k$.</p></div>

## Input

<p>The first line of input contains three integers $n$, $p$ and $k$ ($1 \leq n \leq 10^{18}$, $2 \leq p &lt; 998\,244\,353$, $0 \leq k \leq 5000$).</p><p>It is guaranteed that $p$ is a prime number.</p>

## Output

<p>Output $k+1$ integers, the answers for each $r$ from $0$ to $k$.</p>





```input1|
3 2 3
```




```input2|
1 51549919 2
```




```output1
1 49 294 168
```




```output2
1 51549918 0
```


