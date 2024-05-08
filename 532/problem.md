## Description

<div><p>Once upon a time, Toma found himself in a binary cafe. It is a very popular and unusual place.</p><p>The cafe offers visitors $k$ different delicious desserts. The desserts are numbered from $0$ to $k-1$. The cost of the $i$-th dessert is $2^i$ coins, because it is a binary cafe! Toma is willing to spend no more than $n$ coins on tasting desserts. At the same time, he is not interested in buying any dessert more than once, because one is enough to evaluate the taste.</p><p>In how many different ways can he buy several desserts <span class="tex-font-style-bf">(possibly zero)</span> for tasting?</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>Then follows $t$ lines, each of which describes one test case.</p><p>Each test case is given on a single line and consists of two integers $n$ and $k$ ($1 \le n, k \le 10^9$)&nbsp;— the number of coins Toma is willing to spend and the number of desserts in the binary cafe.</p></div><div class="output-specification"><p>Output $t$ integers, the $i$-th of which should be equal to the answer for the $i$-th test case&nbsp;— the number of ways to buy desserts for tasting.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>Then follows $t$ lines, each of which describes one test case.</p><p>Each test case is given on a single line and consists of two integers $n$ and $k$ ($1 \le n, k \le 10^9$)&nbsp;— the number of coins Toma is willing to spend and the number of desserts in the binary cafe.</p>

## Output

<p>Output $t$ integers, the $i$-th of which should be equal to the answer for the $i$-th test case&nbsp;— the number of ways to buy desserts for tasting.</p>





```input1|2,4,6
5
1 2
2 1
2 2
10 2
179 100
```




```output1
2
2
3
4
180
```



## Note

<p>Variants for 1st sample: {}, {1}</p><p>Variants for 2nd sample: {}, {1}</p><p>Variants for 3rd sample: {}, {1}, {2}</p><p>Variants for 4th sample: {}, {1}, {2}, {1, 2}</p>
