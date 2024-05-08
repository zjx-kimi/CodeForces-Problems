## Description

<div><p>Petr likes to come up with problems about randomly generated data. This time problem is about random permutation. He decided to generate a random permutation this way: he takes identity permutation of numbers from $1$ to $n$ and then $3n$ times takes a random pair of different elements and swaps them. Alex envies Petr and tries to imitate him in all kind of things. Alex has also come up with a problem about random permutation. He generates a random permutation just like Petr but swaps elements $7n+1$ times instead of $3n$ times. Because it is more random, OK?!</p><p>You somehow get a test from one of these problems and now you want to know from which one.</p></div><div class="input-specification"><p>In the first line of input there is one integer $n$ ($10^{3} \le n \le 10^{6}$).</p><p>In the second line there are $n$ distinct integers between $1$ and $n$&nbsp;— the permutation of size $n$ from the test.</p><p>It is guaranteed that all tests except for sample are generated this way: First we choose $n$&nbsp;— the size of the permutation. Then we randomly choose a method to generate a permutation&nbsp;— the one of Petr or the one of Alex. Then we generate a permutation using chosen method.</p></div><div class="output-specification"><p>If the test is generated via Petr's method print "<span class="tex-font-style-tt">Petr</span>" (without quotes). If the test is generated via Alex's method print "<span class="tex-font-style-tt">Um_nik</span>" (without quotes).</p></div>

## Input

<p>In the first line of input there is one integer $n$ ($10^{3} \le n \le 10^{6}$).</p><p>In the second line there are $n$ distinct integers between $1$ and $n$&nbsp;— the permutation of size $n$ from the test.</p><p>It is guaranteed that all tests except for sample are generated this way: First we choose $n$&nbsp;— the size of the permutation. Then we randomly choose a method to generate a permutation&nbsp;— the one of Petr or the one of Alex. Then we generate a permutation using chosen method.</p>

## Output

<p>If the test is generated via Petr's method print "<span class="tex-font-style-tt">Petr</span>" (without quotes). If the test is generated via Alex's method print "<span class="tex-font-style-tt">Um_nik</span>" (without quotes).</p>





```input1
5
2 4 5 1 3

```




```output1
Petr

```



## Note

<p>Please note that the sample is not a valid test (because of limitations for $n$) and is given only to illustrate input/output format. Your program <span class="tex-font-style-bf">still has to print correct answer to this test</span> to get AC.</p><p>Due to randomness of input hacks in this problem are forbidden.</p>
