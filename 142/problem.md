## Description

<div><p>Construct a parentheses sequence consisting of $N$ characters such that it is <span class="tex-font-style-bf">balanced</span> and the length of its <span class="tex-font-style-bf">longest palindromic subsequence (LPS)</span> is exactly $K$. Determine whether such a construction is possible. If there are several possible sequences, construct any of them.</p><p>A parentheses sequence consists of only character <span class="tex-font-style-tt">(</span> and <span class="tex-font-style-tt">)</span>. A parentheses sequence is <span class="tex-font-style-bf">balanced</span> if each character <span class="tex-font-style-tt">(</span> has a corresponding character <span class="tex-font-style-tt">)</span> and the pairs of parentheses are properly nested. For example, <span class="tex-font-style-tt">()</span>, <span class="tex-font-style-tt">(())</span>, <span class="tex-font-style-tt">(())()</span>, and <span class="tex-font-style-tt">((())())</span> are balanced. However, <span class="tex-font-style-tt">)(</span>, <span class="tex-font-style-tt">(()</span>, and <span class="tex-font-style-tt">())</span> are not balanced.</p><p>A sequence is <span class="tex-font-style-bf">palindromic</span> if it reads the same backwards as forwards. For example, <span class="tex-font-style-tt">((</span>, <span class="tex-font-style-tt">)</span>, <span class="tex-font-style-tt">())(</span>, and <span class="tex-font-style-tt">(()((</span> are palindromic. However, <span class="tex-font-style-tt">()</span>, <span class="tex-font-style-tt">)(</span>, and <span class="tex-font-style-tt">(())</span> are not palindromic.</p><p>A <span class="tex-font-style-bf">subsequence</span> can be derived from another sequence by removing zero or more characters without changing the order of the remaining characters. For example, <span class="tex-font-style-tt">(</span>, <span class="tex-font-style-tt">)))</span>, <span class="tex-font-style-tt">())(</span>, and <span class="tex-font-style-tt">(())()</span> are subsequence of <span class="tex-font-style-tt">(())()</span>. However, <span class="tex-font-style-tt">)((</span> and <span class="tex-font-style-tt">((()))</span> are not subsequence of <span class="tex-font-style-tt">(())()</span>.</p><p>The <span class="tex-font-style-bf">longest palindromic subsequence (LPS)</span> of a sequence is a subsequence with the maximum number of characters, derived from that sequence and it is palindromic. For example, the LPS of sequence <span class="tex-font-style-tt">(())()</span> is <span class="tex-font-style-tt">())(</span>, which can be obtained by removing the second and sixth characters. Therefore, the length of the LPS of <span class="tex-font-style-tt">(())()</span> is $4$.</p></div><div class="input-specification"><p>Input consists of two integers $N$ $K$ ($2 \leq N \leq 2000; 1 \leq K \leq N$). $N$ is an even number.</p></div><div class="output-specification"><p>If there is no such parentheses sequence such that it is balanced and the length of its LPS is exactly $K$, then output <span class="tex-font-style-tt">-1</span>.</p><p>Otherwise, output a string of $N$ characters, representing the parentheses sequence. If there are several possible answers, output any of them.</p></div>

## Input

<p>Input consists of two integers $N$ $K$ ($2 \leq N \leq 2000; 1 \leq K \leq N$). $N$ is an even number.</p>

## Output

<p>If there is no such parentheses sequence such that it is balanced and the length of its LPS is exactly $K$, then output <span class="tex-font-style-tt">-1</span>.</p><p>Otherwise, output a string of $N$ characters, representing the parentheses sequence. If there are several possible answers, output any of them.</p>





```input1
6 4
```




```input2
6 3
```




```input3
4 1
```




```input4
14 11
```




```output1
(())()
```




```output2
(()())
```




```output3
-1
```




```output4
()((())()())()
```



## Note

<p><span class="tex-font-style-it">Explanation for the sample input/output #2</span></p><p>The LPS of <span class="tex-font-style-tt">(()())</span> is either <span class="tex-font-style-tt">(((</span> by removing all <span class="tex-font-style-tt">)</span> characters, or <span class="tex-font-style-tt">)))</span> by removing all <span class="tex-font-style-tt">(</span> characters.</p><p>The output <span class="tex-font-style-tt">((()))</span> also satisfies the requirements.</p><p><span class="tex-font-style-it">Explanation for the sample input/output #3</span></p><p>The only possible balanced parentheses sequences are <span class="tex-font-style-tt">(())</span> and <span class="tex-font-style-tt">()()</span>. The length of the LPS of <span class="tex-font-style-tt">(())</span> and <span class="tex-font-style-tt">()()</span> are $2$ and $3$, respectively.</p><p><span class="tex-font-style-it">Explanation for the sample input/output #4</span></p><p>The LPS of <span class="tex-font-style-tt">()((())()())()</span> is <span class="tex-font-style-tt">)())()())()</span>, which can be obtained by removing the first, fourth, and fifth characters.</p>
