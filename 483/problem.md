## Description

<div><p><span class="tex-font-style-it">Kars</span> is tired and resentful of the narrow mindset of his village since they are content with staying where they are and are not trying to become the perfect life form. Being a top-notch inventor, <span class="tex-font-style-it">Kars</span> wishes to enhance his body and become the perfect life form. Unfortunately, $n$ of the villagers have become suspicious of his ideas. The $i$-th villager has a suspicion of $a_i$ on him. Individually each villager is scared of Kars, so they form into groups to be more powerful.</p><p>The power of the group of villagers from $l$ to $r$ be defined as $f(l,r)$ where </p><p>$$f(l,r) = |a_l - a_{l+1}| + |a_{l + 1} - a_{l + 2}| + \ldots + |a_{r-1} - a_r|.$$</p><p>Here $|x-y|$ is the absolute value of $x-y$. A group with only one villager has a power of $0$.</p><p><span class="tex-font-style-it">Kars</span> wants to break the villagers into exactly $k$ contiguous subgroups so that the sum of their power is minimized. Formally, he must find $k - 1$ positive integers $1 \le r_1 &lt; r_2 &lt; \ldots &lt; r_{k - 1} &lt; n$ such that $f(1, r_1) + f(r_1 + 1, r_2) + \ldots + f(r_{k-1} + 1, n)$ is minimised. Help <span class="tex-font-style-it">Kars</span> in finding the minimum value of $f(1, r_1) + f(r_1 + 1, r_2) + \ldots + f(r_{k-1} + 1, n)$.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ $(1 \leq t \leq 100)$&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains two integers $n,k$ $(1 \leq k \leq n \leq 100)$&nbsp;— the number of villagers and the number of groups they must be split into.</p><p>The second line of each test case contains $n$ integers $a_1,a_2, \ldots, a_n$ $(1 \leq a_i \leq 500)$&nbsp;— the suspicion of each of the villagers.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the minimum possible value of sum of power of all the groups i.&nbsp;e. the minimum possible value of $f(1,r_1) + f(r_1 + 1, r_2) + \ldots + f(r_{k-1} + 1, n)$.</p></div>

## Input

<p>The first line contains a single integer $t$ $(1 \leq t \leq 100)$&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains two integers $n,k$ $(1 \leq k \leq n \leq 100)$&nbsp;— the number of villagers and the number of groups they must be split into.</p><p>The second line of each test case contains $n$ integers $a_1,a_2, \ldots, a_n$ $(1 \leq a_i \leq 500)$&nbsp;— the suspicion of each of the villagers.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the minimum possible value of sum of power of all the groups i.&nbsp;e. the minimum possible value of $f(1,r_1) + f(r_1 + 1, r_2) + \ldots + f(r_{k-1} + 1, n)$.</p>





```input1|2,3,6,7
3
4 2
1 3 5 2
6 3
1 9 12 4 7 2
12 8
1 9 8 2 3 3 1 8 7 7 9 2
```




```output1
4
11
2
```



## Note

<p>In the first test case, we will group the villagers with suspicion $(1,3,5,2)$ into $(1,3,5)$ and $(2)$. So, $f(1,3) + f(4,4) = (|1 - 3| + |3 - 5|) + 0 = 4 + 0 = 4$.</p><p>In the second test case, we will group the villagers with suspicion $(1,9,12,4,7,2)$ into $(1),(9,12),(4,7,2)$. So, $f(1,1) + f(2,3) + f(4,6) = 0 + 3 + 8 = 11$.</p>
