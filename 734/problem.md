## Description

<div> Berland&nbsp;— is a huge country consisting of $n$ cities. The road network of Berland can be represented as a root tree, that is, there is only $n - 1$ road in the country, and you can get from any city to any other exactly one way, if you do not visit any city twice. For the convenience of representing the country, for each city $i$, the city $p_i$ is fixed, equal to the first city to which you need to go from the city $i$ to get to the city $1$. In other words, the city $p_i$ is equal to the ancestor of the city $i$ if the tree is hung for the city $1$.<p>There is one gas station in each city of Berland. Gas stations have special pricing, and for each gas station there is a fixed range of prices for which they are ready to sell gasoline. A gas station in the city with the number $i$ is ready to sell gasoline at any price from $l_i$ to $r_i$ inclusive.</p><p>The King of Berland&nbsp;— is an exemplary family man, and for $m$ years, two sons were born to him every year. The king's children have been involved in public affairs since early childhood, and at the end of each year they check the honesty of gasoline prices. From birth, the king's children, who are born in the year $i$, are responsible for checking gasoline prices on the ways from the city of $a_i$ to the city of $b_i$ and from the city of $c_i$ to the city of $d_i$, respectively.</p><p>The check is as follows: both children simultaneously start their journey from the cities $a_i$ and $c_i$, respectively. The first son of the king, born in the year $i$, moves along the path from the city $a_i$ to the city $b_i$, and the second &nbsp;— from the city $c_i$ to the city $d_i$. Children check that the price of gasoline in the city of $a_i$ coincides with the price of gasoline in the city of $c_i$. Next, they check that the price of gasoline in the second city on the way from $a_i$ to $b_i$ coincides with the price in the second city on the way from $c_i$ to $d_i$. Then they repeat the same thing for a couple of third cities on their paths and so on. At the end, they check that the price of gasoline in the city of $b_i$ coincides with the price of gasoline in the city of $d_i$. It is guaranteed that the length of the path from the city $a_i$ to the city $b_i$ coincides with the length of the path from the city $c_i$ to the city $d_i$.</p><p>Gas stations must strictly obey the laws, and therefore all checks of gasoline prices should not reveal violations. Help Berland gas stations find out how many ways they can set gasoline prices for $m$ years. In other words, for each $i$ from $1$ to $m$, calculate how many ways you can set gasoline prices at all gas stations so that after the birth of the first $i$ pairs of the king's children, all their checks did not reveal violations, and at any gas station the price was in the acceptable price range. Since the number of such methods can be large, calculate the answer modulo $10^9 + 7$. </p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($1 \le n \le 200\,000$)&nbsp;— the number of cities in Berland.</p><p>The second line contains $(n - 1)$ numbers $p_2,\ p_3,\ p_4,\ \ldots,\ p_n$ ($1 \le p_i \le n$), where $p_i$ denotes the number of the next city on the way from city $i$ to city $1$.</p><p>In each of the following lines, two integers are given $l_i$ and $r_i$ ($1 \le l_i \le r_i &lt; 10^9+7$), specifying the acceptable range of prices at the gas station number $i$.</p><p>The following line contains a single integer $m$ ($1 \le m \le 200\,000$)&nbsp;— the number of years during which two sons were born to the king.</p><p>In each of the following $m$ lines, four integers are given $a_i$, $b_i$, $c_i$ and $d_i$ ($1 \le a_i, b_i, c_i, d_i \le n$), specifying two paths on which the king's children will check gasoline prices, born in the year $i$. It is guaranteed that the length of the path between the cities $a_i$ and $b_i$ is equal to the length of the path between the cities $c_i$ and $d_i$. </p></div><div class="output-specification"><p>In $m$ lines, print one number each. The number in the $i$ line should be equal to the number of ways to set gasoline prices in all cities so that the king's children born in the years up to and including $i$ do not reveal violations in inspections. Output the numbers modulo $10^9 + 7$. </p></div>

## Input

<p>The first line contains a single integer $n$ ($1 \le n \le 200\,000$)&nbsp;— the number of cities in Berland.</p><p>The second line contains $(n - 1)$ numbers $p_2,\ p_3,\ p_4,\ \ldots,\ p_n$ ($1 \le p_i \le n$), where $p_i$ denotes the number of the next city on the way from city $i$ to city $1$.</p><p>In each of the following lines, two integers are given $l_i$ and $r_i$ ($1 \le l_i \le r_i &lt; 10^9+7$), specifying the acceptable range of prices at the gas station number $i$.</p><p>The following line contains a single integer $m$ ($1 \le m \le 200\,000$)&nbsp;— the number of years during which two sons were born to the king.</p><p>In each of the following $m$ lines, four integers are given $a_i$, $b_i$, $c_i$ and $d_i$ ($1 \le a_i, b_i, c_i, d_i \le n$), specifying two paths on which the king's children will check gasoline prices, born in the year $i$. It is guaranteed that the length of the path between the cities $a_i$ and $b_i$ is equal to the length of the path between the cities $c_i$ and $d_i$. </p>

## Output

<p>In $m$ lines, print one number each. The number in the $i$ line should be equal to the number of ways to set gasoline prices in all cities so that the king's children born in the years up to and including $i$ do not reveal violations in inspections. Output the numbers modulo $10^9 + 7$. </p>





```input1
5
1 1 2 2
2 4
1 3
1 3
2 4
4 4
4
1 1 2 2
1 2 2 1
3 4 4 3
3 4 3 5
```




```input2
8
1 2 3 4 5 8 6
3 7
2 6
3 8
5 10
5 8
2 9
3 8
6 8
4
1 3 7 6
4 1 5 7
1 7 7 1
1 8 2 7
```




```output1
18
18
4
0
```




```output2
720
120
120
1
```



## Note

<p>Consider the first example.</p><p>After the birth of the first two sons, the prices in the cities of $1$ and $2$ should be equal. In total, there are 2 ways to choose the same gasoline price for the cities of $1$ and $2$ so that it falls within the acceptable price range for these cities. So, there are only ways to set gasoline prices: $2 \cdot 3 \cdot 3 \cdot 1 = 18$.</p><p>The second pair of sons will check the prices on the paths $1 - 2$ and $2 - 1$. This means that gasoline prices in the cities of $1$ and $2$ must match, which is already being done. Therefore, after the birth of the second pair of sons, the answer did not change in any way.</p><p>The third pair of sons will check the prices on the tracks $3 - 1 - 2 - 4$ and $4 - 2 - 1 - 3$. Then the price of non-gasoline in the city of $3$ should be equal to the price in the city of $4$, and the price in the city of $1$ should be equal to the price in the city of $2$. Prices in the cities of $1$ and $2$ are already the same. For the cities of $3$ and $4$, there are 2 ways to choose the same price for gasoline so that it falls within the acceptable price range for these cities. So, there are only ways to set gasoline prices: $2 \cdot 2 \cdot 1 = 4$.  The fourth pair of sons will check the prices on the tracks $3 - 1 - 2 - 4$ and $3 - 1 - 2 - 5$. This means that the prices in the cities of $4$ and $5$ should be equal, and since the prices in the cities of $3$ and $4$ already coincide, then in the cities of $3$, $4$ and $5$ there should be the same price for gasoline. The price of gasoline in the city of $3$ should be no more than 3, and the price of gasoline in the city of $5$ should be no less than 4. So, after the birth of the fourth pair of sons, there are no ways to set gasoline prices so that all checks are carried out and prices are in the required ranges. </p>
