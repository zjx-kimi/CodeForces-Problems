## Description

<div><p>There are $n$ officers in the Army of Byteland. Each officer has some power associated with him. The power of the $i$-th officer is denoted by $p_{i}$. As the war is fast approaching, the General would like to know the strength of the army.</p><p>The strength of an army is calculated in a strange way in Byteland. The General selects a random subset of officers from these $n$ officers and calls this subset a battalion.(All $2^n$ subsets of the $n$ officers can be chosen equally likely, including empty subset and the subset of all officers).</p><p>The strength of a battalion is calculated in the following way:</p><p>Let the powers of the chosen officers be $a_{1},a_{2},\ldots,a_{k}$, where $a_1 \le a_2 \le \dots \le a_k$. The strength of this battalion is equal to $a_1a_2 + a_2a_3 + \dots + a_{k-1}a_k$. (If the size of Battalion is $\leq 1$, then the strength of this battalion is $0$).</p><p>The strength of the army is equal to the expected value of the strength of the battalion.</p><p>As the war is really long, the powers of officers may change. Precisely, there will be $q$ changes. Each one of the form $i$ $x$ indicating that $p_{i}$ is changed to $x$.</p><p>You need to find the strength of the army initially and after each of these $q$ updates.</p><p>Note that the changes are permanent.</p><p>The strength should be found by modulo $10^{9}+7$. Formally, let $M=10^{9}+7$. It can be shown that the answer can be expressed as an irreducible fraction $p/q$, where $p$ and $q$ are integers and $q\not\equiv 0 \bmod M$). Output the integer equal to $p\cdot q^{-1} \bmod M$. In other words, output such an integer $x$ that $0 \leq x &lt; M$ and $x ⋅ q \equiv p \bmod M$).</p></div><div class="input-specification"><p>The first line of the input contains a single integer $n$ ($1 \leq n \leq 3⋅10^{5}$) &nbsp;— the number of officers in Byteland's Army.</p><p>The second line contains $n$ integers $p_{1},p_{2},\ldots,p_{n}$ ($1 \leq p_{i} \leq 10^{9}$).</p><p>The third line contains a single integer $q$ ($1 \leq q \leq 3⋅10^{5}$) &nbsp;— the number of updates.</p><p>Each of the next $q$ lines contains two integers $i$ and $x$ ($1 \leq i \leq n$, $ 1 \leq x \leq 10^{9}$), indicating that $p_{i}$ is updated to $x$ .</p></div><div class="output-specification"><p>In the first line output the initial strength of the army.</p><p>In $i$-th of the next $q$ lines, output the strength of the army after $i$-th update.</p></div>

## Input

<p>The first line of the input contains a single integer $n$ ($1 \leq n \leq 3⋅10^{5}$) &nbsp;— the number of officers in Byteland's Army.</p><p>The second line contains $n$ integers $p_{1},p_{2},\ldots,p_{n}$ ($1 \leq p_{i} \leq 10^{9}$).</p><p>The third line contains a single integer $q$ ($1 \leq q \leq 3⋅10^{5}$) &nbsp;— the number of updates.</p><p>Each of the next $q$ lines contains two integers $i$ and $x$ ($1 \leq i \leq n$, $ 1 \leq x \leq 10^{9}$), indicating that $p_{i}$ is updated to $x$ .</p>

## Output

<p>In the first line output the initial strength of the army.</p><p>In $i$-th of the next $q$ lines, output the strength of the army after $i$-th update.</p>





```input1
2
1 2
2
1 2
2 1
```




```input2
4
1 2 3 4
4
1 5
2 5
3 5
4 5
```




```output1
500000004
1
500000004
```




```output2
625000011
13
62500020
375000027
62500027
```



## Note

<p>In first testcase, initially, there are four possible battalions </p><ul> <li> {} Strength = $0$ </li><li> {$1$} Strength = $0$ </li><li> {$2$} Strength = $0$ </li><li> {$1,2$} Strength = $2$ </li></ul> So strength of army is $\frac{0+0+0+2}{4}$ = $\frac{1}{2}$<p>After changing $p_{1}$ to $2$, strength of battallion {$1,2$} changes to $4$, so strength of army becomes $1$.</p><p>After changing $p_{2}$ to $1$, strength of battalion {$1,2$} again becomes $2$, so strength of army becomes $\frac{1}{2}$.</p>
