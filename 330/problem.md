## Description

<div><p>There are $n + 1$ cities with numbers from $0$ to $n$, connected by $n$ roads. The $i$-th $(1 \leq i \leq n)$ road connects city $i-1$ and city $i$ bi-directionally. After Jellyfish flew back to city $0$, she found out that she had left her Miku fufu in city $n$.</p><p>Each road has a <span class="tex-font-style-bf">positive integer</span> level of <span class="tex-font-style-it">beauty</span>. Denote the beauty of the $i$-th road as $a_i$.</p><p>Jellyfish is trying to find her fufu. Because of her poor sense of direction, she doesn't know which way to go. Every day, she randomly chooses a road connected to the city she currently is in and traverses it. Let $s$ be the sum of the beauty of the roads connected to the current city. For each road connected to the current city, Jellyfish will traverse the road with a probability of $\frac x s$, where $x$ is the beauty of the road, reaching the city on the other side of the road.</p><p>Jellyfish will start at city $0$, and she will get only her fufu back when she reaches city $n$.</p><p>You want to choose the beauty of the roads such that the expected number of days Jellyfish takes to find her fufu will be the minimum possible. However, due to limited funding, the sum of beauties of all roads must be less than or equal to $m$. </p><p>Find the minimum expected number of days Jellyfish needs to get her fufu back if the beauty of the roads is chosen optimally.</p></div><div class="input-specification"><p>The first and only line of the input contains two integers $n$ and $m$ ($1 \leq n \leq m \leq 3000$)&nbsp;— the number of the roads and the maximum sum of beauty of the roads.</p></div><div class="output-specification"><p>Output the minimum expected number of days Jellyfish needs to get her fufu back if the beauty of the roads is chosen optimally.</p><p>Your answer will be accepted if the absolute or relative error does not exceed $10^{-9}$. Formally, let your answer be $a$, and the jury's answer be $b$. Your answer is considered correct if $\frac{|a-b|}{\max(1,|b|)} \leq 10^{-9}$.</p></div>

## Input

<p>The first and only line of the input contains two integers $n$ and $m$ ($1 \leq n \leq m \leq 3000$)&nbsp;— the number of the roads and the maximum sum of beauty of the roads.</p>

## Output

<p>Output the minimum expected number of days Jellyfish needs to get her fufu back if the beauty of the roads is chosen optimally.</p><p>Your answer will be accepted if the absolute or relative error does not exceed $10^{-9}$. Formally, let your answer be $a$, and the jury's answer be $b$. Your answer is considered correct if $\frac{|a-b|}{\max(1,|b|)} \leq 10^{-9}$.</p>





```input1
3 8
```




```input2
10 98
```




```output1
5.200000000000
```




```output2
37.721155173329
```



## Note

<p>In the first example, the optimal assignment of beauty is $a=[1, 2, 5]$. The expected number of days Jellyfish needs to get her fufu back is $5.2$.</p>
