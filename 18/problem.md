## Description

<div><p>You are given two integers $n$ and $k$ along with a string $s$.</p><p>Your task is to check whether all possible strings of length $n$ that can be formed using the first $k$ lowercase English alphabets occur as a subsequence of $s$. If the answer is <span class="tex-font-style-tt">NO</span>, you also need to print a string of length $n$ that can be formed using the first $k$ lowercase English alphabets which does not occur as a subsequence of $s$.</p><p>If there are multiple answers, you may print any of them.</p><p><span class="tex-font-style-bf">Note:</span> A string $a$ is called a subsequence of another string $b$ if $a$ can be obtained by deleting some (possibly zero) characters from $b$ without changing the order of the remaining characters.</p></div><div class="input-specification"><p>The first line of input contains a single integer $t \, (1 \le t \le 10^5)$, the number of test cases.</p><p>The first line of each test case contains $3$ integers $n \, (1 \le n \le 26), \: k \, (1 \le k \le 26), \: m \, (1 \le m \le 1000)$, where $n$ and $k$ are the same as described in the input and $m$ is the length of the string $s$.</p><p>The second line of each test case contains a single string $s$ of length $m$, comprising only of the first $k$ lowercase English alphabets.</p><p>It is guaranteed that the sum of $m$ and the sum of $n$ over all test cases does not exceed $10^6$.</p></div><div class="output-specification"><p>For each test case, print <span class="tex-font-style-tt">YES</span> if all possible strings of length $n$ that can be formed using the first $k$ lowercase English alphabets occur as a subsequence of $s$, else print <span class="tex-font-style-tt">NO</span>.</p><p>If your answer is <span class="tex-font-style-tt">NO</span>, print a string of length $n$ that can be formed using the first $k$ lowercase English alphabets which does not occur as a subsequence of $s$ in the next line.</p><p>You may print each letter of <span class="tex-font-style-tt">YES</span> or <span class="tex-font-style-tt">NO</span> in any case (for example, <span class="tex-font-style-tt">YES</span>, <span class="tex-font-style-tt">yES</span>, <span class="tex-font-style-tt">YeS</span> will all be recognized as a positive answer).</p></div>

## Input

<p>The first line of input contains a single integer $t \, (1 \le t \le 10^5)$, the number of test cases.</p><p>The first line of each test case contains $3$ integers $n \, (1 \le n \le 26), \: k \, (1 \le k \le 26), \: m \, (1 \le m \le 1000)$, where $n$ and $k$ are the same as described in the input and $m$ is the length of the string $s$.</p><p>The second line of each test case contains a single string $s$ of length $m$, comprising only of the first $k$ lowercase English alphabets.</p><p>It is guaranteed that the sum of $m$ and the sum of $n$ over all test cases does not exceed $10^6$.</p>

## Output

<p>For each test case, print <span class="tex-font-style-tt">YES</span> if all possible strings of length $n$ that can be formed using the first $k$ lowercase English alphabets occur as a subsequence of $s$, else print <span class="tex-font-style-tt">NO</span>.</p><p>If your answer is <span class="tex-font-style-tt">NO</span>, print a string of length $n$ that can be formed using the first $k$ lowercase English alphabets which does not occur as a subsequence of $s$ in the next line.</p><p>You may print each letter of <span class="tex-font-style-tt">YES</span> or <span class="tex-font-style-tt">NO</span> in any case (for example, <span class="tex-font-style-tt">YES</span>, <span class="tex-font-style-tt">yES</span>, <span class="tex-font-style-tt">YeS</span> will all be recognized as a positive answer).</p>





```input1|2,3,6,7
3
2 2 4
abba
2 2 3
abb
3 3 10
aabbccabab
```




```output1
YES
NO
aa
NO
ccc
```



## Note

<p>For the first test case, all possible strings (<span class="tex-font-style-tt">aa</span>, <span class="tex-font-style-tt">ab</span>, <span class="tex-font-style-tt">ba</span>, <span class="tex-font-style-tt">bb</span>) of length $2$ that can be formed using the first $2$ English alphabets occur as a subsequence of <span class="tex-font-style-tt">abba</span>.</p><p>For the second test case, the string <span class="tex-font-style-tt">aa</span> is not a subsequence of <span class="tex-font-style-tt">abb</span>.</p>
