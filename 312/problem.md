## Description

<div><p>Aca and Milovan, two fellow competitive programmers, decided to give Vasilije a problem to test his skills.</p><p>Vasilije is given three positive integers: $n$, $k$, and $x$, and he has to determine if he can choose $k$ distinct integers between $1$ and $n$, such that their sum is equal to $x$.</p><p>Since Vasilije is now in the weirdest city in Serbia where Aca and Milovan live, Cacak, the problem seems weird to him. So he needs your help with this problem.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains three integers $n$, $k$ and $x$ ($1 \le n \le 2 \cdot 10^5$, $1 \le k \le n$, $1 \le x \le 4 \cdot 10^{10}$)&nbsp;— the maximum element he can choose, the number of elements he can choose and the sum he has to reach.</p><p>Note that the sum of $n$ over all test cases <span class="tex-font-style-bf">may exceed</span> $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case output one line: "<span class="tex-font-style-tt">YES</span>", if it is possible to choose $k$ distinct integers between $1$ and $n$, such that their sum is equal to $x$, and "<span class="tex-font-style-tt">NO</span>", if it isn't. </p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains three integers $n$, $k$ and $x$ ($1 \le n \le 2 \cdot 10^5$, $1 \le k \le n$, $1 \le x \le 4 \cdot 10^{10}$)&nbsp;— the maximum element he can choose, the number of elements he can choose and the sum he has to reach.</p><p>Note that the sum of $n$ over all test cases <span class="tex-font-style-bf">may exceed</span> $2 \cdot 10^5$.</p>

## Output

<p>For each test case output one line: "<span class="tex-font-style-tt">YES</span>", if it is possible to choose $k$ distinct integers between $1$ and $n$, such that their sum is equal to $x$, and "<span class="tex-font-style-tt">NO</span>", if it isn't. </p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p>





```input1|2,4,6,8,10,12
12
5 3 10
5 3 3
10 10 55
6 5 20
2 1 26
187856 87856 2609202300
200000 190000 19000000000
28 5 2004
2 2 2006
9 6 40
47202 32455 613407217
185977 145541 15770805980
```




```output1
YES
NO
YES
YES
NO
NO
YES
NO
NO
NO
YES
YES
```



## Note

<p>In the first test case $n = 5,\ k=3,\ x=10$, so we can choose the numbers: $2$, $3$, $5$, whose sum is $10$, so the answer is "<span class="tex-font-style-tt">YES</span>".</p><p>In the second test case $n = 5, \ k=3, \ x=3$, there is no three numbers which satisfies the condition, so the answer is "<span class="tex-font-style-tt">NO</span>". It can be shown that there are no three numbers whose sum is $3$.</p>
