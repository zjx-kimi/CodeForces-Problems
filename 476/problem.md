## Description

<div><p>In the summer, Vika likes to visit her country house. There is everything for relaxation: comfortable swings, bicycles, and a river.</p><p>There is a wooden bridge over the river, consisting of $n$ planks. It is quite old and unattractive, so Vika decided to paint it. And in the shed, they just found cans of paint of $k$ colors.</p><p>After painting each plank in one of $k$ colors, Vika was about to go swinging to take a break from work. However, she realized that the house was on the other side of the river, and the paint had not yet completely dried, so she could not walk on the bridge yet.</p><p>In order not to spoil the appearance of the bridge, Vika decided that she would still walk on it, but only stepping on planks of the same color. Otherwise, a small layer of paint on her sole will spoil the plank of another color. Vika also has a little paint left, but it will only be enough to repaint <span class="tex-font-style-bf">one</span> plank of the bridge.</p><p>Now Vika is standing on the ground in front of the first plank. To walk across the bridge, she will choose some planks of the same color (after repainting), which have numbers $1 \le i_1 &lt; i_2 &lt; \ldots &lt; i_m \le n$ (planks are numbered from $1$ from left to right). Then Vika will have to cross $i_1 - 1, i_2 - i_1 - 1, i_3 - i_2 - 1, \ldots, i_m - i_{m-1} - 1, n - i_m$ planks as a result of each of $m + 1$ steps.</p><p>Since Vika is afraid of falling, she does not want to take too long steps. Help her and tell her the minimum possible maximum number of planks she will have to cross <span class="tex-font-style-bf">in one step</span>, if she can repaint one (<span class="tex-font-style-bf">or zero</span>) plank a different color while crossing the bridge.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le k \le n \le 2 \cdot 10^5$)&nbsp;— the number of planks in the bridge and the number of different colors of paint.</p><p>The second line of each test case contains $n$ integers $c_1, c_2, c_3, \dots, c_n$ ($1 \le c_i \le k$)&nbsp;— the colors in which Vika painted the planks of the bridge.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the minimum possible maximum number of planks that Vika will have to step over in one step.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le k \le n \le 2 \cdot 10^5$)&nbsp;— the number of planks in the bridge and the number of different colors of paint.</p><p>The second line of each test case contains $n$ integers $c_1, c_2, c_3, \dots, c_n$ ($1 \le c_i \le k$)&nbsp;— the colors in which Vika painted the planks of the bridge.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the minimum possible maximum number of planks that Vika will have to step over in one step.</p>





```input1|2,3,6,7,10,11
5
5 2
1 1 2 1 1
7 3
1 2 3 3 3 2 1
6 6
1 2 3 4 5 6
8 4
1 2 3 4 2 3 1 4
3 1
1 1 1
```




```output1
0
1
2
2
0
```



## Note

<p>In the first test case, Vika can repaint the plank in the middle in color $1$ and walk across the bridge without stepping over any planks.</p><p>In the second test case, Vika can repaint the plank in the middle in color $2$ and walk across the bridge, stepping over only one plank each time.</p><p>In the third test case, Vika can repaint the penultimate plank in color $2$ and walk across the bridge, stepping only on planks with numbers $2$ and $5$. Then Vika will have to step over $1$, $2$ and $1$ plank each time she steps, so the answer is $2$.</p><p>In the fourth test case, Vika can simply walk across the bridge without repainting it, stepping over two planks each time, walking on planks of color $3$.</p><p>In the fifth test case, Vika can simply walk across the bridge without repainting it, without stepping over any planks.</p>
