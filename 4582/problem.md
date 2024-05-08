## Description

<div><p>At the children's festival, children were dancing in a circle. When music stopped playing, the children were still standing in a circle. Then Lena remembered, that her parents gave her a candy box with exactly $k$ candies "Wilky&nbsp;May". Lena is not a greedy person, so she decided to present all her candies to her friends in the circle. Lena knows, that some of her friends have a sweet tooth and others do not. Sweet tooth takes out of the box two candies, if the box has at least two candies, and otherwise takes one. The rest of Lena's friends always take exactly one candy from the box.</p><p>Before starting to give candies, Lena step out of the circle, after that there were exactly $n$ people remaining there. Lena numbered her friends in a clockwise order with positive integers starting with $1$ in such a way that index $1$ was assigned to her best friend Roma.</p><p>Initially, Lena gave the box to the friend with number $l$, after that each friend (starting from friend number $l$) took candies from the box and passed the box to the next friend in clockwise order. The process ended with the friend number $r$ taking the last candy (or two, who knows) and the empty box. Please note that it is possible that some of Lena's friends took candy from the box several times, that is, the box could have gone several full circles before becoming empty.</p><p>Lena does not know which of her friends have a sweet tooth, but she is interested in the maximum possible number of friends that can have a sweet tooth. If the situation could not happen, and Lena have been proved wrong in her observations, please tell her about this.</p></div><div class="input-specification"><p>The only line contains four integers $n$, $l$, $r$ and $k$ ($1 \le n, k \le 10^{11}$, $1 \le l, r \le n$)&nbsp;— the number of children in the circle, the number of friend, who was given a box with candies, the number of friend, who has taken last candy and the initial number of candies in the box respectively.</p></div><div class="output-specification"><p>Print exactly one integer&nbsp;— the maximum possible number of sweet tooth among the friends of Lena or "<span class="tex-font-style-tt">-1</span>" (quotes for clarity), if Lena is wrong.</p></div>

## Input

<p>The only line contains four integers $n$, $l$, $r$ and $k$ ($1 \le n, k \le 10^{11}$, $1 \le l, r \le n$)&nbsp;— the number of children in the circle, the number of friend, who was given a box with candies, the number of friend, who has taken last candy and the initial number of candies in the box respectively.</p>

## Output

<p>Print exactly one integer&nbsp;— the maximum possible number of sweet tooth among the friends of Lena or "<span class="tex-font-style-tt">-1</span>" (quotes for clarity), if Lena is wrong.</p>





```input1
4 1 4 12

```




```input2
5 3 4 10

```




```input3
10 5 5 1

```




```input4
5 4 5 6

```




```output1
2

```




```output2
3

```




```output3
10

```




```output4
-1

```



## Note

<p>In the first example, any two friends can be sweet tooths, this way each person will receive the box with candies twice and the last person to take sweets will be the fourth friend.</p><p>In the second example, sweet tooths can be any three friends, except for the friend on the third position.</p><p>In the third example, only one friend will take candy, but he can still be a sweet tooth, but just not being able to take two candies. All other friends in the circle can be sweet tooths as well, they just will not be able to take a candy even once.</p><p>In the fourth example, Lena is wrong and this situation couldn't happen.</p>
