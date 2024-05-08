## Description

<div><p>The universe is a coordinate plane. There are $n$ space highways, each of which is a straight line $y=kx$ passing through the origin $(0, 0)$. Also, there are $m$ asteroid belts on the plane, which we represent as open upwards parabolas, i.&nbsp;e. graphs of functions $y=ax^2+bx+c$, where $a &gt; 0$.</p><p>You want to photograph each parabola. To do this, for each parabola you need to choose a line that does not intersect this parabola and does not touch it. You can select the same line for different parabolas. Please find such a line for each parabola, or determine that there is no such line.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains $2$ integers $n$ and $m$ ($1 \le n, m \le 10^5$)&nbsp;—the number of lines and parabolas, respectively.</p><p>Each of the next $n$ lines contains one integer $k$ ($|k| \le 10^8$), denoting a line that is described with the equation $y=kx$. The lines are not necessarily distinct, $k$ can be equal to $0$.</p><p>Each of the next $m$ lines contains $3$ integers $a$, $b$, and $c$ ($a, |b|, |c| \le 10^8$, $a &gt; 0$)&nbsp;— coefficients of equations of the parabolas $ax^2+bx+c$. The parabolas are not necessarily distinct.</p><p>It is guaranteed that the sum $n$ over all test cases does not exceed $10^5$, and the sum $m$ over all test cases also does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output the answers for each parabola in the given order. If there is a line that does not intersect the given parabola and doesn't touch it, print on a separate line the word "<span class="tex-font-style-tt">YES</span>", and then on a separate line the number $k$&nbsp;— the coefficient of this line. If there are several answers, print any of them. If the line does not exist, print one word "<span class="tex-font-style-tt">NO</span>".</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p><p>The empty lines in the output in the example are given only for illustration, you do not need to output them (but you can).</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains $2$ integers $n$ and $m$ ($1 \le n, m \le 10^5$)&nbsp;—the number of lines and parabolas, respectively.</p><p>Each of the next $n$ lines contains one integer $k$ ($|k| \le 10^8$), denoting a line that is described with the equation $y=kx$. The lines are not necessarily distinct, $k$ can be equal to $0$.</p><p>Each of the next $m$ lines contains $3$ integers $a$, $b$, and $c$ ($a, |b|, |c| \le 10^8$, $a &gt; 0$)&nbsp;— coefficients of equations of the parabolas $ax^2+bx+c$. The parabolas are not necessarily distinct.</p><p>It is guaranteed that the sum $n$ over all test cases does not exceed $10^5$, and the sum $m$ over all test cases also does not exceed $10^5$.</p>

## Output

<p>For each test case, output the answers for each parabola in the given order. If there is a line that does not intersect the given parabola and doesn't touch it, print on a separate line the word "<span class="tex-font-style-tt">YES</span>", and then on a separate line the number $k$&nbsp;— the coefficient of this line. If there are several answers, print any of them. If the line does not exist, print one word "<span class="tex-font-style-tt">NO</span>".</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p><p>The empty lines in the output in the example are given only for illustration, you do not need to output them (but you can).</p>





```input1|2,3,4,5,11,12,13,17,18,19,20,21,22
5
1 2
1
1 -1 2
1 -1 3
2 2
1
4
1 2 1
2 5 1
1 1
0
1 0 0
1 1
100000000
100000000 100000000 100000000
2 3
0
2
2 2 1
1 -2 1
1 -2 -1
```




```output1
YES
1
YES
1

YES
1
YES
4

NO

YES
100000000

YES
0
NO
NO
```



## Note

<p>In the first test case, both parabolas do not intersect the only given line $y=1\cdot x$, so the answer is two numbers $1$.</p><center> <img class="tex-graphics" src="file://hCl8pJ01.png" style="max-width: 100.0%;max-height: 100.0%;" width="302px"> </center><p>In the second test case, the line $y=x$ and the parabola $2x^2+5x+1$ intersect, and also the line $y=4x$ and the parabola $x^2+2x+1$ touch, so these pairs do not satisfy the condition. So for the first parabola, the answer is $1$ ($y=1x$), and for the second parabola&nbsp;— $4$.</p><center> <img class="tex-graphics" src="file://5gEeNcYJ.png" style="max-width: 100.0%;max-height: 100.0%;" width="302px"> </center><p>In the third test set, the line and the parabola intersect, so the answer is "<span class="tex-font-style-tt">NO</span>".</p>
