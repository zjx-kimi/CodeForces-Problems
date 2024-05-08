## Description

<div><p>You went to the store, selling $n$ types of chocolates. There are $a_i$ chocolates of type $i$ in stock.</p><p>You have unlimited amount of cash (so you are not restricted by any prices) and want to buy as many chocolates as possible. However if you buy $x_i$ chocolates of type $i$ (clearly, $0 \le x_i \le a_i$), then for all $1 \le j &lt; i$ at least one of the following must hold:</p><ul> <li> $x_j = 0$ (you bought zero chocolates of type $j$)</li><li> $x_j &lt; x_i$ (you bought less chocolates of type $j$ than of type $i$) </li></ul><p>For example, the array $x = [0, 0, 1, 2, 10]$ satisfies the requirement above (assuming that all $a_i \ge x_i$), while arrays $x = [0, 1, 0]$, $x = [5, 5]$ and $x = [3, 2]$ don't.</p><p>Calculate the maximum number of chocolates you can buy.</p></div><div class="input-specification"><p>The first line contains an integer $n$ ($1 \le n \le 2 \cdot 10^5$), denoting the number of types of chocolate.</p><p>The next line contains $n$ integers $a_i$ ($1 \le a_i \le 10^9$), denoting the number of chocolates of each type.</p></div><div class="output-specification"><p>Print the maximum number of chocolates you can buy.</p></div>

## Input

<p>The first line contains an integer $n$ ($1 \le n \le 2 \cdot 10^5$), denoting the number of types of chocolate.</p><p>The next line contains $n$ integers $a_i$ ($1 \le a_i \le 10^9$), denoting the number of chocolates of each type.</p>

## Output

<p>Print the maximum number of chocolates you can buy.</p>





```input1
5
1 2 1 3 6
```




```input2
5
3 2 5 4 10
```




```input3
4
1 1 1 1
```




```output1
10
```




```output2
20
```




```output3
1
```



## Note

<p>In the first example, it is optimal to buy: $0 + 0 + 1 + 3 + 6$ chocolates.</p><p>In the second example, it is optimal to buy: $1 + 2 + 3 + 4 + 10$ chocolates.</p><p>In the third example, it is optimal to buy: $0 + 0 + 0 + 1$ chocolates.</p>
