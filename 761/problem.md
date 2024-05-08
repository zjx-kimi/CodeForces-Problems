## Description

<div><p>Li Hua wants to solve a problem about $\varphi$&nbsp;— Euler's totient function. Please recall that $\varphi(x)=\sum\limits_{i=1}^x[\gcd(i,x)=1]$.$^{\dagger,\ddagger}$</p><p>He has a sequence $a_1,a_2,\cdots,a_n$ and he wants to perform $m$ operations:</p><ul> <li> "1 $l$ $r$" ($1\le l\le r\le n$)&nbsp;— for <span class="tex-font-style-bf">each</span> $x\in[l,r]$, change $a_x$ into $\varphi(a_x)$. </li><li> "2 $l$ $r$" ($1\le l\le r\le n$)&nbsp;— find out the minimum changes needed to make sure $a_l=a_{l+1}=\cdots=a_r$. In each change, he chooses <span class="tex-font-style-bf">one</span> $x\in[l,r]$, change $a_x$ into $\varphi(a_x)$. Each operation of this type is independent, which means the array doesn't actually change. </li></ul><p>Suppose you were Li Hua, please solve this problem.</p><p>$^\dagger$ $\gcd(x,y)$ denotes the <a href="https://en.wikipedia.org/wiki/Greatest_common_divisor">greatest common divisor (GCD)</a> of integers $x$ and $y$. </p><p>$^\ddagger$ The notation $[\textrm{cond}]$ equals $1$ if the condition $\textrm{cond}$ is true, and $0$ otherwise.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $m$ ($1\le n,m\le 10^{5}$)&nbsp;— the number of elements in the array and the number of operations to process, respectively.</p><p>The second line contains $n$ integers $a_{1},a_{2},\cdots ,a_{n}$ ($1\le a_{i}\le 5\cdot 10^{6}$)&nbsp;— the elements of the array.</p><p>Next $m$ lines, each line contains three integers $t_{i},l_{i},r_{i}$ ($t_i\in\{1,2\},1\le l_i\le r_i\le n$)&nbsp;— the $i$-th operation. </p></div><div class="output-specification"><p>For each "2 $l$ $r$", output the answer in an separate line.</p></div>

## Input

<p>The first line contains two integers $n$ and $m$ ($1\le n,m\le 10^{5}$)&nbsp;— the number of elements in the array and the number of operations to process, respectively.</p><p>The second line contains $n$ integers $a_{1},a_{2},\cdots ,a_{n}$ ($1\le a_{i}\le 5\cdot 10^{6}$)&nbsp;— the elements of the array.</p><p>Next $m$ lines, each line contains three integers $t_{i},l_{i},r_{i}$ ($t_i\in\{1,2\},1\le l_i\le r_i\le n$)&nbsp;— the $i$-th operation. </p>

## Output

<p>For each "2 $l$ $r$", output the answer in an separate line.</p>





```input1
5 4
8 1 6 3 7
2 1 5
2 3 4
1 1 3
2 3 4
```




```output1
10
2
1
```



## Note

<p>Denote $\varphi^k(x)=\begin{cases}x,&amp;k=0\\\varphi(\varphi^{k-1}(x)),&amp;k &gt; 0\end{cases}$.</p><p>At first, $a=[8,1,6,3,7]$.</p><p>To make sure $a_1=a_2=a_3=a_4=a_5$, we can change $a$ to $a'=[\varphi^3(8),\varphi^0(1),\varphi^2(6),\varphi^2(3),\varphi^3(7)]=[1,1,1,1,1]$, using $3+0+2+2+3=10$ changes.</p><p>To make sure $a_3=a_4$, we can change $a$ to $a'=[\varphi^0(8),\varphi^0(1),\varphi^1(6),\varphi^1(3),\varphi^0(7)]=[8,1,2,2,7]$, using $0+0+1+1+0=2$ changes.</p><p>After "1 $1$ $3$", $a$ is changed to $a=[\varphi^1(8),\varphi^1(1),\varphi^1(6),\varphi^0(3),\varphi^0(7)]=[4,1,2,3,7]$.</p><p>To make sure $a_3=a_4$, we can change $a$ to $a'=[\varphi^0(4),\varphi^0(1),\varphi^0(2),\varphi^1(3),\varphi^0(7)]=[4,1,2,2,7]$, using $0+0+0+1+0=1$ change.</p>
