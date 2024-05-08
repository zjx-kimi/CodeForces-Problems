## Description

<div><p>Grandfather Ahmed's School has $n+1$ students. The students are divided into $k$ classes, and $s_i$ students study in the $i$-th class. So, $s_1 + s_2 + \ldots + s_k = n+1$.</p><p>Due to the upcoming April Fools' Day, all students will receive gifts!</p><p>Grandfather Ahmed planned to order $n+1$ boxes of gifts. Each box can contain one or more gifts. He plans to distribute the boxes between classes so that the following conditions are satisfied:</p><ol> <li> Class number $i$ receives <span class="tex-font-style-bf">exactly</span> $s_i$ boxes (so that each student can open exactly one box). </li><li> The total number of gifts in the boxes received by the $i$-th class should be a multiple of $s_i$ (it should be possible to equally distribute the gifts among the $s_i$ students of this class). </li></ol><p>Unfortunately, Grandfather Ahmed ordered only $n$ boxes with gifts, the $i$-th of which contains $a_i$ gifts.</p><p>Ahmed has to buy the missing gift box, and the number of gifts in the box should be an integer between $1$ and $10^6$. Help Ahmed to determine, how many gifts should the missing box contain, and build a suitable distribution of boxes to classes, or report that this is impossible.</p></div><div class="input-specification"><p>The first line of the input contains two integers $n$ and $k$ ($1 \le n, k \le 200$, $k \le n + 1$).</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^6$)&nbsp;— the number of gifts in the available boxes.</p><p>The third line contains $k$ integers $s_1, s_2, \ldots, s_k$ ($1 \le s_i \le n+1$)&nbsp;— the number of students in classes. It is guaranteed that $\sum s_i = n+1$.</p></div><div class="output-specification"><p>If there is no way to buy the remaining box, output the integer $-1$ in a single line.</p><p>Otherwise, in the first line, output a single integer $s$&nbsp;— the number of gifts in the box that Grandfather Ahmed should buy ($1 \le s \le 10^6$).</p><p>Next, in $k$ lines, print the distribution of boxes to classes. In the $i$-th line print $s_i$ integers&nbsp;— the sizes of the boxes that should be sent to the $i$-th class.</p><p>If there are multiple solutions, print any of them.</p></div>

## Input

<p>The first line of the input contains two integers $n$ and $k$ ($1 \le n, k \le 200$, $k \le n + 1$).</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^6$)&nbsp;— the number of gifts in the available boxes.</p><p>The third line contains $k$ integers $s_1, s_2, \ldots, s_k$ ($1 \le s_i \le n+1$)&nbsp;— the number of students in classes. It is guaranteed that $\sum s_i = n+1$.</p>

## Output

<p>If there is no way to buy the remaining box, output the integer $-1$ in a single line.</p><p>Otherwise, in the first line, output a single integer $s$&nbsp;— the number of gifts in the box that Grandfather Ahmed should buy ($1 \le s \le 10^6$).</p><p>Next, in $k$ lines, print the distribution of boxes to classes. In the $i$-th line print $s_i$ integers&nbsp;— the sizes of the boxes that should be sent to the $i$-th class.</p><p>If there are multiple solutions, print any of them.</p>





```input1
4 2
7 7 7 127
2 3
```




```input2
18 4
1 2 3 4 5 6 7 8 9 1 2 3 4 5 6 7 8 9
6 1 9 3
```




```output1
1
7 7 
7 127 1
```




```output2
9
7 1 7 6 5 4 
9 
1 2 3 8 3 2 9 8 9 
6 5 4
```



## Note

<p>In the first test, Grandfather Ahmed can buy a box with just $1$ gift. After that, two boxes with $7$ gifts are sent to the first class. $7 + 7 = 14$ is divisible by $2$. And the second class gets boxes with $1, 7, 127$ gifts. $1 + 7 + 127 = 135$ is evenly divisible by $3$.</p><p>In the second test, the classes have sizes $6$, $1$, $9$, and $3$. We show that the available boxes are enough to distribute into classes with sizes $6$, $9$, $3$, and in the class with size $1$, you can buy a box of any size. In class with size $6$ we send boxes with sizes $7$, $1$, $7$, $6$, $5$, $4$. $7 + 1 + 7 + 6 + 5 + 4 = 30$ is divisible by $6$. In class with size $9$ we send boxes with sizes $1$, $2$, $3$, $8$, $3$, $2$, $9$, $8$, $9$. $1 + 2 + 3 + 8 + 3 + 2 + 9 + 8 + 9 = 45$ is divisible by $9$. The remaining boxes ($6$, $5$, $4$) are sent to the class with size $3$. $6 + 5 + 4 = 15$ is divisible by $3$.</p>
