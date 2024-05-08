## Description

<div><p>Lura was bored and decided to make a simple language using the five letters $\texttt{a}$, $\texttt{b}$, $\texttt{c}$, $\texttt{d}$, $\texttt{e}$. There are two types of letters: </p><ul> <li> <span class="tex-font-style-it">vowels</span>&nbsp;— the letters $\texttt{a}$ and $\texttt{e}$. They are represented by $\textsf{V}$. </li><li> <span class="tex-font-style-it">consonants</span>&nbsp;— the letters $\texttt{b}$, $\texttt{c}$, and $\texttt{d}$. They are represented by $\textsf{C}$. </li></ul> There are two types of <span class="tex-font-style-it">syllables</span> in the language: $\textsf{CV}$ (consonant followed by vowel) or $\textsf{CVC}$ (vowel with consonant before and after). For example, $\texttt{ba}$, $\texttt{ced}$, $\texttt{bab}$ are syllables, but $\texttt{aa}$, $\texttt{eda}$, $\texttt{baba}$ are not.<p>A <span class="tex-font-style-it">word</span> in the language is a sequence of syllables. Lura has written a word in the language, but she doesn't know how to split it into syllables. Help her break the word into syllables.</p><p>For example, given the word $\texttt{bacedbab}$, it would be split into syllables as $\texttt{ba.ced.bab}$ (the dot $\texttt{.}$ represents a syllable boundary).</p></div><div class="input-specification"><p>The input consists of multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 100$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ ($1 \leq n \leq 2 \cdot 10^5$)&nbsp;— the length of the word.</p><p>The second line of each test case contains a string consisting of $n$ lowercase Latin characters &nbsp;— the word. </p><p>All words given are valid words in the language; that is, they only use the letters $\texttt{a}$, $\texttt{b}$, $\texttt{c}$, $\texttt{d}$, $\texttt{e}$, and each word is made up of several syllables.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For test case, output a string denoting the word split into syllables by inserting a dot $\texttt{.}$ between every pair of adjacent syllables.</p><p>If there are multiple possible splittings, output any of them. The input is given in such a way that at least one possible splitting exists.</p></div>

## Input

<p>The input consists of multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 100$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ ($1 \leq n \leq 2 \cdot 10^5$)&nbsp;— the length of the word.</p><p>The second line of each test case contains a string consisting of $n$ lowercase Latin characters &nbsp;— the word. </p><p>All words given are valid words in the language; that is, they only use the letters $\texttt{a}$, $\texttt{b}$, $\texttt{c}$, $\texttt{d}$, $\texttt{e}$, and each word is made up of several syllables.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For test case, output a string denoting the word split into syllables by inserting a dot $\texttt{.}$ between every pair of adjacent syllables.</p><p>If there are multiple possible splittings, output any of them. The input is given in such a way that at least one possible splitting exists.</p>





```input1|2,3,6,7,10,11
6
8
bacedbab
4
baba
13
daddecabeddad
3
dac
6
dacdac
22
dababbabababbabbababba
```




```output1
ba.ced.bab
ba.ba
dad.de.ca.bed.dad
dac
dac.dac
da.bab.ba.ba.bab.bab.ba.bab.ba
```


