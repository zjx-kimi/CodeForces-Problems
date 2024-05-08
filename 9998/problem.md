## Description

<div><p>You are in a nuclear laboratory that is about to explode and destroy the Earth. You must save the Earth before the final countdown reaches zero. </p><p>The countdown consists of $n$ ($1 \le n \le 4 \cdot 10^5$) mechanical indicators, each showing one decimal digit. You noticed that when the countdown changes its state from $x$ to $x-1$, it doesn't happen in one move. Instead, each change of a single digit takes one second. </p><p>So, for example, if the countdown shows <span class="tex-font-style-tt">42</span>, then it will change to <span class="tex-font-style-tt">41</span> in one second, because only one digit is changed, but if the countdown shows <span class="tex-font-style-tt">2300</span>, then it will change to <span class="tex-font-style-tt">2299</span> in three seconds, because the three last digits are changed.</p><p>Find out how much time is left before the countdown reaches zero.</p></div><div class="input-specification"><p>The first line of input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then the descriptions of the test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($1\le n\le 4\cdot 10^5$). </p><p>The second line contains a string of $n$ digits, the current state of the countdown. It is guaranteed that at least one digit is not zero.</p><p>The sum of $n$ for all tests does not exceed $4\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print a single integer without leading zeroes, the number of seconds left before the countdown reaches zero. Note that this number may be huge.</p></div>

## Input

<p>The first line of input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then the descriptions of the test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($1\le n\le 4\cdot 10^5$). </p><p>The second line contains a string of $n$ digits, the current state of the countdown. It is guaranteed that at least one digit is not zero.</p><p>The sum of $n$ for all tests does not exceed $4\cdot 10^5$.</p>

## Output

<p>For each test case, print a single integer without leading zeroes, the number of seconds left before the countdown reaches zero. Note that this number may be huge.</p>





```input1|2,3,6,7,10,11
5
2
42
5
12345
2
99
4
0005
27
456480697259671309012631002
```




```output1
46
13715
108
5
507200774732968121125145546
```



## Note

<p>In the first example, there are four changes that take 2 seconds: <span class="tex-font-style-tt">40</span> to <span class="tex-font-style-tt">39</span>, <span class="tex-font-style-tt">30</span> to <span class="tex-font-style-tt">29</span>, <span class="tex-font-style-tt">20</span> to <span class="tex-font-style-tt">19</span>, and <span class="tex-font-style-tt">10</span> to <span class="tex-font-style-tt">09</span>, other changes take 1 second each. So the total time is $2\cdot 4 + 1\cdot(42-4) = 46$.</p>
