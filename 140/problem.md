## Description

<div><p>Polycarp has a problem — his laptop keyboard is broken.</p><p>Now, when he presses the '<span class="tex-font-style-tt">b</span>' key, it acts like an unusual backspace: it deletes the last (rightmost) lowercase letter in the typed string. If there are no lowercase letters in the typed string, then the press is completely ignored.</p><p>Similarly, when he presses the '<span class="tex-font-style-tt">B</span>' key, it deletes the last (rightmost) uppercase letter in the typed string. If there are no uppercase letters in the typed string, then the press is completely ignored.</p><p>In both cases, the letters '<span class="tex-font-style-tt">b</span>' and '<span class="tex-font-style-tt">B</span>' are not added to the typed string when these keys are pressed.</p><p>Consider an example where the sequence of key presses was "<span class="tex-font-style-tt">ARaBbbitBaby</span>". In this case, the typed string will change as follows: <span class="tex-font-style-tt">""</span> $\xrightarrow{\texttt{A}}$ <span class="tex-font-style-tt">"A"</span> $\xrightarrow{\texttt{R}}$ <span class="tex-font-style-tt">"AR"</span> $\xrightarrow{\texttt{a}}$ <span class="tex-font-style-tt">"ARa"</span> $\xrightarrow{\texttt{B}}$ <span class="tex-font-style-tt">"Aa"</span> $\xrightarrow{\texttt{b}}$ <span class="tex-font-style-tt">"A"</span> $\xrightarrow{\texttt{b}}$ <span class="tex-font-style-tt">"A"</span> $\xrightarrow{\texttt{i}}$ <span class="tex-font-style-tt">"Ai"</span> $\xrightarrow{\texttt{t}}$ <span class="tex-font-style-tt">"Ait"</span> $\xrightarrow{\texttt{B}}$ <span class="tex-font-style-tt">"it"</span> $\xrightarrow{\texttt{a}}$ <span class="tex-font-style-tt">"ita"</span> $\xrightarrow{\texttt{b}}$ <span class="tex-font-style-tt">"it"</span> $\xrightarrow{\texttt{y}}$ <span class="tex-font-style-tt">"ity"</span>.</p><p>Given a sequence of pressed keys, output the typed string after processing all key presses.</p></div><div class="input-specification"><p>The first line of the input data contains an integer $t$ ($1 \le t \le 1000$), the number of test cases in the test.</p><p>The following contains $t$ non-empty lines, which consist of lowercase and uppercase letters of the Latin alphabet.</p><p>It is guaranteed that each line contains at least one letter and the sum of the lengths of the lines does not exceed $10^6$.</p></div><div class="output-specification"><p>For each test case, output the result of processing the key presses on a separate line. If the typed string is empty, then output an empty line.</p></div>

## Input

<p>The first line of the input data contains an integer $t$ ($1 \le t \le 1000$), the number of test cases in the test.</p><p>The following contains $t$ non-empty lines, which consist of lowercase and uppercase letters of the Latin alphabet.</p><p>It is guaranteed that each line contains at least one letter and the sum of the lengths of the lines does not exceed $10^6$.</p>

## Output

<p>For each test case, output the result of processing the key presses on a separate line. If the typed string is empty, then output an empty line.</p>





```input1|2,4,6,8,10,12
12
ARaBbbitBaby
YetAnotherBrokenKeyboard
Bubble
Improbable
abbreviable
BbBB
BusyasaBeeinaBedofBloomingBlossoms
CoDEBARbIES
codeforces
bobebobbes
b
TheBBlackbboard
```




```output1
ity
YetnotherrokenKeoard
le
Imprle
revile

usyasaeeinaedofloominglossoms
CDARIES
codeforces
es

helaoard
```


