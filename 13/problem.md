## Description

<div><p>You have a square piece of paper with a side length equal to $1$ unit. In one operation, you fold each corner of the square to the center of the paper, thus forming another square with a side length equal to $\dfrac{1}{\sqrt{2}}$ units. By taking this square as a new square, you do the operation again and repeat this process a total of $N$ times.</p><center>  <img class="tex-graphics" src="file://1SLQLp6I.png" style="max-width: 100.0%;max-height: 100.0%;" width="675px">   <span class="tex-font-size-small">Performing operations for $N = 2$.</span> </center><p>After performing the set of operations, you open the paper with the same side up you started with and see some crease lines on it. Every crease line is one of two types: a mountain or a valley. A mountain is when the paper folds outward, and a valley is when the paper folds inward.</p><p>You calculate the sum of the length of all mountain crease lines on the paper and call it $M$. Similarly, you calculate for valley crease lines and call it $V$. You want to find the value of $\dfrac{M}{V}$.</p><p>It can be proved that this value can be represented in the form of $A + B\sqrt{2}$, where $A$ and $B$ are rational numbers. Let this $B$ be represented as an irreducible fraction $\dfrac{p}{q}$, your task is to print $p*inv(q)$ modulo $999\,999\,893$ <span class="tex-font-style-bf">(note the unusual modulo)</span>, where $inv(q)$ is the <a href="https://en.wikipedia.org/wiki/Modular_multiplicative_inverse">modular inverse</a> of $q$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 10^4$). Description of the test cases follows.</p><p>The only line of each test case contains an integer $N$ ($1 \leq N \leq 10^9$), the number of operations you perform on the square paper.</p></div><div class="output-specification"><p>For each test case, print on a new line the required answer.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 10^4$). Description of the test cases follows.</p><p>The only line of each test case contains an integer $N$ ($1 \leq N \leq 10^9$), the number of operations you perform on the square paper.</p>

## Output

<p>For each test case, print on a new line the required answer.</p>





```input1|2,4
3
1
2
3
```




```output1
0
1
714285638
```



## Note

<p>The blue lines in the given figures represent mountain crease lines, and the green lines represent valley crease lines.</p><center>  <table class="tex-tabular"><tbody><tr><td class="tex-tabular-text-align-center"><img class="tex-graphics" src="file://uvdsFMKJ.png" style="max-width: 100.0%;max-height: 100.0%;" width="320px"></td><td class="tex-tabular-text-align-center"><img class="tex-graphics" src="file://QOQz3KN6.png" style="max-width: 100.0%;max-height: 100.0%;" width="315px"></td></tr><tr><td class="tex-tabular-text-align-center"><span class="tex-font-size-small">Crease lines after $1$ operation $(\dfrac{M}{V} = 0)$.</span></td><td class="tex-tabular-text-align-center"><span class="tex-font-size-small">Crease lines after $2$ operations $(\dfrac{M}{V} = \sqrt{2} - 1)$.</span></td></tr></tbody></table> </center>
