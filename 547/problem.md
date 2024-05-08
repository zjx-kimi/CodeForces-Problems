## Description

<div><p>A regular bracket sequence is a bracket sequence that can be transformed into a correct arithmetic expression by inserting characters "<span class="tex-font-style-tt">1</span>" and "<span class="tex-font-style-tt">+</span>" between the original characters of the sequence. For example:</p><ul> <li> the bracket sequences "<span class="tex-font-style-tt">()()</span>" and "<span class="tex-font-style-tt">(())</span>" are regular (the resulting expressions are: "<span class="tex-font-style-tt">(1)+(1)</span>" and "<span class="tex-font-style-tt">((1+1)+1)</span>"); </li><li> the bracket sequences "<span class="tex-font-style-tt">)(</span>", "<span class="tex-font-style-tt">(</span>" and "<span class="tex-font-style-tt">)</span>" are not. </li></ul><p>A bracket sequence is called <span class="tex-font-style-it">beautiful</span> if one of the following conditions is satisfied:</p><ul> <li> it is a regular bracket sequence; </li><li> if the order of the characters in this sequence is reversed, it becomes a regular bracket sequence. </li></ul><p>For example, the bracket sequences "<span class="tex-font-style-tt">()()</span>", "<span class="tex-font-style-tt">(())</span>", "<span class="tex-font-style-tt">)))(((</span>", "<span class="tex-font-style-tt">))()((</span>" are beautiful.</p><p>You are given a bracket sequence $s$. You have to color it in such a way that:</p><ul> <li> every bracket is colored into one color; </li><li> for every color, there is at least one bracket colored into that color; </li><li> for every color, if you write down the sequence of brackets having that color in the order they appear, you will get a beautiful bracket sequence. </li></ul><p>Color the given bracket sequence $s$ into the <span class="tex-font-style-bf">minimum</span> number of colors according to these constraints, or report that it is impossible.</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of two lines. The first line contains one integer $n$ ($2 \le n \le 2 \cdot 10^5$) — the number of characters in $s$. The second line contains $s$ — a string of $n$ characters, where each character is either "<span class="tex-font-style-tt">(</span>" or "<span class="tex-font-style-tt">)</span>".</p><p>Additional constraint on the input: the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print the answer as follows:</p><ul> <li> if it is impossible to color the brackets according to the problem statement, print $-1$; </li><li> otherwise, print two lines. In the first line, print one integer $k$ ($1 \le k \le n$) — the minimum number of colors. In the second line, print $n$ integers $c_1, c_2, \dots, c_n$ ($1 \le c_i \le k$), where $c_i$ is the color of the $i$-th bracket. If there are multiple answers, print any of them. </li></ul></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of two lines. The first line contains one integer $n$ ($2 \le n \le 2 \cdot 10^5$) — the number of characters in $s$. The second line contains $s$ — a string of $n$ characters, where each character is either "<span class="tex-font-style-tt">(</span>" or "<span class="tex-font-style-tt">)</span>".</p><p>Additional constraint on the input: the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, print the answer as follows:</p><ul> <li> if it is impossible to color the brackets according to the problem statement, print $-1$; </li><li> otherwise, print two lines. In the first line, print one integer $k$ ($1 \le k \le n$) — the minimum number of colors. In the second line, print $n$ integers $c_1, c_2, \dots, c_n$ ($1 \le c_i \le k$), where $c_i$ is the color of the $i$-th bracket. If there are multiple answers, print any of them. </li></ul>





```input1|2,3,6,7
4
8
((())))(
4
(())
4
))((
3
(()
```




```output1
2
2 2 2 1 2 2 2 1
1
1 1 1 1
1
1 1 1 1
-1
```


