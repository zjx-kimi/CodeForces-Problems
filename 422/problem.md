## Description

<div><p>A bracket sequence is a string consisting of characters '<span class="tex-font-style-tt">(</span>' and/or '<span class="tex-font-style-tt">)</span>'. A regular bracket sequence is a bracket sequence that can be transformed into a correct arithmetic expression by inserting characters '<span class="tex-font-style-tt">1</span>' and '<span class="tex-font-style-tt">+</span>' between the original characters of the sequence. For example:</p><ul> <li> bracket sequences "<span class="tex-font-style-tt">()()</span>" and "<span class="tex-font-style-tt">(())</span>" are regular (they can be transformed into "<span class="tex-font-style-tt">(1)+(1)</span>" and "<span class="tex-font-style-tt">((1+1)+1)</span>", respectively); </li><li> bracket sequences "<span class="tex-font-style-tt">)(</span>", "<span class="tex-font-style-tt">(</span>" and "<span class="tex-font-style-tt">)</span>" are not regular. </li></ul><p>You are given a bracket sequence $s$; let's define its length as $n$. Your task is to find a regular bracket sequence $t$ of length $2n$ such that $s$ <span class="tex-font-style-bf">does not</span> occur in $t$ as a <span class="tex-font-style-bf">contiguous substring</span>, or report that there is no such sequence.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains a string $s$ ($2 \le |s| \le 50$), consisting of characters "<span class="tex-font-style-tt">(</span>" and/or "<span class="tex-font-style-tt">)</span>".</p></div><div class="output-specification"><p>For each test case, print the answer to it. If there is no required regular bracket sequence, print <span class="tex-font-style-tt">NO</span> in a separate line. Otherwise, print <span class="tex-font-style-tt">YES</span> in the first line, and the required regular bracket sequence $t$ itself in the second line. If there are multiple answers — you may print any of them.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains a string $s$ ($2 \le |s| \le 50$), consisting of characters "<span class="tex-font-style-tt">(</span>" and/or "<span class="tex-font-style-tt">)</span>".</p>

## Output

<p>For each test case, print the answer to it. If there is no required regular bracket sequence, print <span class="tex-font-style-tt">NO</span> in a separate line. Otherwise, print <span class="tex-font-style-tt">YES</span> in the first line, and the required regular bracket sequence $t$ itself in the second line. If there are multiple answers — you may print any of them.</p>





```input1|2,4
4
)(
(()
()
))()
```




```output1
YES
(())
YES
()()()
NO
YES
()(()())
```


