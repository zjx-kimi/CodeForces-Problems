## Description

<div><p>As you know, Martian scientists are actively engaged in space research. One of the highest priorities is Pluto. In order to study this planet in more detail, it was decided to build a laboratory on Pluto.</p><p>It is known that the lab will be built of $n$ square blocks of equal size. For convenience, we will assume that Pluto's surface is a plane divided by vertical and horizontal lines into unit squares. Each square is either occupied by a lab block or not, and only $n$ squares are occupied.</p><p>Since each block is square, it has four walls. If a wall is adjacent to another block, it is considered <span class="tex-font-style-it">inside</span>, otherwise&nbsp;— <span class="tex-font-style-it">outside</span>.</p><p>Pluto is famous for its extremely cold temperatures, so the outside walls of the lab must be insulated. One unit of insulation per exterior wall would be required. Thus, the greater the total length of the outside walls of the lab (i.&nbsp;e., its perimeter), the more insulation will be needed.</p><p>Consider the lab layout in the figure below. It shows that the lab consists of $n = 33$ blocks, and all the blocks have a total of $24$ outside walls, i.&nbsp;e. $24$ units of insulation will be needed.</p><p>You should build the lab optimally, i.&nbsp;e., minimize the amount of insulation. On the other hand, there may be many optimal options, so scientists may be interested in the number of ways to build the lab using the minimum amount of insulation, modulo a prime number $m$.</p><p>Two ways are considered the same if they are the same when overlapping without turning. Thus, if a lab plan is rotated by $90^{\circ}$, such a new plan can be considered a separate way.</p><p>To help scientists explore Pluto, you need to write a program that solves these difficult problems.</p><center> <img class="tex-graphics" src="file://onp2H63Y.png" style="max-width: 100.0%;max-height: 100.0%;"> </center></div><div class="input-specification"><p>The first line contains two integers $t$ and $u$ ($1 \le t \le 2\cdot 10^5$, $1 \le u \le 2$)&nbsp;— the number of test cases and the test type. If $u=1$, you need to find any way to build the lab in an optimal way, and if $u=2$, you need to calculate the number of ways to do it.</p><p>If $u=2$, then in the following line of input there is a prime integer $m$ ($10^8 \le m \le 10^9 + 9$), modulo which you need to calculate the number of ways.</p><p>Each of the following $t$ lines of input contains a description of a test case consisting of one integer $n$ ($1 \le n \le 4\cdot 10^5$)&nbsp;— the number of blocks the lab should consist of.</p><p>It is guaranteed that if $u=1$, then the sum of $n$ on all test cases does not exceed $8\cdot10^5$.</p></div><div class="output-specification"><p>For each test case, output the answers in the format below, separating them with a newline. The output format depends on $u$ in the input data.</p><p>If $u=1$, in the first line you need to print two integers $h$ and $w$&nbsp;—the height and width of the area in which the lab should be built. Then, in each of the following $h$ lines, you must output a line $s_i$ consisting of $w$ characters "<span class="tex-font-style-tt">#</span>" and "<span class="tex-font-style-tt">.</span>". If the $j$-th character of the row $s_i$ is "<span class="tex-font-style-tt">#</span>", then the corresponding square must contain a block of laboratory, otherwise, it is considered empty. Thus, we get a matrix of symbols. The condition must also be met that the first and last rows of the matrix, as well as the first and last columns, must have at least one character "<span class="tex-font-style-tt">#</span>", otherwise we could output the same lab layout, but with smaller $h$ and $w$. If there are many options to build an optimal lab, you can print any of them.</p><p>If $u=2$, you need to print two integers $p$ and $c$&nbsp;— the number of outside walls in an optimal lab, and the remainder of the number of ways by prime modulo $m$.</p></div>

## Input

<p>The first line contains two integers $t$ and $u$ ($1 \le t \le 2\cdot 10^5$, $1 \le u \le 2$)&nbsp;— the number of test cases and the test type. If $u=1$, you need to find any way to build the lab in an optimal way, and if $u=2$, you need to calculate the number of ways to do it.</p><p>If $u=2$, then in the following line of input there is a prime integer $m$ ($10^8 \le m \le 10^9 + 9$), modulo which you need to calculate the number of ways.</p><p>Each of the following $t$ lines of input contains a description of a test case consisting of one integer $n$ ($1 \le n \le 4\cdot 10^5$)&nbsp;— the number of blocks the lab should consist of.</p><p>It is guaranteed that if $u=1$, then the sum of $n$ on all test cases does not exceed $8\cdot10^5$.</p>

## Output

<p>For each test case, output the answers in the format below, separating them with a newline. The output format depends on $u$ in the input data.</p><p>If $u=1$, in the first line you need to print two integers $h$ and $w$&nbsp;—the height and width of the area in which the lab should be built. Then, in each of the following $h$ lines, you must output a line $s_i$ consisting of $w$ characters "<span class="tex-font-style-tt">#</span>" and "<span class="tex-font-style-tt">.</span>". If the $j$-th character of the row $s_i$ is "<span class="tex-font-style-tt">#</span>", then the corresponding square must contain a block of laboratory, otherwise, it is considered empty. Thus, we get a matrix of symbols. The condition must also be met that the first and last rows of the matrix, as well as the first and last columns, must have at least one character "<span class="tex-font-style-tt">#</span>", otherwise we could output the same lab layout, but with smaller $h$ and $w$. If there are many options to build an optimal lab, you can print any of them.</p><p>If $u=2$, you need to print two integers $p$ and $c$&nbsp;— the number of outside walls in an optimal lab, and the remainder of the number of ways by prime modulo $m$.</p>





```input1|2,4
3 1
1
2
7
```




```input2|3,5
3 2
1000000007
1
2
7
```




```output1
1 1
#
1 2
##
2 4
.###
####
```




```output2
4 1
6 2
12 22
```



## Note

<p>Consider the second example.</p><p>If $n=1$, the only way to build a lab is to place a single block. In this case, the perimeter will be equal to four.</p><p>When $n=2$, you must place two blocks side by side. This can be done either vertically or horizontally, so there are two ways. It is easy to see that the lab has six outside walls in this case.</p><p>For $n=7$, all the $22$ optimal plans are shown in the picture below.</p><center> <img class="tex-graphics" src="file://th53cMWT.png" style="max-width: 100.0%;max-height: 100.0%;"> </center>
