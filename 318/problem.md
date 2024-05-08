## Description

<div><p>Pak Chanek has just bought an empty fish tank and he has been dreaming to fill it with his favourite kind of fish, clownfish. Pak Chanek likes clownfish because of their ability to change their genders on demand. Because of the size of his fish tank, Pak Chanek wants to buy exactly $k$ clownfish to fill the tank.</p><p>Pak Chanek goes to the local fish shop. The shop provides $n$ clownfish numbered from $1$ to $n$, with clownfish $i$ having a size of $a_i$. Initially, every clownfish in the store does not have an assigned gender, but has the ability to be assigned to two possible clownfish genders, female or male.</p><p>The store has a procedure which Pak Chanek should follow to buy clownfish. The shop owner will point at each clownfish sequentially from $1$ to $n$ and for each clownfish, she asks Pak Chanek whether to buy it or not. Each time Pak Chanek is asked, he must declare whether to buy the currently asked clownfish or not, before the shop owner moves on to the next clownfish. If Pak Chanek declares to buy the currently asked clownfish, he must also declare the gender to be assigned to that clownfish immediately. When assigning the gender for the currently asked clownfish, the following conditions must be satisfied: </p><ul> <li> If Pak Chanek assigns it to be female and he has bought a female clownfish before, then the size of the current one must be exactly $1$ <span class="tex-font-style-bf">bigger</span> than the last female one. </li><li> If Pak Chanek assigns it to be male and he has bought a male clownfish before, then the size of the current one must be exactly $1$ <span class="tex-font-style-bf">smaller</span> than the last male one. </li></ul><p>Pak Chanek wants to buy exactly $k$ clownfish such that: </p><ul> <li> There is at least one female clownfish and one male clownfish. </li><li> Among the $k$ clownfish Pak Chanek buys, the mean size of the female clownfish is equal to the mean size of the male clownfish. </li></ul><p>Let $l$ and $r$ respectively be the minimum and maximum <span class="tex-font-style-bf">index</span> of a clownfish Pak Chanek buys. What is the minimum possible value of $r-l$?</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $k$ ($2 \leq k \leq n \leq 2\cdot10^5$) — the number of clownfish in the shop and the number of clownfish Pak Chanek has to buy.</p><p>The second line contains $n$ integers $a_1,a_2,a_3,\ldots,a_n$ ($1\leq a_i\leq n$) — the size of each clownfish.</p></div><div class="output-specification"><p>An integer representing the minimum possible value of $r-l$. If it is impossible to buy exactly $k$ clownfish and satisfy the problem's condition, print $-1$.</p></div>

## Input

<p>The first line contains two integers $n$ and $k$ ($2 \leq k \leq n \leq 2\cdot10^5$) — the number of clownfish in the shop and the number of clownfish Pak Chanek has to buy.</p><p>The second line contains $n$ integers $a_1,a_2,a_3,\ldots,a_n$ ($1\leq a_i\leq n$) — the size of each clownfish.</p>

## Output

<p>An integer representing the minimum possible value of $r-l$. If it is impossible to buy exactly $k$ clownfish and satisfy the problem's condition, print $-1$.</p>





```input1
9 6
2 4 2 3 2 4 1 3 4
```




```input2
6 6
2 6 5 2 6 5
```




```input3
5 4
1 2 3 4 5
```




```output1
6
```




```output2
-1
```




```output3
-1
```



## Note

<p>In the first example, Pak Chanek can do the following: </p><ol> <li> Do not buy clownfish $1$. </li><li> Buy clownfish $2$ and assign it as male. </li><li> Buy clownfish $3$ and assign it as female. </li><li> Buy clownfish $4$ and assign it as male. </li><li> Buy clownfish $5$ and assign it as male. </li><li> Do not buy clownfish $6$. </li><li> Buy clownfish $7$ and assign it as male. </li><li> Buy clownfish $8$ and assign it as female. </li><li> Do not buy clownfish $9$. </li></ol><p>Then, we get that: </p><ul> <li> The mean size among the $2$ female clownfish Pak Chanek buys is $\frac{2+3}{2} = 2.5$. </li><li> The mean size among the $4$ male clownfish Pak Chanek buys is $\frac{4+3+2+1}{4} = 2.5$. </li><li> $l=2$, $r=8$, $r-l=6$. </li></ul><p>There are no better strategies.</p>
