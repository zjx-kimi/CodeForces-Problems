## Description

<div><p>Slime and his $n$ friends are at a party. Slime has designed a game for his friends to play.</p><p>At the beginning of the game, the $i$-th player has $a_i$ biscuits. At each second, Slime will choose a biscuit randomly uniformly among all $a_1 + a_2 + \ldots + a_n$ biscuits, and the owner of this biscuit will give it to a random uniform player among $n-1$ players except himself. The game stops when one person will have all the biscuits.</p><p>As the host of the party, Slime wants to know the expected value of the time that the game will last, to hold the next activity on time.</p><p>For convenience, as the answer can be represented as a rational number $\frac{p}{q}$ for coprime $p$ and $q$, you need to find the value of $(p \cdot q^{-1})\mod 998\,244\,353$. You can prove that $q\mod 998\,244\,353 \neq 0$.</p></div><div class="input-specification"><p>The first line contains one integer $n\ (2\le n\le 100\,000)$: the number of people playing the game.</p><p>The second line contains $n$ non-negative integers $a_1,a_2,\dots,a_n\ (1\le a_1+a_2+\dots+a_n\le 300\,000)$, where $a_i$ represents the number of biscuits the $i$-th person own at the beginning.</p></div><div class="output-specification"><p>Print one integer: the expected value of the time that the game will last, modulo $998\,244\,353$.</p></div>

## Input

<p>The first line contains one integer $n\ (2\le n\le 100\,000)$: the number of people playing the game.</p><p>The second line contains $n$ non-negative integers $a_1,a_2,\dots,a_n\ (1\le a_1+a_2+\dots+a_n\le 300\,000)$, where $a_i$ represents the number of biscuits the $i$-th person own at the beginning.</p>

## Output

<p>Print one integer: the expected value of the time that the game will last, modulo $998\,244\,353$.</p>





```input1
2
1 1
```




```input2
2
1 2
```




```input3
5
0 0 0 0 35
```




```input4
5
8 4 2 0 1
```




```output1
1
```




```output2
3
```




```output3
0
```




```output4
801604029
```



## Note

<p>For the first example, in the first second, the probability that player $1$ will give the player $2$ a biscuit is $\frac{1}{2}$, and the probability that player $2$ will give the player $1$ a biscuit is $\frac{1}{2}$. But anyway, the game will stop after exactly $1$ second because only one player will occupy all biscuits after $1$ second, so the answer is $1$.</p>
