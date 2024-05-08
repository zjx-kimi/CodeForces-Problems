## Description

<div><p>Once upon a time, bartender Decim found three threadlets and a pair of scissors.</p><p>In one operation, Decim chooses any threadlet and cuts it into two threadlets, whose lengths are <span class="tex-font-style-bf">positive integers</span> and their sum is <span class="tex-font-style-bf">equal</span> to the length of the threadlet being cut.</p><p>For example, he can cut a threadlet of length $5$ into threadlets of lengths $2$ and $3$, but he cannot cut it into threadlets of lengths $2.5$ and $2.5$, or lengths $0$ and $5$, or lengths $3$ and $4$.</p><p>Decim can perform <span class="tex-font-style-bf">at most</span> three operations. He is allowed to cut the threadlets obtained from previous cuts. Will he be able to make all the threadlets of equal length?</p></div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then follows the description of each test case.</p><p>In a single line of each test case, there are three integers $a$, $b$, $c$ ($1 \le a, b, c \le 10^9$)&nbsp;— the lengths of the threadlets.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if it is possible to make all the threadlets of equal length by performing at most three operations, otherwise output "<span class="tex-font-style-tt">NO</span>".</p><p>You can output "<span class="tex-font-style-tt">YES</span>" and "<span class="tex-font-style-tt">NO</span>" in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then follows the description of each test case.</p><p>In a single line of each test case, there are three integers $a$, $b$, $c$ ($1 \le a, b, c \le 10^9$)&nbsp;— the lengths of the threadlets.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if it is possible to make all the threadlets of equal length by performing at most three operations, otherwise output "<span class="tex-font-style-tt">NO</span>".</p><p>You can output "<span class="tex-font-style-tt">YES</span>" and "<span class="tex-font-style-tt">NO</span>" in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p>





```input1|2,4,6,8,10,12,14,16
15
1 3 2
5 5 5
6 36 12
7 8 7
6 3 3
4 4 12
12 6 8
1000000000 1000000000 1000000000
3 7 1
9 9 1
9 3 6
2 8 2
5 3 10
8 4 8
2 8 4
```




```output1
YES
YES
NO
NO
YES
YES
NO
YES
NO
NO
YES
YES
NO
YES
NO
```



## Note

<p>Let's consider some testcases of the first test.</p><p>In the first testcase, you can apply following operations:</p><p>$1, 3, 2 \to 1, 2, 1, 2 \to 1, 1, 1, 1, 2 \to 1, 1, 1, 1, 1, 1$.</p><p>In the second testcase, you can do nothing, the threadlets are already of equal length.</p><p>In the third testcase, it isn't possible to make threadlets of equal length.</p>
