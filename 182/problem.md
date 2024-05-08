## Description

<div><p>Vasya is a sorcerer that fights monsters. Again. There are $n$ monsters standing in a row, the amount of health points of the $i$-th monster is $a_i$.</p><p>Vasya is a very powerful sorcerer who knows many overpowered spells. In this fight, he decided to use a chain lightning spell to defeat all the monsters. Let's see how this spell works.</p><p>Firstly, Vasya chooses an index $i$ of some monster ($1 \le i \le n$) and the initial power of the spell $x$. Then the spell hits monsters <span class="tex-font-style-bf">exactly</span> $n$ times, one hit per monster. The first target of the spell is always the monster $i$. For every target <span class="tex-font-style-bf">except for the first one</span>, the chain lightning will choose a <span class="tex-font-style-bf">random</span> monster <span class="tex-font-style-bf">who was not hit by the spell and is adjacent to one of the monsters that already was hit</span>. So, each monster will be hit exactly once. The first monster hit by the spell receives $x$ damage, the second monster receives $(x-1)$ damage, the third receives $(x-2)$ damage, and so on.</p><p>Vasya wants to show how powerful he is, so he wants to kill all the monsters with a single chain lightning spell. The monster is considered dead if the damage he received is not less than the amount of its health points. On the other hand, Vasya wants to show he doesn't care that much, so he wants to choose the <span class="tex-font-style-bf">minimum</span> initial power of the spell $x$ such that it kills all monsters, <span class="tex-font-style-bf">no matter which monster (among those who can get hit) gets hit on each step</span>.</p><p>Of course, Vasya is a sorcerer, but the amount of calculations required to determine the optimal spell setup is way above his possibilities, so you have to help him find the minimum spell power required to kill all the monsters.</p><p>Note that Vasya chooses the initial target and the power of the spell, other things should be considered random and Vasya wants to kill all the monsters even in the worst possible scenario.</p></div><div class="input-specification"><p>The first line of the input contains one integer $n$ ($1 \le n \le 3 \cdot 10^5$) — the number of monsters.</p><p>The second line of the input contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$), where $a_i$ is the amount of health points of the $i$-th monster.</p></div><div class="output-specification"><p>Print one integer — the minimum spell power required to kill all the monsters if Vasya chooses the first target optimally, and the order of spell hits can be any possible within the given rules.</p></div>

## Input

<p>The first line of the input contains one integer $n$ ($1 \le n \le 3 \cdot 10^5$) — the number of monsters.</p><p>The second line of the input contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$), where $a_i$ is the amount of health points of the $i$-th monster.</p>

## Output

<p>Print one integer — the minimum spell power required to kill all the monsters if Vasya chooses the first target optimally, and the order of spell hits can be any possible within the given rules.</p>





```input1
6
2 1 5 6 4 3
```




```input2
5
4 4 4 4 4
```




```input3
2
1 1000000000
```




```output1
8
```




```output2
8
```




```output3
1000000000
```


