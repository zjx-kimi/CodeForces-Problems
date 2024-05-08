## Description

<div><p>Jabber ID on the national Berland service «Babber» has a form <span class="tex-font-style-tt">&lt;username&gt;@&lt;hostname&gt;[/resource]</span>, where </p><ul> <li> <span class="tex-font-style-tt">&lt;username&gt;</span> — is a sequence of Latin letters (lowercase or uppercase), digits or underscores characters «<span class="tex-font-style-tt">_</span>», the length of <span class="tex-font-style-tt">&lt;username&gt;</span> is between 1 and 16, inclusive. </li><li> <span class="tex-font-style-tt">&lt;hostname&gt;</span> — is a sequence of word separated by periods (characters «<span class="tex-font-style-tt">.</span>»), where each word should contain only characters allowed for <span class="tex-font-style-tt">&lt;username&gt;</span>, the length of each word is between 1 and 16, inclusive. The length of <span class="tex-font-style-tt">&lt;hostname&gt;</span> is between 1 and 32, inclusive. </li><li> <span class="tex-font-style-tt">&lt;resource&gt;</span> — is a sequence of Latin letters (lowercase or uppercase), digits or underscores characters «<span class="tex-font-style-tt">_</span>», the length of <span class="tex-font-style-tt">&lt;resource&gt;</span> is between 1 and 16, inclusive. </li></ul><p>The content of square brackets is optional — it can be present or can be absent.</p><p>There are the samples of correct Jabber IDs: <span class="tex-font-style-tt"><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="f19c989a94b1929e9594979e83929482df929e9c">[email&nbsp;protected]</a></span>, <span class="tex-font-style-tt"><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="1929292e597c77377a767d7c7f766b7a7c6a377a7674">[email&nbsp;protected]</a>/contest</span>.</p><p>Your task is to write program which checks if given string is a correct Jabber ID.</p></div><div class="input-specification"><p>The input contains of a single line. The line has the length between 1 and 100 characters, inclusive. Each characters has ASCII-code between 33 and 127, inclusive.</p></div><div class="output-specification"><p>Print <span class="tex-font-style-tt">YES</span> or <span class="tex-font-style-tt">NO</span>.</p></div>

## Input

<p>The input contains of a single line. The line has the length between 1 and 100 characters, inclusive. Each characters has ASCII-code between 33 and 127, inclusive.</p>

## Output

<p>Print <span class="tex-font-style-tt">YES</span> or <span class="tex-font-style-tt">NO</span>.</p>





```input1
<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="f09d999b95b0939f9495969f82939583de939f9d">[email&nbsp;protected]</a>

```




```input2
<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="3953565157174a54504d51795a565d5c5f564b5a5c4a174b4c">[email&nbsp;protected]</a>/contest.icpc/12

```




```output1
YES

```




```output2
NO

```


