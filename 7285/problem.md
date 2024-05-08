## Description

<div><p>When Sasha was studying in the seventh grade, he started listening to music a lot. In order to evaluate which songs he likes more, he introduced the notion of the song's <span class="tex-font-style-it">prettiness</span>. The title of the song is a word consisting of uppercase Latin letters. The <span class="tex-font-style-it">prettiness</span> of the song is the <span class="tex-font-style-it">prettiness</span> of its title.</p><p>Let's define the <span class="tex-font-style-it">simple prettiness</span> of a word as the ratio of the number of vowels in the word to the number of all letters in the word.</p><p>Let's define the <span class="tex-font-style-it">prettiness</span> of a word as the sum of <span class="tex-font-style-it">simple prettiness</span> of all the substrings of the word.</p><p>More formally, let's define the function <span class="tex-span"><i>vowel</i>(<i>c</i>)</span> which is equal to <span class="tex-span">1</span>, if <span class="tex-span"><i>c</i></span> is a vowel, and to <span class="tex-span">0</span> otherwise. Let <span class="tex-span"><i>s</i><sub class="lower-index"><i>i</i></sub></span> be the <span class="tex-span"><i>i</i></span>-th character of string <span class="tex-span"><i>s</i></span>, and <span class="tex-span"><i>s</i><sub class="lower-index"><i>i</i>..<i>j</i></sub></span> be the substring of word <span class="tex-span"><i>s</i></span>, staring at the <span class="tex-span"><i>i</i></span>-th character and ending at the <span class="tex-span"><i>j</i></span>-th character (<span class="tex-span"><i>s</i><sub class="lower-index"><i>is</i></sub><sub class="lower-index"><i>i</i> + 1</sub>... <i>s</i><sub class="lower-index"><i>j</i></sub></span>, <span class="tex-span"><i>i</i> ≤ <i>j</i></span>).</p><p>Then the <span class="tex-font-style-it">simple prettiness</span> of <span class="tex-span"><i>s</i></span> is defined by the formula:</p><center class="tex-equation"><img align="middle" class="tex-formula" src="file://ifCtCqIM.png" style="max-width: 100.0%;max-height: 100.0%;"></center><p>The <span class="tex-font-style-it">prettiness</span> of <span class="tex-span"><i>s</i></span> equals </p><center class="tex-equation"><img align="middle" class="tex-formula" src="file://oq0yLzF9.png" style="max-width: 100.0%;max-height: 100.0%;"></center><p>Find the <span class="tex-font-style-it">prettiness</span> of the given song title.</p><p>We assume that the vowels are <span class="tex-span"><i>I</i>, <i>E</i>, <i>A</i>, <i>O</i>, <i>U</i>, <i>Y</i></span>.</p></div><div class="input-specification"><p>The input contains a single string <span class="tex-span"><i>s</i></span> (<span class="tex-span">1 ≤ |<i>s</i>| ≤ 5·10<sup class="upper-index">5</sup></span>) — the title of the song.</p></div><div class="output-specification"><p>Print the <span class="tex-font-style-it">prettiness</span> of the song with the absolute or relative error of at most <span class="tex-span">10<sup class="upper-index"> - 6</sup></span>.</p></div>

## Input

<p>The input contains a single string <span class="tex-span"><i>s</i></span> (<span class="tex-span">1 ≤ |<i>s</i>| ≤ 5·10<sup class="upper-index">5</sup></span>) — the title of the song.</p>

## Output

<p>Print the <span class="tex-font-style-it">prettiness</span> of the song with the absolute or relative error of at most <span class="tex-span">10<sup class="upper-index"> - 6</sup></span>.</p>





```input1
IEAIAIO

```




```input2
BYOB

```




```input3
YISVOWEL

```




```output1
28.0000000

```




```output2
5.8333333

```




```output3
17.0500000

```



## Note

<p>In the first sample all letters are vowels. The <span class="tex-font-style-it">simple prettiness</span> of each substring is <span class="tex-span">1</span>. The word of length <span class="tex-span">7</span> has <span class="tex-span">28</span> substrings. So, the <span class="tex-font-style-it">prettiness</span> of the song equals to <span class="tex-span">28</span>.</p>
