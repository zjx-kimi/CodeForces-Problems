## Description

<div><p>After a successful year of milk production, Farmer John is rewarding his cows with their favorite treat: tasty grass!</p><p>On the field, there is a row of $n$ units of grass, each with a sweetness $s_i$. Farmer John has $m$ cows, each with a favorite sweetness $f_i$ and a hunger value $h_i$. He would like to pick two disjoint subsets of cows to line up on the left and right side of the grass row. There is no restriction on how many cows must be on either side. The cows will be treated in the following manner: </p><ul> <li> The cows from the left and right side will take turns feeding in an order decided by Farmer John. </li><li> When a cow feeds, it walks towards the other end without changing direction and eats grass of its favorite sweetness until it eats $h_i$ units. </li><li> The moment a cow eats $h_i$ units, it will fall asleep there, preventing further cows from passing it from both directions. </li><li> If it encounters another sleeping cow or reaches the end of the grass row, it will get upset. Farmer John absolutely does not want any cows to get upset. </li></ul><p>Note that grass does not grow back. Also, to prevent cows from getting upset, not every cow has to feed since FJ can choose a subset of them. </p><p>Surprisingly, FJ has determined that sleeping cows are the most satisfied. If FJ orders optimally, what is the maximum number of sleeping cows that can result, and how many ways can FJ choose the subset of cows on the left and right side to achieve that maximum number of sleeping cows (modulo $10^9+7$)? The order in which FJ sends the cows does not matter as long as no cows get upset. </p></div><div class="input-specification"><p>The first line contains two integers $n$ and $m$ ($1 \le n \le 5000$, $1 \le m \le 5000$) &nbsp;— the number of units of grass and the number of cows. </p><p>The second line contains $n$ integers $s_1, s_2, \ldots, s_n$ ($1 \le s_i \le n$) &nbsp;— the sweetness values of the grass.</p><p>The $i$-th of the following $m$ lines contains two integers $f_i$ and $h_i$ ($1 \le f_i, h_i \le n$) &nbsp;— the favorite sweetness and hunger value of the $i$-th cow. <span class="tex-font-style-bf">No two cows have the same hunger and favorite sweetness simultaneously</span>.</p></div><div class="output-specification"><p>Output two integers &nbsp;— the maximum number of sleeping cows that can result and the number of ways modulo $10^9+7$. </p></div>

## Input

<p>The first line contains two integers $n$ and $m$ ($1 \le n \le 5000$, $1 \le m \le 5000$) &nbsp;— the number of units of grass and the number of cows. </p><p>The second line contains $n$ integers $s_1, s_2, \ldots, s_n$ ($1 \le s_i \le n$) &nbsp;— the sweetness values of the grass.</p><p>The $i$-th of the following $m$ lines contains two integers $f_i$ and $h_i$ ($1 \le f_i, h_i \le n$) &nbsp;— the favorite sweetness and hunger value of the $i$-th cow. <span class="tex-font-style-bf">No two cows have the same hunger and favorite sweetness simultaneously</span>.</p>

## Output

<p>Output two integers &nbsp;— the maximum number of sleeping cows that can result and the number of ways modulo $10^9+7$. </p>





```input1
5 2
1 1 1 1 1
1 2
1 3
```




```input2
5 2
1 1 1 1 1
1 2
1 4
```




```input3
3 2
2 3 2
3 1
2 1
```




```input4
5 1
1 1 1 1 1
2 5
```




```output1
2 2
```




```output2
1 4
```




```output3
2 4
```




```output4
0 1
```



## Note

<p>In the first example, FJ can line up the cows as follows to achieve $2$ sleeping cows: </p><ul> <li> Cow $1$ is lined up on the left side and cow $2$ is lined up on the right side. </li><li> Cow $2$ is lined up on the left side and cow $1$ is lined up on the right side. </li></ul><p>In the second example, FJ can line up the cows as follows to achieve $1$ sleeping cow: </p><ul> <li> Cow $1$ is lined up on the left side. </li><li> Cow $2$ is lined up on the left side. </li><li> Cow $1$ is lined up on the right side. </li><li> Cow $2$ is lined up on the right side. </li></ul><p>In the third example, FJ can line up the cows as follows to achieve $2$ sleeping cows: </p><ul> <li> Cow $1$ and $2$ are lined up on the left side. </li><li> Cow $1$ and $2$ are lined up on the right side. </li><li> Cow $1$ is lined up on the left side and cow $2$ is lined up on the right side. </li><li> Cow $1$ is lined up on the right side and cow $2$ is lined up on the left side. </li></ul><p>In the fourth example, FJ cannot end up with any sleeping cows, so there will be no cows lined up on either side.</p>
