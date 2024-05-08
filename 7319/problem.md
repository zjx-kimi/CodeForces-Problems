## Description

<div><p>You have a new professor of graph theory and he speaks very quickly. You come up with the following plan to keep up with his lecture and make notes.</p><p>You know two languages, and the professor is giving the lecture in the first one. The words in both languages consist of lowercase English characters, each language consists of several words. For each language, all words are distinct, i.e. they are spelled differently. Moreover, the words of these languages have a one-to-one correspondence, that is, for each word in each language, there exists exactly one word in the other language having has the same meaning.</p><p>You can write down every word the professor says in either the first language or the second language. Of course, during the lecture you write down each word in the language in which the word is shorter. In case of equal lengths of the corresponding words you prefer the word of the first language.</p><p>You are given the text of the lecture the professor is going to read. Find out how the lecture will be recorded in your notes.</p></div><div class="input-specification"><p>The first line contains two integers, <span class="tex-span"><i>n</i></span> and <span class="tex-span"><i>m</i></span> (<span class="tex-span">1 ≤ <i>n</i> ≤ 3000</span>, <span class="tex-span">1 ≤ <i>m</i> ≤ 3000</span>) — the number of words in the professor's lecture and the number of words in each of these languages.</p><p>The following <span class="tex-span"><i>m</i></span> lines contain the words. The <span class="tex-span"><i>i</i></span>-th line contains two strings <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub></span>, <span class="tex-span"><i>b</i><sub class="lower-index"><i>i</i></sub></span> meaning that the word <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub></span> belongs to the first language, the word <span class="tex-span"><i>b</i><sub class="lower-index"><i>i</i></sub></span> belongs to the second language, and these two words have the same meaning. It is guaranteed that no word occurs in both languages, and each word occurs in its language exactly once.</p><p>The next line contains <span class="tex-span"><i>n</i></span> space-separated strings <span class="tex-span"><i>c</i><sub class="lower-index">1</sub>, <i>c</i><sub class="lower-index">2</sub>, ..., <i>c</i><sub class="lower-index"><i>n</i></sub></span> — the text of the lecture. It is guaranteed that each of the strings <span class="tex-span"><i>c</i><sub class="lower-index"><i>i</i></sub></span> belongs to the set of strings <span class="tex-span">{<i>a</i><sub class="lower-index">1</sub>, <i>a</i><sub class="lower-index">2</sub>, ... <i>a</i><sub class="lower-index"><i>m</i></sub>}</span>.</p><p>All the strings in the input are non-empty, each consisting of no more than <span class="tex-span">10</span> lowercase English letters.</p></div><div class="output-specification"><p>Output exactly <span class="tex-span"><i>n</i></span> words: how you will record the lecture in your notebook. Output the words of the lecture in the same order as in the input.</p></div>

## Input

<p>The first line contains two integers, <span class="tex-span"><i>n</i></span> and <span class="tex-span"><i>m</i></span> (<span class="tex-span">1 ≤ <i>n</i> ≤ 3000</span>, <span class="tex-span">1 ≤ <i>m</i> ≤ 3000</span>) — the number of words in the professor's lecture and the number of words in each of these languages.</p><p>The following <span class="tex-span"><i>m</i></span> lines contain the words. The <span class="tex-span"><i>i</i></span>-th line contains two strings <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub></span>, <span class="tex-span"><i>b</i><sub class="lower-index"><i>i</i></sub></span> meaning that the word <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub></span> belongs to the first language, the word <span class="tex-span"><i>b</i><sub class="lower-index"><i>i</i></sub></span> belongs to the second language, and these two words have the same meaning. It is guaranteed that no word occurs in both languages, and each word occurs in its language exactly once.</p><p>The next line contains <span class="tex-span"><i>n</i></span> space-separated strings <span class="tex-span"><i>c</i><sub class="lower-index">1</sub>, <i>c</i><sub class="lower-index">2</sub>, ..., <i>c</i><sub class="lower-index"><i>n</i></sub></span> — the text of the lecture. It is guaranteed that each of the strings <span class="tex-span"><i>c</i><sub class="lower-index"><i>i</i></sub></span> belongs to the set of strings <span class="tex-span">{<i>a</i><sub class="lower-index">1</sub>, <i>a</i><sub class="lower-index">2</sub>, ... <i>a</i><sub class="lower-index"><i>m</i></sub>}</span>.</p><p>All the strings in the input are non-empty, each consisting of no more than <span class="tex-span">10</span> lowercase English letters.</p>

## Output

<p>Output exactly <span class="tex-span"><i>n</i></span> words: how you will record the lecture in your notebook. Output the words of the lecture in the same order as in the input.</p>





```input1
4 3
codeforces codesecrof
contest round
letter message
codeforces contest letter contest

```




```input2
5 3
joll wuqrd
euzf un
hbnyiyc rsoqqveh
hbnyiyc joll joll euzf joll

```




```output1
codeforces round letter round

```




```output2
hbnyiyc joll joll un joll

```


