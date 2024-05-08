## Description

<div><p>Tokitsukaze and her friends are trying to infiltrate a secret base built by Claris. However, Claris has been aware of that and set a bomb which is going to explode in a minute. Although they try to escape, they have no place to go after they find that the door has been locked.</p><p>At this very moment, CJB, Father of Tokitsukaze comes. With his magical power given by Ereshkigal, the goddess of the underworld, CJB is able to set $m$ barriers to protect them from the explosion. Formally, let's build a Cartesian coordinate system on the plane and assume the bomb is at $O(0, 0)$. There are $n$ persons in Tokitsukaze's crew, the $i$-th one of whom is at $P_i(X_i, Y_i)$. Every barrier can be considered as a line with infinity length and they can intersect each other. For every person from Tokitsukaze's crew, there must be at least one barrier separating the bomb and him, which means the line between the bomb and him intersects with at least one barrier. In this definition, if there exists a person standing at the position of the bomb, any line through $O(0, 0)$ will satisfy the requirement.</p><p>Although CJB is very powerful, he still wants his barriers to be as far from the bomb as possible, in order to conserve his energy. Please help him calculate the maximum distance between the bomb and the closest barrier while all of Tokitsukaze's crew are safe.</p></div><div class="input-specification"><p>The first line contains two integers $n$, $m$ ($1 \leq n, m \leq 10^5$), indicating the number of people and the number of barriers respectively.</p><p>The $i$-th line of the next $n$ lines contains two integers $X_i$, $Y_i$ ($-10^5 \leq X_i, Y_i \leq 10^5$), indicating the $i$-th person's location $P_i(X_i, Y_i)$. Note that $P_i$ may have the same coordinates as $P_j$ ($j \neq i$) or even $O$.</p></div><div class="output-specification"><p>Print a single real number&nbsp;— the maximum distance meeting the requirement. Your answer is considered correct if its absolute or relative error does not exceed $10^{-6}$.</p><p>Formally, let your answer be $a$, and the jury's answer be $b$. Your answer is accepted if and only if $\frac{|a - b|}{\max(1, |b|)} \leq 10^{-6}$.</p></div>

## Input

<p>The first line contains two integers $n$, $m$ ($1 \leq n, m \leq 10^5$), indicating the number of people and the number of barriers respectively.</p><p>The $i$-th line of the next $n$ lines contains two integers $X_i$, $Y_i$ ($-10^5 \leq X_i, Y_i \leq 10^5$), indicating the $i$-th person's location $P_i(X_i, Y_i)$. Note that $P_i$ may have the same coordinates as $P_j$ ($j \neq i$) or even $O$.</p>

## Output

<p>Print a single real number&nbsp;— the maximum distance meeting the requirement. Your answer is considered correct if its absolute or relative error does not exceed $10^{-6}$.</p><p>Formally, let your answer be $a$, and the jury's answer be $b$. Your answer is accepted if and only if $\frac{|a - b|}{\max(1, |b|)} \leq 10^{-6}$.</p>





```input1
3 1
2 0
0 2
-1 0
```




```input2
1 1
0 0
```




```input3
2 1
-1 -1
-1 -1
```




```input4
3 100000
3 2
-1 -3
2 -5
```




```output1
0.0000000000
```




```output2
0.0000000000
```




```output3
1.4142135617
```




```output4
3.1622776602
```



## Note

<p>In the first two examples, CJB must set the barrier crossing $O(0, 0)$.</p><p>In the last two examples, CJB can set each barrier crossing some $P_i$ such that the barrier is perpendicular to the line between $P_i$ and $O$.</p>
