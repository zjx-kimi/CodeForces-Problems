## Description

<div><p>Anya lives in the Flower City. By order of the city mayor, she has to build a fence for herself.</p><p>The fence consists of $n$ planks, each with a height of $a_i$ meters. According to the order, the heights of the planks must <span class="tex-font-style-bf">not increase</span>. In other words, it is true that $a_i \ge a_j$ for all $i &lt; j$.</p><p>Anya became curious whether her fence is <span class="tex-font-style-it">symmetrical</span> with respect to the diagonal. In other words, will she get the same fence if she lays all the planks horizontally in the same order.</p><p>For example, for $n = 5$, $a = [5, 4, 3, 2, 1]$, the fence is <span class="tex-font-style-it">symmetrical</span>. Because if all the planks are laid horizontally, the fence will be $[5, 4, 3, 2, 1]$, as shown in the diagram.</p><center> <img class="tex-graphics" src="file://FSrlRCO0.png" style="max-width: 100.0%;max-height: 100.0%;"><p> <span class="tex-font-size-small">On the left is the fence $[5, 4, 3, 2, 1]$, on the right is the same fence laid horizontally</span> </p></center><p>But for $n = 3$, $a = [4, 2, 1]$, the fence is not <span class="tex-font-style-it">symmetrical</span>. Because if all the planks are laid horizontally, the fence will be $[3, 2, 1, 1]$, as shown in the diagram.</p><center> <img class="tex-graphics" src="file://PbJAbaST.png" style="max-width: 100.0%;max-height: 100.0%;"><p> <span class="tex-font-size-small">On the left is the fence $[4, 2, 1]$, on the right is the same fence laid horizontally</span> </p></center> <p>Help Anya and determine whether her fence is <span class="tex-font-style-it">symmetrical</span>.</p></div><div class="input-specification"><p>The first line of the input contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. </p><p>The description of the test cases follows.</p><p>The first line of a test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the fence.</p><p>The second line of a test case contains $n$ integers $a_1 \ge a_2 \ge a_3 \ge \dots \ge a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the heights of the planks.</p><p>The sum of the values of $n$ for all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if the fence is <span class="tex-font-style-it">symmetrical</span>, otherwise output "<span class="tex-font-style-tt">NO</span>".</p><p>You can output each letter in any case (lowercase or uppercase). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be accepted as a positive answer.</p></div>

## Input

<p>The first line of the input contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. </p><p>The description of the test cases follows.</p><p>The first line of a test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the fence.</p><p>The second line of a test case contains $n$ integers $a_1 \ge a_2 \ge a_3 \ge \dots \ge a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the heights of the planks.</p><p>The sum of the values of $n$ for all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if the fence is <span class="tex-font-style-it">symmetrical</span>, otherwise output "<span class="tex-font-style-tt">NO</span>".</p><p>You can output each letter in any case (lowercase or uppercase). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be accepted as a positive answer.</p>





```input1|2,3,6,7,10,11,14,15
7
5
5 4 3 2 1
3
3 1 1
3
4 2 1
1
2
5
5 3 3 1 1
5
5 5 5 3 3
2
6 1
```




```output1
YES
YES
NO
NO
YES
YES
NO
```



## Note

<p>In the first and second test cases of the example, the fence is <span class="tex-font-style-it">symmetrical</span>.</p><p>In the third test case of the example, the fence is not <span class="tex-font-style-it">symmetrical</span>. If the planks are laid horizontally, the fence will be $[3, 2, 1, 1]$.</p><p>In the fourth test case of the example, the fence is not <span class="tex-font-style-it">symmetrical</span>. If the planks are laid horizontally, the fence will be $[1, 1]$.</p><p>In the fifth and sixth test cases of the example, the fence is <span class="tex-font-style-it">symmetrical</span>.</p><p>In the seventh test case of the example, the fence is not <span class="tex-font-style-it">symmetrical</span>. If the planks are laid horizontally, the fence will be $[2, 1, 1, 1, 1, 1]$.</p>
