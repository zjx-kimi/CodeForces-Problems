## Description

<div><p><span class="tex-font-style-bf">The easy and hard versions of this problem differ only in the constraints on $n$. In the easy version, the sum of values of $n^2$ over all test cases does not exceed $10^6$. Furthermore, $n$ does not exceed $1000$ in each test case</span>.</p><p>There are $2n$ light bulbs arranged in a row. Each light bulb has a color from $1$ to $n$ (<span class="tex-font-style-bf">exactly two light bulbs for each color</span>).</p><p>Initially, all light bulbs are turned off. You choose a set of light bulbs $S$ that you initially turn on. After that, you can perform the following operations in any order any number of times:</p><ul> <li> choose two light bulbs $i$ and $j$ <span class="tex-font-style-bf">of the same color</span>, exactly one of which is on, and turn on the second one; </li><li> choose three light bulbs $i, j, k$, such that both light bulbs $i$ and $k$ <span class="tex-font-style-bf">are on and have the same color</span>, and the light bulb $j$ is between them ($i &lt; j &lt; k$), and turn on the light bulb $j$. </li></ul><p>You want to choose a set of light bulbs $S$ that you initially turn on in such a way that by performing the described operations, you can ensure that all light bulbs are turned on.</p><p>Calculate two numbers:</p><ul> <li> the minimum size of the set $S$ that you initially turn on; </li><li> the number of sets $S$ of minimum size (taken modulo $998244353$). </li></ul></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then follow the descriptions of the test cases.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 1000$)&nbsp;— the number of pairs of light bulbs.</p><p>The second line of each test case contains $2n$ integers $c_1, c_2, \dots, c_{2n}$ ($1 \le c_i \le n$), where $c_i$ is the color of the $i$-th light bulb. For each color from $1$ to $n$, exactly two light bulbs have this color.</p><p>Additional constraint on the input: the sum of values of $n^2$ over all test cases does not exceed $10^6$.</p></div><div class="output-specification"><p>For each test case, output two integers:</p><ul> <li> the minimum size of the set $S$ that you initially turn on; </li><li> the number of sets $S$ of minimum size (taken modulo $998244353$). </li></ul></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then follow the descriptions of the test cases.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 1000$)&nbsp;— the number of pairs of light bulbs.</p><p>The second line of each test case contains $2n$ integers $c_1, c_2, \dots, c_{2n}$ ($1 \le c_i \le n$), where $c_i$ is the color of the $i$-th light bulb. For each color from $1$ to $n$, exactly two light bulbs have this color.</p><p>Additional constraint on the input: the sum of values of $n^2$ over all test cases does not exceed $10^6$.</p>

## Output

<p>For each test case, output two integers:</p><ul> <li> the minimum size of the set $S$ that you initially turn on; </li><li> the number of sets $S$ of minimum size (taken modulo $998244353$). </li></ul>





```input1|2,3,6,7
4
2
2 2 1 1
2
1 2 2 1
2
1 2 1 2
5
3 4 4 5 3 1 1 5 2 2
```




```output1
2 4
1 2
1 4
2 8
```


