## Description

<div><p>You were walking down the street and heard a sound. The sound was described by the string $s$ consisting of lowercase and uppercase Latin characters. Now you want to find out if the sound was a cat meowing.</p><p>For the sound to be a meowing, the string can only contain the letters '<span class="tex-font-style-tt">m</span>', '<span class="tex-font-style-tt">e</span>', '<span class="tex-font-style-tt">o</span>' and '<span class="tex-font-style-tt">w</span>', in either uppercase or lowercase. Also: </p><ul> <li> string must start with non-empty sequence consisting only of characters '<span class="tex-font-style-tt">m</span>' or '<span class="tex-font-style-tt">M</span>' </li><li> it must be immediately followed by non-empty sequence consisting only of characters '<span class="tex-font-style-tt">e</span>' or '<span class="tex-font-style-tt">E</span>' </li><li> it must be immediately followed by non-empty sequence consisting only of characters '<span class="tex-font-style-tt">o</span>' or '<span class="tex-font-style-tt">O</span>' </li><li> it must be immediately followed by non-empty sequence consisting only of characters '<span class="tex-font-style-tt">w</span>' or '<span class="tex-font-style-tt">W</span>', this sequence ends the string, after it immediately comes the string end </li></ul><p>For example, strings "<span class="tex-font-style-tt">meow</span>", "<span class="tex-font-style-tt">mmmEeOWww</span>", "<span class="tex-font-style-tt">MeOooOw</span>" describe a meowing, but strings "<span class="tex-font-style-tt">Mweo</span>", "<span class="tex-font-style-tt">MeO</span>", "<span class="tex-font-style-tt">moew</span>", "<span class="tex-font-style-tt">MmEW</span>", "<span class="tex-font-style-tt">meowmeow</span>" do not.</p><p>Determine whether the sound you heard was a cat meowing or something else.</p></div><div class="input-specification"><p>The first line of input data contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ ($1 \le n \le 50$) — the length of the string describing the sound.</p><p>The second line of each test case contains a string $s$ of $n$ characters. The string describes the sound you heard and consists only of lowercase and uppercase Latin letters. </p></div><div class="output-specification"><p>For each test case, output on a separate line: </p><ul> <li> <span class="tex-font-style-tt">YES</span> if the sound was a cat meowing; </li><li> <span class="tex-font-style-tt">NO</span> otherwise. </li></ul><p>You can output <span class="tex-font-style-tt">YES</span> and <span class="tex-font-style-tt">NO</span> in any case (for example, strings <span class="tex-font-style-tt">yEs</span>, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span> and <span class="tex-font-style-tt">YES</span> will be recognized as positive response).</p></div>

## Input

<p>The first line of input data contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ ($1 \le n \le 50$) — the length of the string describing the sound.</p><p>The second line of each test case contains a string $s$ of $n$ characters. The string describes the sound you heard and consists only of lowercase and uppercase Latin letters. </p>

## Output

<p>For each test case, output on a separate line: </p><ul> <li> <span class="tex-font-style-tt">YES</span> if the sound was a cat meowing; </li><li> <span class="tex-font-style-tt">NO</span> otherwise. </li></ul><p>You can output <span class="tex-font-style-tt">YES</span> and <span class="tex-font-style-tt">NO</span> in any case (for example, strings <span class="tex-font-style-tt">yEs</span>, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span> and <span class="tex-font-style-tt">YES</span> will be recognized as positive response).</p>





```input1|2,3,6,7,10,11,14,15
7
4
meOw
14
mMmeoOoWWWwwwW
3
mew
7
MmeEeUw
4
MEOW
6
MmyaVW
5
meowA
```




```output1
YES
YES
NO
NO
YES
NO
NO
```



## Note

<p>In the first test case, the string consists of a sequence of characters '<span class="tex-font-style-tt">m</span>', '<span class="tex-font-style-tt">e</span>', '<span class="tex-font-style-tt">O</span>', '<span class="tex-font-style-tt">w</span>', which satisfies the definition of meowing.</p><p>In the second test case, the string consists of a sequence of $3$ characters '<span class="tex-font-style-tt">m</span>' and '<span class="tex-font-style-tt">M</span>', one '<span class="tex-font-style-tt">e</span>', a sequence of $3$ characters '<span class="tex-font-style-tt">o</span>' and '<span class="tex-font-style-tt">O</span>' and a sequence of $7$ characters '<span class="tex-font-style-tt">w</span>' and '<span class="tex-font-style-tt">W</span>', which satisfies the definition of meowing.</p><p>In the third test case, the string does not describe a meowing because it lacks a sequence of '<span class="tex-font-style-tt">o</span>' or '<span class="tex-font-style-tt">O</span>' characters between '<span class="tex-font-style-tt">e</span>' and '<span class="tex-font-style-tt">w</span>'.</p><p>In the fourth test case, the string contains the character '<span class="tex-font-style-tt">U</span>', so it does not describe a meowing.</p>
