## Description

<div><p>After holding one team contest, boy Yura got very tired and wanted to change his life and move to Japan. In honor of such a change, Yura changed his name to something nice.</p><p>Fascinated by this idea he already thought up a name $s$ consisting only of characters "<span class="tex-font-style-tt">_</span>" and "<span class="tex-font-style-tt">^</span>". But there's a problem — Yura likes smiley faces "<span class="tex-font-style-tt">^_^</span>" and "<span class="tex-font-style-tt">^^</span>". Therefore any character of the name must be a part of at least one such smiley. Note that only the <span class="tex-font-style-bf">consecutive</span> characters of the name can be a smiley face.</p><p>More formally, consider all occurrences of the strings "<span class="tex-font-style-tt">^_^</span>" and "<span class="tex-font-style-tt">^^</span>" in the string $s$. Then all such occurrences must cover the whole string $s$, possibly with intersections. For example, in the string "<span class="tex-font-style-tt">^^__^_^^__^</span>" the characters at positions $3,4,9,10$ and $11$ are not contained inside any smileys, and the other characters at positions $1,2,5,6,7$ and $8$ are contained inside smileys.</p><p>In one operation Jura can insert one of the characters "<span class="tex-font-style-tt">_</span>" and "<span class="tex-font-style-tt">^</span>" into his name $s$ (you can insert it at any position in the string). He asks you to tell him the minimum number of operations you need to do to make the name fit Yura's criteria.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 100$)&nbsp;—the number of test cases. The description of test cases follows.</p><p>The first and only line of each test case contains a single string $s$ ($1 \leq |s| \leq 100$), consisting of characters "<span class="tex-font-style-tt">_</span>" and "<span class="tex-font-style-tt">^</span>", &nbsp;— the name to change.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the minimum number of characters you need to add to the name to make it fit for Yura. If you don't need to change anything in the name, print $0$.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 100$)&nbsp;—the number of test cases. The description of test cases follows.</p><p>The first and only line of each test case contains a single string $s$ ($1 \leq |s| \leq 100$), consisting of characters "<span class="tex-font-style-tt">_</span>" and "<span class="tex-font-style-tt">^</span>", &nbsp;— the name to change.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the minimum number of characters you need to add to the name to make it fit for Yura. If you don't need to change anything in the name, print $0$.</p>





```input1|2,4,6,8
7
^______^
___^_^^^_^___^
^_
^
^_^^^^^_^_^^
___^^
_
```




```output1
5
5
1
1
0
3
2
```



## Note

<p>In the first test case, you can get the following name by adding $5$ characters: </p><p><span class="tex-font-style-tt">^_</span><span class="tex-font-style-bf">^</span><span class="tex-font-style-tt">_</span><span class="tex-font-style-bf">^</span><span class="tex-font-style-tt">_</span><span class="tex-font-style-bf">^</span><span class="tex-font-style-tt">_</span><span class="tex-font-style-bf">^</span><span class="tex-font-style-tt">_</span><span class="tex-font-style-bf">^</span><span class="tex-font-style-tt">_^</span></p><p>In the third test case, we can add one character "<span class="tex-font-style-tt">^</span>" to the end of the name, then we get the name:</p><p><span class="tex-font-style-tt">^_</span><span class="tex-font-style-bf">^</span></p><p>In the fourth test case, we can add one character "<span class="tex-font-style-tt">^</span>" to the end of the name, then we get the name:</p><p>^<span class="tex-font-style-bf">^</span></p><p>In the fifth test case, all of the characters are already contained in smiley faces, so the answer is $0$.</p><p>In the seventh test case, you can add one character "<span class="tex-font-style-tt">^</span>" at the beginning of the name and one character "<span class="tex-font-style-tt">^</span>" at the end of the name, then you get the name:</p><p><span class="tex-font-style-bf">^</span><span class="tex-font-style-tt">_</span><span class="tex-font-style-bf">^</span></p>
