## Description

<div><p><span class="tex-font-style-bf">This is the hard version of the problem. The only difference is that in this version $k\le n$. You can make hacks only if both versions of the problem are solved.</span> </p><center>  <img class="tex-graphics" src="file://u8YmdS5Y.png" style="max-width: 100.0%;max-height: 100.0%;" width="360px">   <span class="tex-font-size-small">Chtholly and the floating islands.</span> </center><p>LuoTianyi now lives in a world with $n$ floating islands. The floating islands are connected by $n-1$ undirected air routes, and any two of them can reach each other by passing the routes. That means, the $n$ floating islands form a tree.</p><p>One day, LuoTianyi wants to meet her friends: Chtholly, Nephren, William, .... Totally, she wants to meet $k$ people. She doesn't know the exact positions of them, but she knows that they are in <span class="tex-font-style-bf">pairwise distinct</span> islands. She define an island is <span class="tex-font-style-it">good</span> if and only if the sum of the distances$^{\dagger}$ from it to the islands with $k$ people is the minimal among all the $n$ islands.</p><p>Now, LuoTianyi wants to know that, if the $k$ people are randomly set in $k$ distinct of the $n$ islands, then what is the expect number of the good islands? You just need to tell her the expect number modulo $10^9+7$.</p><p>$^{\dagger}$The distance between two islands is the minimum number of air routes you need to take to get from one island to the other.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $k$ ($1\le k \le n \le 2\cdot 10^5$) — the number of the islands and people respectively.</p><p>Next $n−1$ lines describe the air routes. The $i$-th of them contains two integers $u_i$ and $v_i$ ($1 \le u_i,v_i \le n, u_i \neq v_i$) — the islands connected by the $i$-th air route.</p></div><div class="output-specification"><p>Print a single integer — the expect number of the good islands modulo $10^9 + 7$.</p><p>Formally, let $M = 10^9 + 7$. It can be shown that the answer can be expressed as an irreducible fraction $\frac{p}{q}$, where $p$ and $q$ are integers and $q \not \equiv 0$ ($\operatorname{mod} M$). Output the integer equal to $p \cdot q^{-1}$ $\operatorname{mod} M$. In other words, output such an integer $x$ that $0 \le x &lt; M$ and $x \cdot q \equiv p$ ($\operatorname{mod} M$).</p></div>

## Input

<p>The first line contains two integers $n$ and $k$ ($1\le k \le n \le 2\cdot 10^5$) — the number of the islands and people respectively.</p><p>Next $n−1$ lines describe the air routes. The $i$-th of them contains two integers $u_i$ and $v_i$ ($1 \le u_i,v_i \le n, u_i \neq v_i$) — the islands connected by the $i$-th air route.</p>

## Output

<p>Print a single integer — the expect number of the good islands modulo $10^9 + 7$.</p><p>Formally, let $M = 10^9 + 7$. It can be shown that the answer can be expressed as an irreducible fraction $\frac{p}{q}$, where $p$ and $q$ are integers and $q \not \equiv 0$ ($\operatorname{mod} M$). Output the integer equal to $p \cdot q^{-1}$ $\operatorname{mod} M$. In other words, output such an integer $x$ that $0 \le x &lt; M$ and $x \cdot q \equiv p$ ($\operatorname{mod} M$).</p>





```input1
4 2
1 2
2 3
3 4
```




```input2
5 5
1 2
2 3
3 4
3 5
```




```output1
666666674
```




```output2
1
```



## Note

<p>In the first example the air routes form the following tree:</p><center> <img class="tex-graphics" src="file://9qu55M6P.png" style="max-width: 100.0%;max-height: 100.0%;">   </center> <p>If the people are in the islands $1$ and $2$, then islands $1$ and $2$ will be good.</p><p>The sum of the distances from island $1$ or $2$ to all the people is $1+0=1$, which is the minimal. While the sum of the distances from island $3$ to all the people is $2+1=3$, which is greater than $1$.</p><p>Like this, when the people are in island $1$ and $3$, then islands $1,2$ and $3$ will be good.</p><p>When the people are in islands $1$ and $4$, then islands $1,2,3$ and $4$ will be good.</p><p>When the people are in islands $2$ and $3$, then islands $2$ and $3$ will be good.</p><p>When the people are in islands $2$ and $4$, then islands $2,3$ and $4$ will be good.</p><p>When the people are in islands $3$ and $4$, then islands $3$ and $4$ will be good.</p><p>So the expect of the number of the good islands is $\frac{16}{6}$, which equals to $666666674$ modulo $10^9+7$.</p><p>In the second example the air routes form the following tree:</p><center> <img class="tex-graphics" src="file://oP33JAP8.png" style="max-width: 100.0%;max-height: 100.0%;">   </center><p>We can see that there is one person in each island, and only the island $3$ is good. So the expect number is $1$.</p>
